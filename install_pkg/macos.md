# RStanのインストール for macOS

このガイドは，2024年5月21日に作成されました．macOS 13.3 (Ventura) で確認しています．

## インストール

[RStan Getting Started](https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started) の説明を基に，手順を簡単にまとめました．

以下の手順は，電源に接続した状態，かつ安定したネット環境で実行することをおすすめします．

1. RStudioを起動する．
2. コンソールから以下のように入力する．コマンドライン・デベロッパツールをインストールするか聞かれた場合は「インストール」を選ぶ．
    ```sh
    install.packages("remotes")
    remotes::install_github("coatless-mac/macrtools")
    ```
3. コンソールから以下のように入力する．パスワードを聞かれるので入力すると RTools のインストールが始まる．これには15分程度を要する．
    ```sh
    macrtools::macos_rtools_install()
    ```
    成功すれば，"Congratulations! Xcode CLI, Gfortran, and R developer binaries have been installed successfully." と表示される．
4. コンソールから以下のように入力する．
    ```sh
    install.packages("rstan", repos = "https://cloud.r-project.org/", dependencies = TRUE)
    ```
これで RStan がインストールできた．

## テスト
コンソールから以下のように入力する．
```r
library(rstan)
(stan(model_code="parameters {real p;} model {p~normal(0,1);}"))
```
実行に時間がかかるので，しばらく待つ．

正常に完了すると，以下のように表示されるはず．これが表示されればRStanは正常にインストールできている．

![](./win_step5-2.png?raw=true)
