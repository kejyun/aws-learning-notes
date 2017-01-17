# Auto Scaling 自動部署程式

## 建立 IAM 角色 (Role)

### 設定角色名稱

![Images](./images/code-deploy-auto-scaling-setting-iam-roles-name.png)

### 設定角色類型


![Images](./images/code-deploy-auto-scaling-setting-iam-roles-type.png)

## 設定 Code Deploy

### 選擇部署機器類型

選擇 Auto Scaling Group，當 Auto Scaling 觸發時，則會自動執行程式部署

![Images](./images/code-deploy-auto-scaling-create-deployment-group-select-auto-sacling-group.png)

### 選擇 Deploy IAM Role

![Images](./images/code-deploy-auto-scaling-create-deployment-group-select-iam-role.png)


## EC2 Plugin

請先安裝 [AWS CLI](../ec2/cli/ec2-cli-README.md)

### 安裝 CodeDeploy Agent

```shell
sudo apt-get update
sudo apt-get install python-pip
sudo apt-get install ruby
sudo apt-get install wget
cd /home/ubuntu
wget https://bucket-name.s3.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
```

### 測試 CodeDeploy Agent

```shell
sudo service codedeploy-agent status
sudo service codedeploy-agent start
```

安裝完 Agent 之後，AWS 才可以透過 Agent 自動部署程式

## 參考資料
* [Install or Reinstall the AWS CodeDeploy Agent - AWS CodeDeploy](http://docs.aws.amazon.com/codedeploy/latest/userguide/how-to-run-agent-install.html)
* [Installing the AWS Command Line Interface - AWS Command Line Interface](http://docs.aws.amazon.com/cli/latest/userguide/installing.html#install-bundle-other-os)