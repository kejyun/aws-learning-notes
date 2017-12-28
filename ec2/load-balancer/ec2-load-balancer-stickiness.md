# AWS Load Balancer Stickiness


在 AWS Load Balancer 中可以看到 Stickness 的設定，開啟 Stickness 表示 Load Balancer 會針對同一個使用者的請求，會使用指向同一台 EC2 機器。

![AWS Load Balancer Stickiness 設定](./images/load-balancer-stickiness-setting.png)

在 Stickness 設定視窗中你會看到有三個設定方式

 1. Disable stickiness
 2. Enable load balancer generated cookie stickiness
 3. Enable application generated cookie stickiness

![AWS Load Balancer Stickiness 設定視窗](./images/load-balancer-stickiness-setting-dialog.png)

## Stickness 設定方式

「Load Balancer」與「application generated」設定方式的差異分別如下

### Enable Load Balancer Generated Cookie Stickiness

Load Balancer 會自己加入一個自己的 Cookie 資訊到瀏覽器，並設定 Cookie 的失效時間，Load Balancer 會自行控制該 Cookie 的狀況

![AWS Load Balancer Stickiness 設定視窗](./images/load-balancer-stickiness-setting-dialog-load-balancer-generated-cookie-stickiness.png)

### Enable application generated cookie stickiness

Load Balancer 會針對使用者自己網站的 cookie，去分配流量到機器的狀況，由使用者自己網站的應用程式自行去控制 Cookie 的過期時間。

![AWS Load Balancer Stickiness 設定視窗](./images/load-balancer-stickiness-setting-dialog-application-generated-cookie-stickiness.png)

## 參考資料
* [amazon ec2 - EC2 load balancer - difference between "Load Balancer" and "Application" Generated Cookie Stickiness - Server Fault](https://serverfault.com/questions/435431/ec2-load-balancer-difference-between-load-balancer-and-application-generat)