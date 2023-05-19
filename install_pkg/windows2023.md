# RStanのインストール for Windows

このガイドは，2023年5月19日に更新されました．
Windows11で確認しています．

参考：[github/Configuring C Toolchain for Windows](https://github.com/stan-dev/rstan/wiki/Configuring-C---Toolchain-for-Windows)


# STEP 1:ユーザ名とアカウント権限の確認

### for windows 10

次のリンク先にある，「インストール前の確認」をよく読み，問題ないことを確認してください．
誤ったユーザ名やアカウントを使った場合，RStanのインストールに失敗します．

- [for Windows10](https://github.com/yyamnk/DataAnalysis/blob/master/install/windows10.md#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E5%89%8D%E3%81%AE%E7%A2%BA%E8%AA%8D): 

### for windows 11

次の2点を確認してください．

- [R, RstudioのインストールのSTEP1-1](https://github.com/yyamnk/DataAnalysis/blob/master/install/windows11_2023.md#step-1-%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E5%89%8D%E3%81%AE%E6%BA%96%E5%82%99)を参照し，ユーザフォルダの表示名に，全角文字が含まれていないこと．
- [R, RstudioのインストールのSTEP1-2](https://github.com/yyamnk/DataAnalysis/blob/master/install/windows11_2023.md#step-1-2-%E7%AE%A1%E7%90%86%E8%80%85%E6%A8%A9%E9%99%90%E3%81%AE%E7%A2%BA%E8%AA%8D%E3%81%A8%E5%A4%89%E6%9B%B4)を参照し，管理者権限があること．


# STEP 2: パッケージのインストール先の確認

1. RStudioの右下にあるPackagesタブを開く
2. Installタブを開く
    ![](./win_step1.png?raw=true)
3. Install to Libraryを確認
    - `Install to Library`の表示が，`C:/Users/ユーザ名/AppData/Local/R/win-library/バージョン番号` となっていることを確認．
        - `ユーザ名`と`バージョン番号`は各自で異なるので，適宜読み替えること．
    ![](./win_step2.png?raw=true)


# STEP 3: Rtoolsをインストールする

1. 図のように，RStudioのコンソールに
    ```r
    R.version.string
    ```
    と打ち込み，使用しているRのバージョンを確認する．
    ![](check_Rversion.png)

- 使用しているのが，R4.3.xだった場合（xは任意）
    - [Rtools4.3の配布元ページ](https://cran.r-project.org/bin/windows/Rtools/rtools43/rtools.html)にアクセスし，`Rtools43 installer`のリンクからインストーラをダウンロードする．
        ![](./rtools43.png?raw=true)
    - ダウンロードしたインストーラ`rtools43-XXXX-XXXX.exe`を実行する．
    - 選択肢は全てデフォルトのまま，インストールする

- 使用しているのが，R4.2.xだった場合（xは任意）
    - [Rtools4.2の配布元ページ](https://cran.r-project.org/bin/windows/Rtools/rtools42/rtools.html)にアクセスし，`Rtools42 installer`のリンクからインストーラをダウンロードする．
        ![](./rtools42.png?raw=true)
    - ダウンロードしたインストーラ`rtools42-XXXX-XXXX.exe`を実行する．
    - 選択肢は全てデフォルトのまま，インストールする


# STEP 4: Rstanのパッケージをインストールする．

1. Rstudioのコンソールに，
    ```r
    install.packages("StanHeaders", repos = c("https://mc-stan.org/r-packages/", getOption("repos")))
    install.packages("rstan", repos = c("https://mc-stan.org/r-packages/", getOption("repos")))
    ```
    と打ち込み，インストールする．
2. コンソールに`library('rstan')`と打つ（下図の⑥）
3. このときPackagesタブのrstanにチェックが入ればインストールできている．
    ![](./win_step5.png?raw=true)
