# RStanのインストール for Windows

このガイドは，2022年5月20日に作成されました．
Windows11で確認しています．

# インストール前の確認

次のリンク先にある，「インストール前の確認」をよく読み，問題ないことを確認してください．
誤ったユーザ名やアカウントを使った場合，RStanのインストールに失敗します．

- [for Windows10](https://github.com/yyamnk/DataAnalysis/blob/master/install/windows10.md#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E5%89%8D%E3%81%AE%E7%A2%BA%E8%AA%8D): 
- [for Windows11](https://github.com/yyamnk/DataAnalysis/blob/master/install/windows11.md#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E5%89%8D%E3%81%AE%E7%A2%BA%E8%AA%8D) 


# RStanのインストール

ここではR4.1.3を例にインストールを進めます．

1. RStudioの右下にあるPackagesタブを開く
2. Installタブを開く
    ![](./win_step1.png?raw=true)
3. Install to Libraryを確認
    - `Install to Library`の表示が，
        - R4.2.xの場合: `C:/Users/ユーザ名/AppData/Local/R/win-library/バージョン番号` 
        - R4.1.xの場合: `C:/Users/ユーザ名/Documents/R/win-library/バージョン番号`
        - `ユーザ名`と`バージョン番号`は各自で異なるので，適宜読み替えること．
    ![](./win_step2.png?raw=true)
4. インストール先に問題が無ければ，Packagesに「rstan」と入力し，Install
5. 次のような警告（Rtoolsが必要だが，インストールされていない）が出た場合，Rtoolsをインストールする．
    - まず，使用しているRのバージョンを確認して，適切なRtoolsのインストーラを入手する必要がある．RのバージョンはConsoleに表示されている．
    ![](./win_step3.png?raw=true)
    - [Rtoolsインストーラへのリンク](https://cran.r-project.org/bin/windows/Rtools/)から，使用しているRのバージョンに一致したインストーラをダウンロードする．
    ![](./win_step4.png?raw=true)
    - ダウンロードしたら，インストーラを起動し，全てデフォルト（変更せずにNextを押す）で進める．
    - Rtoolsがインストーラできたら，一度Rstudioを閉じ（Rstudioの再起動），再び手順4を行う．
6. Consoleに`library('rstan')`と打つ．このときPackagesタブのrstanにチェックが入ればインストールできている．
    ![](./win_step5.png?raw=true)


# RStanのインストール動画 (この動画にはRtoolsのインストールは含まれていません）

[Youtube: パッケージのインストール](https://youtu.be/JyKWeQMp5F4)
[![](https://img.youtube.com/vi/JyKWeQMp5F4/0.jpg)](https://www.youtube.com/watch?v=JyKWeQMp5F4)


# 上記の方法でインストールできない場合

何らかの原因で上記の方法ではインストールできない報告がある．
その場合は，Rstudioのコンソールに次のコマンドを入力し，ソースからインストールする．

```R
remove.packages(c("StanHeaders", "rstan"))
install.packages("StanHeaders", repos = c("https://mc-stan.org/r-packages/", getOption("repos")))
install.packages("rstan", repos = c("https://mc-stan.org/r-packages/", getOption("repos")))
```

