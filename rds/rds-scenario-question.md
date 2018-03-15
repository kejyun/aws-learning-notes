# AWS RDS 情境問題

## 建立資料庫 Snapshot 是否會影響正式機器運作？

不會

## 建立 Auto scaling replica 副本前置作業

需要先手動建立自己的 replica 副本，讓 Auto scaling 自動偵測 DB cluster 的 replica reader 的數據（CPU %, DB connection），去做自動擴展

auto scaling replica 不會刪除手動建立的 replica

## 手動建立 replica 副本是否會影響正式機器運作？

不會，所以儘管正式 RDS 正在運作，隨時可以手動建立 replica，不會影響服務運行

## 使用 ab test 測試 writer 及 reader，是否 AWS 會使用 writer 機器來當作讀取用？

不會

## 故障轉移（Failover）使用方式

執行故障轉移時，AWS 會針對 cluster 中所有機器的 Failover priority 優先順序，選擇 priority 中，目前運轉正常的機器，所以不管對哪一台機器做 Failover，則都會對目前所有機器（排除當前的 writer 機器）去做故障轉移。

https://docs.aws.amazon.com/zh_cn/AmazonRDS/latest/UserGuide/CHAP_Troubleshooting.html

## 在有 replica reader 下，刪除 writer 機器的狀況會怎樣？

writer 機器會 Failover 到其他機器，然後再將機器刪除，但機器刪除時，會有短暫的連不到資料庫的狀態

## AutoScaling 開的機器與手動開的機器有何不同？

Auto Scaling 開的機器會顯示「application-autoscaling-一串編碼」的名稱及 endpoint，Auto Scaling 不會關閉手動開的 replica 機器。

## AutoScaling Cloudwatch 是否需要設定？

不需要，僅需要指定要偵測的數值，AWS 會盡量將數值維持在指定的數值內，當高於該數值就會自動開啟機器，低於該數值就會關閉機器。

