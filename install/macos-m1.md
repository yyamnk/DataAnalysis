# R, RStudio, RStanのインストール for macOS (M1 Mac版)

このガイドは，2023年5月16日に作成されました．macOS 13.3 (Ventura) で確認しています．

# Rのインストール

1. [R for macOS](https://cran.r-project.org/bin/macosx/)を開き，Rの最新版のパッケージ (R 4.3.0 ならば R-4.3.0-arm64.pkg) をダウンロードする．
2. ダウンロードしたパッケージを開く．指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．
3. Rを起動し，Rコンソールが表示されることを確認する．


# RStudioのインストール

1. [rstudio.com](https://www.rstudio.com/products/rstudio/download/)を開き，「2. Install RStudio」の「DOWNLOAD RSTUDIO DESKTOP FOR MACOS 11+」を押してmacOS用のディスクイメージをダウンロードする．
2. ディスクイメージを開く．
3. RStudioのアイコンをApplicationsのアイコンの上までドラッグして離す．管理者の名前とパスワードを聞かれた場合には入力する．
4. RStudioを起動する．
5. コマンドライン・デベロッパツールをインストールするか聞かれた場合はインストールする．


# RStanのインストール

1. Xcodeをインストールする(Apple IDが必要)．macOS Ventura ならば App Store からインストールできる．そのほかの macOS の場合は https://developer.apple.com/download/all/?q=xcode から[互換性のあるバージョン](https://developer.apple.com/jp/support/xcode/) (例えば Monterey ならば Xcode 14.2) を選んでインストールする．インストールしたら一度起動しておく（ライセンスに同意が必要なため）．
2. まだコマンドライン・デベロッパツールをインストールしていない場合は，ターミナルを開き，以下のように入力してインストールする．

        xcode-select --install

2. ターミナルから以下のように入力する。

        mkdir .R ; echo "FLIBS = -L/usr/local/gfortran/lib -lgfortran" > .R/Makevars

3. [gfortran for macOS](https://github.com/fxcoudert/gfortran-for-macOS/releases)から適当な版を，例えば M1 の Mac で OS が Ventura ならば gfortran-ARM-12.2-Ventura.dmg を選んでダウンロードする．ディスクイメージを開く，パッケージ `gfortran.pkg` を開く．指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．

4. RStudioを起動する．
5. コンソールから以下のように入力する．

        install.packages(c("remotes", "Rcpp", "RcppArmadillo"))

6. コンソールから以下のように入力する．

        remotes::install_git("https://github.com/hsbadr/rstan", subdir = "StanHeaders", ref = "develop")

   「パッケージのソースからインストールを行いますか？」と聞かれた場合にはnoと入力する．

7. コンソールから以下のように入力する．

        remotes::install_git("https://github.com/hsbadr/rstan", subdir = "rstan/rstan", ref = "develop")


これで RStan がインストールできたので，RStudio のコンソールから `library(rstan)` と入力して RStan を読み込めることを確認する．
