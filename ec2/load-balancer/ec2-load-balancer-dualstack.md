# dualstack DNS name

`dualstack` DNS 在使用 `EC2-Classic (Internet-facing, non-VPC) Elastic Load Balancer.` 會回傳 IPv6 及 IPv4 的紀錄，若沒有使用 `dualstack` 的話，則會回傳 IPv4 的紀錄


```
name-1234567890.region.elb.amazonaws.com
```

```
name-123456789.region.elb.amazonaws.com
ipv6.name-123456789.region.elb.amazonaws.com    
dualstack.name-123456789.region.elb.amazonaws.com
```

**EC2-VPC**

> Load balancers in a VPC support IPv4 addresses only. [...]

**EC2-Classic**

> Load balancers in EC2-Classic support both IPv4 and IPv6 addresses. [...]

> The base public DNS name returns only IPv4 records. The public DNS name with the ipv6 prefix returns only IPv6 records. The public DNS name with the dualstack prefix returns both IPv4 and IPv6 records. We recommend that you enable IPv6 support by using the DNS name with the dualstack prefix to ensure that clients can access the load balancer using either IPv4 or IPv6.


## 參考資料
* [Internet-Facing Classic Load Balancers - Elastic Load Balancing](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-internet-facing-load-balancers.html)
* [amazon web services - What does the dualstack prefix mean in AWS ELB - Stack Overflow](https://stackoverflow.com/questions/41623388/what-does-the-dualstack-prefix-mean-in-aws-elb)
* [Troubleshoot Your Application Load Balancers - Elastic Load Balancing](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-troubleshooting.html)
