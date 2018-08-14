# Instance 實例

## T2 Instance CPU Credit


### 參考資料
* [CPU 积分和基准性能 - Amazon Elastic Compute Cloud](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/t2-credits-baseline-concepts.html)


## T2 Unlimited

在使用 T2 EC2 主機時，會有 CPU credit 的問題，當 CPU Credit 使用完時，主機會進入無法進行運算的狀態，AWS 使用 `T2 Unlimited` 的方式，讓我們可以預支未來 24 小時的 CPU Credit 給目前繁忙的主機運算使用，但當可以預支的 CPU Credit 預支完時，AWS 會依照 vCPU 運算資源去做收費 `$0.05 / hour per vCPU`

| T2 類型  | vCPU	  | Over T2 limit 價格  | On-demand 價格 |
|---|---|---|---|
| t2.nano    | 1 |  $0.05 / hour | $0.0076 / hour |
| t2.micro	 | 1 |  $0.05 / hour | $0.0152 / hour |
| t2.small	 | 1 |  $0.05 / hour | $0.0304 / hour |
| t2.medium	 | 2 |  $0.1 / hour | $0.0608 / hour |
| t2.large	 | 2 |  $0.1 / hour | $0.1216 / hour |
| t2.xlarge	 | 4 |  $0.2 / hour | $0.2432 / hour |
| t2.2xlarge | 8 |  $0.4 / hour | $0.4864 / hour |


### 參考資料
* [T2 无限 - Amazon Elastic Compute Cloud](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/t2-unlimited.html)
* [使用 T2 实例 - Amazon Elastic Compute Cloud](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/t2-how-to.html#modify-t2)
* [EC2 執行個體定價 – Amazon Web Services (AWS)](https://aws.amazon.com/tw/ec2/pricing/on-demand/)
