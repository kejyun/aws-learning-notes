# Auto Scaling 規則


## Placing Spot instance request

在做 Auto Scaling 時，機器會一直不段的開開關關，且顯示 `Placing Spot instance request` 的訊息，這個是表示 **Scaling Policies** 規則中，Scale-up 與 Scale-down 的規則相互有衝突導致，此時必須要檢查一下規則是否有設定錯誤。

```
Placing Spot instance request. Status Reason: Spot instance request: sir-bcpgayih has been cancelled. Group size decreased while waiting for Spot instance request to be fulfilled.
```

```
At 2017-10-26T07:53:21Z a monitor alarm CPU Too Low in state ALARM triggered policy CPU Too Low changing the desired capacity from 2 to 1. At 2017-10-26T07:54:04Z a monitor alarm CPU Credit Too Low in state ALARM triggered policy CPU Credit Too Low changing the desired capacity from 1 to 2. At 2017-10-26T07:54:14Z a difference between desired and actual capacity changing the desired capacity, increasing the capacity from 1 to 2.
```

### 參考資料
* [AWS Developer Forums: Some spot requests for Auto Scale group ...](https://forums.aws.amazon.com/thread.jspa?threadID=159903)