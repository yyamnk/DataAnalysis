# RStanのインストール for macOS

このガイドは，2022年4月9日に作成されました．macOS 12.1 (Monterey) で確認しています．

# RStanのインストール

1. App StoreからXcodeをインストールする．(Apple IDが必要)
2. まだコマンドライン・デベロッパツールをインストールしていない場合は，ターミナルを開き，以下のように入力してインストールする．
    ```sh
    xcode-select --install
    ```

3. [gfortran for Monterey Intel](https://github.com/fxcoudert/gfortran-for-macOS/releases/download/11.2-monterey-intel/gfortran-Intel-11.2-Monterey.dmg)をダウンロードし、ディスクイメージ `gfortran-Intel-11.2-Monterey.dmg`を開く．パッケージ `gfortran.pkg` を開く。指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．

    以上は macOS 12.1 (Monterey) の場合．これ以外の macOS を使っている場合は、 <https://github.com/fxcoudert/gfortran-for-macOS/> から適当な版を選んでインストールする．

3. RStudioを起動する．
4. コンソールから以下のように入力する．
    ```sh
    install.packages(c("remotes", "Rcpp", "RcppArmadillo"))
    ```

5. コンソールから以下のように入力する．
    ```sh
    remotes::install_git("https://github.com/hsbadr/rstan", subdir = "StanHeaders", ref = "develop")
    ```

   「パッケージのソースからインストールを行いますか？」と聞かれた場合にはnoと入力する．

6. コンソールから以下のように入力する．
    ```sh
    remotes::install_git("https://github.com/hsbadr/rstan", subdir = "rstan/rstan", ref = "develop")
    ```


これで RStan がインストールできたので、RStudio のコンソールから `library(rstan)` と入力して RStan を読み込めることを確認する．
