# 第5回目課題
## ①. 組み込みサーバ（Puma）でのRailsアプリケーション動作確認  
- PumaサービスのCLIコマンドでの確認
![](./image_lec05/0001_Puma.service_cmd.png)<br><br>
- PumaサービスのWebブラウザでの動作確認
![](./image_lec05/0002_Puma.service_3000.png)

## ②. 組込みサーバとUnix Socketを使ったRailsアプリの動作確認
- 組込みサーバとUnix Socketを使ったRailsアプリのCLIコマンドでの確認
![](./image_lec05/0003_Puma_service_Unix_socket_cmd.png)<br><br>
- PumaサービスをUnix Socketにcurlにてリクエストを送信
![](./image_lec05/0004_Puma_service_Unix_socket_cmd.png)

## ③. Nginxの単体起動確認
- Nginxサービスの単体での起動をWebブラウザで確認
![](./image_lec05/0005_Nginx.service_80.png)<br><br>
- NginxサービスCLIコマンドでの確認
![](./image_lec05/0007_Nginx_service_80_cmd.png)

## ④. Nginxと組込みサーバ、Unix Socketを組み合わせてのRailsアプリケーション動作確認
- Nginxと組込みサーバ、Unix Socketを組み合わせてのRailsアプリケーションをブラウザで確認
![](./image_lec05/0008_Nginx_service_80.png)<br><br>
- Nginxと組込みサーバ、Unix Socketを組み合わせてのRailsアプリケーションをCILコマンドで確認
![](./image_lec05/0009_Nginx_service_80_cmd.png)<br><br>

![TeraTerm5でのSSH接続](./image_lec4/0012_EC2_login.png)
## ⑤. ALBでの設定と接続確認
![EC2からRDSへの接続](./image_lec4/0013_RDS_login.png)
## ⑥. EC2のセキュリティルール
![EC2のセキュリティールール](./image_lec4/0015_EC2_Security.png)
## ⑦. RDSのセキュリティールール
![RDSのセキュリティールール](./image_lec4/0017_RDS_Security_rule.png)

## 今回の課題で学んだこと、感じたこと
VPCの作成については、既存のVPCにサブネットの設定をしてしまい、EC2の作成とRDSの作成を含め約1カ月以上時間を費やすことになりました。AWSの無料期間が過ぎてしまったので、新しく家族の枠でAWSのアカウントを作成しました。以降の課題もこちらで行います。
今回の課題で作成したEC2でgithubに課題の画像などをPushしております。以降もこのEC2で行うようにします。
サブネットやセキュリティーグループ、ゲートウェイの設定などネットワーク設定で時間を費やすことになりましたが、自身で調べて納得しているので今後役に立つと思っています。