# Load Balancer Access Log

## 說明

Load Balancer 的 Access Log 存放在 S3，在啟用 Access Log 時，必須授權給 Load Balancer 有存取 S3 的權限

## 授權 Load Balancer 存取 S3 權限

[AWS Policy Generator](http://awspolicygen.s3.amazonaws.com/policygen.html)

* Select Type of Policy: 選擇 S3 Bucket Policy
* Effect: 選擇 Allow
* Principal: 輸入所屬區域 Elastic Load Balancing 帳戶編號，若允許多個則使用逗號分格（,）
* Actions: 選擇 PutObject
* Amazon Resource Name (ARN): arn:aws:s3:::bucket/prefix/AWSLogs/aws-account-id/*

> aws-account-id 輸入自己 AWS 帳號編號，在 [AWS Support](https://console.aws.amazon.com/support/home) 右上方可以看到自己的 Account Number

* 點選 `Generate Policy` 產生 Policy

## 設定 S3 權限

* 進入 S3 選擇 Log 的 bucket，點選右上方 `Properties` 頁籤
* 在 `Permissions` 區塊點選 `Edit Bucket Policy`，將剛剛產生的 policy 貼上並儲存即可

## 參考資料
* [为负载均衡器启用访问日志 - Elastic Load Balancing](http://docs.aws.amazon.com/zh_cn/elasticloadbalancing/latest/classic/enable-access-logs.html)
* [Classic负载均衡器的访问日志 - Elastic Load Balancing](http://docs.aws.amazon.com/zh_cn/elasticloadbalancing/latest/classic/access-log-collection.html)
* [AWS Policy Generator](http://awspolicygen.s3.amazonaws.com/policygen.html)
* [AWS Support](https://console.aws.amazon.com/support/home)