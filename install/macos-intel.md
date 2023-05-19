# R, RStudio, RStanのインストール for macOS (Intel Mac版)

このガイドは，2023年5月16日に作成されました．macOS 12.6 (Monterey) で確認しています．

# Rのインストール

1. 最新版のRだと2023年5月16日現在[RStanのインストール](#RStanのインストール)に問題があるので，最新版ではなく [R for macOS](https://cran.r-project.org/bin/macosx/) にある R-4.2.3.pkg をダウンロードする．
2. パッケージ `R-4.2.3.pkg` を開く．指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．
3. Rを起動し，Rコンソールが表示されることを確認する．


# RStudioのインストール

1. [rstudio.com](https://www.rstudio.com/products/rstudio/download/)を開き，「All Installers and Tarballs」からmacOS用のディスクイメージをダウンロードする．
2. ディスクイメージを開く．
3. RStudioのアイコンをApplicationsのアイコンの上までドラッグして離す．管理者の名前とパスワードを聞かれた場合には入力する．
4. RStudioを起動する．
5. コマンドライン・デベロッパツールをインストールするか聞かれた場合はインストールする．




# RStanのインストール

1. Xcodeをインストールする(Apple IDが必要)．macOS Ventura ならば App Store からインストールできる．そのほかの macOS の場合は https://developer.apple.com/download/all/?q=xcode から[互換性のあるバージョン](https://developer.apple.com/jp/support/xcode/) (例えば Monterey ならば Xcode 14.2) を選んでインストールする．インストールしたら一度起動しておく（ライセンスに同意が必要なため）．
2. まだコマンドライン・デベロッパツールをインストールしていない場合は，ターミナルを開き，以下のように入力してインストールする．

        xcode-select --install

3. [gfortran for macOS](https://github.com/fxcoudert/gfortran-for-macOS/releases)から適当な版を，例えば Intel の Mac で OS が Monterey ならば gfortran-Intel-12.1-Monterey.dmg を選んでダウンロードする．ディスクイメージを開く，パッケージ `gfortran.pkg` を開く．指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．

4. RStudioを起動する．
5. コンソールから以下のように入力する．

        install.packages(c("remotes", "Rcpp", "RcppArmadillo"))

6. コンソールから以下のように入力する．

        remotes::install_git("https://github.com/hsbadr/rstan", subdir = "StanHeaders", ref = "develop")

   「パッケージのソースからインストールを行いますか？」と聞かれた場合にはnoと入力する．

7. コンソールから以下のように入力する．

        remotes::install_git("https://github.com/hsbadr/rstan", subdir = "rstan/rstan", ref = "develop")


これで RStan がインストールできたので，RStudio のコンソールから `library(rstan)` と入力して RStan を読み込めることを確認する．
