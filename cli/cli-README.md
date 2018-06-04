# AWS CLI

## 安裝 AWS CLI

***1. 安裝 python***

```shell
$ brew install python3
```

***2. 安裝 pip***

```shell
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ python3 get-pip.py
```

***3. 安裝 aws cli***

```shell
$ pip install awscli
```

***4 設定 AWS CLI A***

設定可以存取 AWS 的 Access Key ID 、 Secret Access Key 與區域，Key 可以從 IAM 個人帳號那邊去產生

```shell
$ aws configure

AWS Access Key ID [None]:
AWS Secret Access Key [None]:
Default region name [None]: ap-northeast-1
Default output format [None]:
```

## 參考資料
* [AWS 命令列界面](https://aws.amazon.com/tw/cli/)
* [Mac OSX 正確地同時安裝 Python 2.7 和 Python3 – 字串小豬](https://stringpiggy.hpd.io/mac-osx-python3-dual-install/)
* [Installation — pip 10.0.1 documentation](https://pip.pypa.io/en/stable/installing/)
