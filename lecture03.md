# サンプルアプリケーションの起動

## ①. サンプルアプリケーションの入手
![サンプルアプリケーション](./image/0006_raisetech-live8-sample-app.png)
## ②. 添付されている README.md の理解
![README.mdの理解](./image/0005_README.md.png)
## ③. デプロイ作業
![mysqlの起動確認](./image/0007_mysqld_install_script_ato.png)
## ⑤. Webブラウザでの起動確認
![New fruit1](./image/0001_New_fruit.png)
![New fruit2](./image/0002_New_fruit.png)
![New fruit3](./image/0003_New_fruit.png)
![Listing fruit](./image/0004_Listing_fruit.png)

## 1. APサーバについて調べる
### ・APサーバの名前とバージョンの確認
RailsのAPサーバはPumaです。バージョンは 6.4.2です。
![APサーバの名前とバージョン確認](./image/0010_pume-version.png)

### ・APサーバを終了させた場合、引き続きアクセス可能か
APサーバを終了させた場合は、APにアクセスできません
![APサーバを終了](./image/0011_puma-kill.png)
![APサーバ終了後](./image/0012_Oops.png)

## 2. DBサーバについて調べる

### . サンプルアプリケーションを使ったDBサーバ(DBエンジン)の名前と、今Cloud9で動作しているバージョンの確認
DBエンジン名：mysql  DBエンジンのバージョン：8.4.2
![DBエンジン名とDBエンジンのバージョン](./image/0015_mysql-version.png)

### ・DBサーバを終了させた場合、引き続きアクセス可能か
DBサーバを終了させた場合は、DBサーバからのエラーメッセージが表示されるので、APにアクセスできません。
以下のコマンドを投入してDBサービスを停止
sudo systemctl stop mysqld
![DBサーバ終了後の表示](./image/0014_mysqld_stop.png)

### ・Railsの構成管理ツールの名前
Railsの構成管理ツールの名前はBundlerです。gemのバージョンやgemの依存関係を管理が可能。bundlerを使うことで、gemのバージョンを一致させることができます。複数人の開発環境であった場合に、同じgemに統一したり、開発するシステムに合わせてgemのバージョンを切り替える、といったことが可能です。

## 3. 今回の課題で学んだこと、感じたこと
・課題の作成にかなり時間をかけてしまいました。2週間程度の日数を費やしています。
・APサーバについて調べるでは、APサーバを停止させるという課題で、プロセスを停止することをなかなか思いつかなくて時間がかかってしまいました。
・Markdownの画像埋め込み方法とgithubにアップデートする順番などに時間を費やしてしまいました。
・仕事と同じように納期があることを意識し、調べる時間に制限をつけてなるべく早く課題を終了させる、質問をするように心がけたいと思います。