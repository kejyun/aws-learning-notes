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

```shell
sudo apt-get install python-pip python-dev build-essential
sudo pip install --upgrade pip
sudo pip install --upgrade virtualenv
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

## 查詢 AWS CLI 版本

```shell
aws --version
aws-cli/1.15.80 Python/2.7.12 Linux/4.4.0-1061-aws botocore/1.10.79
```

## 更新 AWS CLI

```shell
pip install awscli --upgrade --user
```

## 解除安裝 AWS CLI

```shell
pip uninstall awscli
```

## 參考資料
* [AWS 命令列界面](https://aws.amazon.com/tw/cli/)
* [Mac OSX 正確地同時安裝 Python 2.7 和 Python3 – 字串小豬](https://stringpiggy.hpd.io/mac-osx-python3-dual-install/)
* [Installation — pip 10.0.1 documentation](https://pip.pypa.io/en/stable/installing/)
* [安装 AWS Command Line Interface - AWS Command Line Interface](https://docs.aws.amazon.com/zh_cn/cli/latest/userguide/installing.html)
