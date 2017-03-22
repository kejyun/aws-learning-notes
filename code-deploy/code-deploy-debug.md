# Code Deploy Debug

## S3

若是把程式放在 S3 的話，記得在 IAM Role 中設定 S3 的存取權限，可以使用 `Attach Polocy` 將 S3 的權限加入，或者可以用 `Inline Policy` 將權限加入，這樣才可以正常 Deploy

```json
{
    "Version": "2012-10-17",
    "Statement": [
      {
          "Action": [
              "s3:Get*",
              "s3:List*"
          ],
          "Effect": "Allow",
          "Resource": "*"
      }
    ]
}
```

![Images](./images/code-deploy-debug-s3-permission.png)

若沒有正確的設定權限，則會看到 `DownloadBundle` 的 `Access Denied` 的訊息

![Images](./images/code-deploy-debug-s3-permission-download-bundle.png)

![Images](./images/code-deploy-debug-s3-permission-download-bundle-access-denied.png)



## Log

若要看到操作過程的相關 Log，可以到 EC2 下，找到下列目錄，就可以看到相關的存取 Log

#### 流程紀錄

```
less /var/log/aws/codedeploy-agent/codedeploy-agent.log
```

#### 部署記錄

```
less /opt/codedeploy-agent/deployment-root/`deployment-group-ID`/`deployment-ID`/logs/scripts.log
```

 - deployment-group-ID：由 Code Deploy 產生的 Deploy Group 代號
 - deployment-ID：在產生新的 Deploy 時，會有自己特定的部署編號，會長的像 `d-6CTSMH2MK`

![Images](./images/code-deploy-debug-log-deployment-id.png)


## 參考資料
* [Troubleshoot Instance Issues - AWS CodeDeploy](http://docs.aws.amazon.com/codedeploy/latest/userguide/troubleshooting-ec2-instances.html)
* [View AWS CodeDeploy logs in Amazon CloudWatch console | AWS DevOps Blog](https://aws.amazon.com/blogs/devops/view-aws-codedeploy-logs-in-amazon-cloudwatch-console/)
* [http://docs.aws.amazon.com/codedeploy/latest/userguide/troubleshooting-deployments.html](Troubleshoot Deployment Issues - AWS CodeDeploy)
