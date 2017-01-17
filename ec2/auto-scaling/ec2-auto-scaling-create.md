# 建立 Auto Scaling

# 建立設定檔

Auto Scaling / Launch Configurations / Create launch configuration

![Images](./images/ec2-auto-scaling-create-dashboard-create-btn.png)

## 選擇自己的 AMI 映像檔

![Images](./images/ec2-auto-scaling-create-launch-configuration.png)

## 選擇機器類型

![Images](./images/ec2-auto-scaling-create-choose-instance-type.png)

## 設定細節

設定設定檔名稱
若有選擇用 Spot Instance 的話，則需要設定最大出價價格（上方為目前的 spot instance 目前價格）

![Images](./images/ec2-auto-scaling-create-configuration-detail.png)

## 設定儲存空間

![Images](./images/ec2-auto-scaling-create-add-storage.png)

## 設定 Security Group

通常會設定 22 (SSH)、80 (HTTP) 與 443 (HTTPS)

![Images](./images/ec2-auto-scaling-create-configuration-security-group.png)

## 建立 Auto Scaling Group

Auto Scaling / Auto Scaling Groups / Create Auto Scaling group

![Images](./images/ec2-auto-scaling-create-auto-scaling-group-btn.png)

## 選擇設定檔

![Images](./images/ec2-auto-scaling-create-select-configuration.png)

## 建立 Group

![Images](./images/ec2-auto-scaling-create-auto-scaling-group.png)


## 建立 Scaling 條件

![Images](./images/ec2-auto-scaling-create-scaling-policles.png)

## 設定 Scaling 的機器在哪些 Load Balancer 下面

![Images](./images/ec2-auto-scaling-create-setting-belong-which-load-balancers.png)


