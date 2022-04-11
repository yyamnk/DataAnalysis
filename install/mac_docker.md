# R, Rstudioのインストール for Mac

残念ながら，下記に記すMacの情報は，私のほうで確認できていません．（手元にMac環境がないので...）
昨年度に他コースで情報共有されていましたので，こちらに転記します．


# 概要

ここでは、Dockerを使ってデータ解析の授業に必要なRStudioの環境を整える方法を紹介します。
Dockerとは、OSを含むソフトウェア環境を任意のPCの上で実行できる仮想化プラットフォームです。

このたび、データ解析の授業用のDockerイメージを公開しました。
RStanなどのインストールが済んでいるので、学生はインストールで苦労する必要がなく、全員全く同じ環境を使うことができます。


# Dockerのインストール

インストールの手順は全て以下のページに書かれています。
https://docs.docker.jp/docker-for-mac/install.html

1. Docker Desktop for Macをダウンロードしてインストールします。
    - [このページ](https://hub.docker.com/editions/community/docker-ce-desktop-mac/)の "Get Docker Desktop for Mac (stable)" をクリックしてダウンロードし、
    - Docker.dmg をダブルクリックして開き、
    - Dockerのアイコンをアプリケーションフォルダのアイコンの上にドラッグ&ドロップしてインストールします。

2. アプリケーションフォルダの中のDockerをダブルクリックすると、Dockerが起動し、"Get started with Docker in a few easy steps!" という画面が現れます。"Skip tutorial" を押してください。次回からはログインすると自動で起動します。

3. Dockerが起動している時は、ステータスバーに鯨のアイコンが現れています。ここからダッシュボードを起動することができます。ダッシュボードを使うと、起動した仮想マシン(コンテナと呼ばれます)を確認したり終了したりできます。


# Docker上のRStanを実行

以下は、DockerをインストールしたPC上でデータ解析用のRStudioを動作させる方法です。

1. ターミナルを起動します。
    - ターミナルは、macOS の Finder の「移動」メニューの中にある「ユーティリティ」からアイコンを探してダブルクリックするか、
    - Launchpadの検索欄に「ターミナル」と入れて現れたアイコンを選ぶと起動できます。

2. `docker run -e PASSWORD=dataanalysis --rm -p 8787:8787 -v ${HOME}:/home/rstudio/localhome hirokisince1998/rstudio-srv-rstan` と入力します。
    - 最初に実行した時だけ、イメージのダウンロードに少し時間がかかります。イメージは 2.7GB あります。

3. "starting services" "done." と表示されたら準備完了です。
    - ブラウザを起動し、[http://localhost:8787/](http://localhost:8787/)を開きます。(リンクのクリックでもOK)
    - ユーザ名: `rstudio`
    - パスワード: `dataanalysis`

これで、ブラウザ上に RStudio の画面が現れます。後は、ふつうの RStudio と同じように使うことができます。
PC上のファイルを開きたい場合には、Files タブから localhome というディレクトリに入ってください。
