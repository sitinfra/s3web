【Webサイト構築手順】

- TerraformでS3バケットを作成し、静的Webサイトホスティングを有効化
  ```
  tofu apply
  ```
- ローカルのWebサイトフォルダをS3にアップロード
  ```
  aws s3 cp ./mywebsite s3://sit-lxx-123456/ --recursive
  ```
- S3のWebサイトURLで公開
  ```
  http://sit-lxx-123456.s3-website-us-east-1.amazonaws.com/
  ```