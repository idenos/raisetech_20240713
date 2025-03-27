# 第6回目課題
## ①. 最後にAWSを利用した日の記録をCloudTrailのイベントから探し出す
- CloudTrailのイベント履歴から自身のIAMユーザで最後に利用したイベント(にS3バケットを削除した)を確認
  - イベント名：DeleteBucket
![](./image_lec06/0001_CloudTrail_DeleteBucket.png)<br><br>

## ②. CloudWatchアラームを使って、ALBのアラームを設定し、メール通知する
- CloudWatchアラームのALBアラームとアクションの設定
  - ALBのターゲットグループが「異常」を監視するアラームを設定
![](./image_lec06/0002_CloudWatch_Alarm.png)<br><br>
  - ALBのターゲットグループが「異常」であればアラートメールを送信するアクションをSNSに設定
![](./image_lec06/0003_CloudWatch_Alarm_Action.png)<br><br>
  - ALBのターゲットグループが「正常」に戻ったことを監視するアラームを設定
![](./image_lec06/0004_CloudWatch_Alarm_OK.png)<br><br>
  - ALBのターゲットグループが「正常」に戻ったことを知らせるアラートメールを送信するアクションをSNSに設定
![](./image_lec06/0005_CloudWatch_Alarm_OK_Action.png)<br><br>
- Railsアプリケーションを使えない状態にしてアラームが通知されるかを確認
  - nginxサービスを停止状態にする
![](./image_lec06/0008_raisetech001_nginx_stop.png)<br><br>
  - ALBでターゲットグループがヘルスチェックがUnhealthyを確認
![](./image_lec06/0009_raisetec001-alb-tg-raisetech001-Unhealthy.png)<br><br>
  - アラームメールの通知を確認
![](./image_lec06/0011_Alarm_Mail.png)<br><br>
  - nginxサービスをリスタートして稼働させる
![](./image_lec06/0012_raisetech001_nginx_start_status_OK.png)<br><br>
  - ALBでターゲットグループがヘルスチェックがHealthyに戻っていることを確認
![](./image_lec06/0013_raisetec001-alb-tg-raisetech001-Healthy.png)<br><br>
  - アラーム復旧メールの通知を確認
![](./image_lec06/0014_AlarmOK_Mail.png)

## ③. AWS利用料の見積を作成する
[AWS利用料の見積り]https://calculator.aws/#/estimate?id=ce776c078ee4e17b7cda0a1bfa7d95356bd19c28


## ④. 今月までのAWSの料金
- 現在 2025年3月18日時点での利用料
![](./image_lec06/0013_見積.png)<br><br>

- ECSの料金
![](./image_lec06/0015_EC2.png)<br><br>

- VPCの料金
![](./image_lec06/0014_VPC.png)<br><br>

## 考察
- 第5回の課題に時間がかかり、その間マシンを停止しなかったため無料分の750時間を超えてしまっているので、通常の費用がかかっています。またロードバランサ確認のためマシンを２台作成しています。
- VPCのパブリックIPアドレスの使用に費用が掛かることに気づいていませんでした。構築での予算配分などまだまだ勉強が必要と感じました。


