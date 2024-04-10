# R, Rstudioのインストール for windows 11


- このドキュメントは，Windows11 (22H2)で動作確認しました．
- 作成日：2023/04/13


## 始める前の注意

以下のドキュメントを注意深く読み，手順を守って実行すること．
誤った操作や手順で行った場合，PCが使えなくなる可能性がある．


# STEP 1: インストール前の準備

RとRstudioをインストールする前に，使っているPCのユーザアカウントを確認し，
必要であれば設定を変更する．

行うことは次の2点:
- STEP 1-1: ユーザフォルダの表示名の確認
- STEP 1-2: 管理者権限の確認


## STEP 1-1: ユーザフォルダ名の確認

1. ショートカットキー`WIN（ウインドウズキー）+ r`で`ファイル名を指定して実行`を開き，`cmd`と入力，OK押す
2. `C:\Users\`の後に表示されている文字に，全角文字（ひらがな・カタカナ・漢字・全角スペース）がないか確かめる．
    ![](./figs_win11/cmd.png?raw=true)
    - 全角文字が含まれていない場合 (例えば左図): 
        - 現在のアカウントをそのまま使用できる．STEP 1-2に進む．
    - 含まれている場合（例えば右図）: 
        - 現在のアカウントは使用できない．
        - [新規アカウントの作成](win11_add_account.md)を参照し，新規ユーザを作成する


> !!! 注意 !!!
>
> 既に作成済みのアカウントでユーザフォルダ名のみを変更しても，問題が生じる可能性が高い
> 新規にアカウントを作成すること


## STEP 1-2: 管理者権限の確認と変更

前提：授業で使用するユーザ（以降，ユーザAとする）でサインインしているものとする．

1. `Windowsマーク`を右クリック 
2. 設定
3. アカウント
4. ユーザの情報
    - この表示に，次のように「管理者」と書かれているか確認する．
    - 書かれてる: OK.
    - 書かれていない: 次の5以降を実行する
    ![](./figs_win11/open_settings.jpg?raw=true)
    ![](./figs_win11/open_settings_ms.png?raw=true)
5. 今使用しているユーザとは別に，管理者のユーザ（以降，ユーザBとする）があるはずなので，ユーザBでサインインする．
6. ユーザAについて，[アカウントの種類の変更] から [管理者] を選択し、[OK] を選択する．
    ![](./figs_win11/add_user5.png?raw=true)
7. PCを再起動する．
8. ユーザAでサインインし，上記4を確認する．


# STEP 2: Rのインストール

公式ページからインストーラをダウンロードして，インストール先を確認後，インストールしてください．

1. インストーラのダウンロード
    1. [r-project: R for Windows](https://cran.r-project.org/bin/windows/)を開く
    1. `base`からインストーラをダウンロード
1. インストーラ `R-バージョン番号.exe`を開く
    - バージョン番号はダウンロードのタイミングによって異なるので，各自で読み替えること
1. 下記のように選択＆確認しながら，インストーラの指示に従う
    1. 使用する言語:`日本語`
    1. 規約: 同意して次へ
    1. インストール先の指定が出たら，インストール先が
        `C:¥Program Files¥R¥R-バージョン番号`となっていることを確認する．
        - 問題無い場合は，インストール先を変更せずに次へ進む．
    1. 残りは全て`次へ`を選択する．
1. Rを起動し，R Consolが表示されることを確認する．
    - Winマーク -> 検索窓に`R 4.`と入力 -> 出てきた`R バージョン番号`を開く


### Rのインストール動画 (動画ではWindows10を使用しているが，やることは同じ)

[Youtube: RとRStudioのインストール](https://www.youtube.com/watch?v=hOq1HbtwKcs)
[![](https://img.youtube.com/vi/hOq1HbtwKcs/0.jpg)](https://www.youtube.com/watch?v=hOq1HbtwKcs)

> 補足
>
> 動画では，インストーラはC-learningのリンクから取得していますが，
> [r-project](https://cran.r-project.org/)から取得してください．



# STEP 3: RStudioのインストール

1. インストーラのダウンロード
    1. [rstudio.com](https://www.rstudio.com/products/rstudio/download/)を開く
    1. 「All Installers」からWindows10/11用のインストーラをダウンロードする
1. インストーラ `RStudio-バージョン番号.exe`を開く（バージョン番号はダウンロードのタイミングによって変わる）
1. 下記のように選択＆確認しながら，インストーラの指示に従う
    1. インストール先を選択する画面が出たら，インストール先が`C:¥Program Files¥RStudio`となっていることを確認する．
        - 問題無い場合は，インストール先を変更せずに次へ進む．
    1. 残りは全て`次へ`を選択する．
1. RStudioを起動し，ダイアログで出てきたら，次のように設定＆確認
    1. `Please select the version of R to use.`と表示されたら， `Use your machine's default 64-bit version of R`を選択
    1. `Enable automated crash reporting`と表示されたら，`はい`
    1. メニューバーのTools > Install Packages を開き，`Install to Library`の表示が，
    `C:/Users/ユーザ名/AppData/Local/R/win-library/バージョン番号`となっていることを確認する．
        - ユーザ名とバージョン番号は各自で異なるので，適宜読み替えること



### R studioのインストール動画 (動画ではWindows10を使用しているが，やることは同じ)

[Youtube: RとRStudioのインストール，03:29〜](https://www.youtube.com/watch?v=hOq1HbtwKcs&t=209s)
[![](https://img.youtube.com/vi/hOq1HbtwKcs/0.jpg)](https://www.youtube.com/watch?v=hOq1HbtwKcs&t=209s)

> 補足
>
> 動画では，インストーラはC-learningのリンクから取得していますが，
> [rstudio.com](https://www.rstudio.com/products/rstudio/download/)から取得してください．
> 新しいRStudioでは，表示等に変化がある場合があります．
