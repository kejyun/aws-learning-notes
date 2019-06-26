# S3 CLI

## 複製本機檔案至 S3

```
aws s3 cp "本機檔案路徑" "S3 目錄路徑"
```

```
aws s3 cp /home/kejyun/web.tar.gz s3://kj-bucket-name/my/folder/
```

## 複製 S3 檔案至本機

```
aws s3 cp "S3 檔案路徑" "本機目錄"
```

```
aws s3 cp s3://kj-bucket-name/my/folder/web.tar.gz /home/kejyun/
```



## 參考資料
* [如何以指令碼將檔案備份到 Amazon S3 – AWS](https://aws.amazon.com/tw/getting-started/tutorials/backup-to-s3-cli/)
