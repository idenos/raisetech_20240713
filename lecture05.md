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

## ⑤. ALBでの設定と接続確認
- ALBの設定
![](./image_lec05/0010_alb.png)
- ブラウザにてALBのDNS名にアクセスしてRailsアプリケーションが表示できるか確認
![](./image_lec05/0011_alb_app.png)
## ⑥. S3の追加と設定
- Railsアプリで画像ファイルを追加する(aaaという名前で追加)
![](./image_lec05/0013_App_file_add_aaa.png)
- 画像ファイルの追加に成功
![](./image_lec05/0014_Fruit_file_aaa_add_success.png)
- aaaという名前の画像ファイルが追加されたことを確認
![](./image_lec05/0016_App_Home_aaa.png)
- Railsアプリで画像ファイル追加後にS3バケットを確認する
![](./image_lec05/0017_S3_bucket_aaa.png)
- Railsアプリで画像ファイルを削除する
![](./image_lec05/0018_App_del_aaa.png)
- ブラウザで削除した画像ファイルが無いことを確認
![](./image_lec05/0019_alb_app.png)
- Railsアプリで画像ファイルを削除後にS3バケットを確認する
![](./image_lec05/0020_S3_bucket_0.png)

## ⑦. 構造図
![](./image_lec05/lecture05_5.png)

## 今回の課題で学んだこと、感じたこと
今回の課題では、前回(4回)AWSのアカウントでEC2を作りましたが、アプリの動作で画像ファイルを保存したものを表示ができなかった点を修正する箇所で時間を費やしてしまいました。また課題に取り組んでいる最中にいろいろな出来事があり、一旦講座を聞くのみとなってしまい。4カ月以上も何も出来ない時期がありました。ALB設定はそれほど時間を費やすことはありませんでしたが、セキュリティーグループをEC2に紐づける設定など難易度が高く感じられました。AWSの構造図を記載では、矢印の作成に手間取りました。構成図作成にはテクニックや慣れが必要かと感じました。
