# R, RStudioのインストール for windows 10


以下の手順は2022年時点のものです．
現在の最新OSはWindows11となっており，Windows10のサポートはあと1-2年で終了します．

可能であれば，Windows11にアップデートしてから，
前ページにある手順書に従ってRとRStudioをインストールすることをおすすめします．



# インストール前の確認

RとRstudioをインストールする前に，使っているPCのユーザアカウントを確認し，必要であれば新しいアカウントを作成してください．

1. 現在のユーザ情報の確認
    - `Windowsマークを右クリック -> 設定 -> アカウント -> ユーザ情報`を開く 
        ![](./figs_win10/open_settings_edit.png?raw=true)
    - ユーザ名とアカウント種類を確認する
        - ユーザ名に，全角文字（ひらがな・カタカナ・漢字・全角スペース）は含まれていない
        - アカウントの種類が`ローカルアカウント`かつ`管理者`である
            - 両方`Yes`ならば，このアカウントを使ってRを実行できる．インストール前の確認は終えて，Rのインストールに進むこと．
            - どちらかでも`No`ならば，2に進む．
        ![](./figs_win10/user_info_edit.png?raw=true)

2. 新規ローカルアカウントの作成
    - [Microsoftサポート：Windows でローカルのユーザー アカウントまたは管理者アカウントを作成する](https://support.microsoft.com/ja-jp/windows/windows-でローカルのユーザー-アカウントまたは管理者アカウントを作成する-20de74e0-ac7f-3502-a866-32915af2a34d)に従って，ローカルのユーザアカウントを作成する．
    - 具体的には，
        - `Windowsマークを右クリック -> 設定 -> アカウント -> 家族とその他のユーザ`を開く
        - `その他のユーザをこのPCに追加`を選択
            ![](./figs_win10/add_user1.png?raw=true)
        - `このユーザのサインイン情報がありません`を選択
            ![](./figs_win10/add_user2.png?raw=true)
        - `Microsoftアカウントを持たないユーザを追加する`を選択
        - `ユーザ名，パスワード，パスワードのヒント`を入力する．
            - このとき，ユーザ名に全角文字（ひらがな・カタカナ・漢字・全角スペース）を含めないこと！
            - 例えば`Ruser`はOK
            ![](./figs_win10/input_new_user.png?raw=true)
        - 作成したアカウントについて，[アカウントの種類] から [管理者] を選択し、[OK] を選択します。
            ![](./figs_win10/change_to_admin.png?raw=true)
        - サインアウトして，新規作成したアカウントでログインする

> **!!! 注意 !!!**
> 
> 作成したアカウントでは，「OneDriveとの連携」や「Microsoftアカウントに切り替える」など
> Microsoft関連のクラウド連携は行わないこと．


### インストール前の確認の動画

[![](https://img.youtube.com/vi/uTb8WgAuOIY/0.jpg)](https://www.youtube.com/watch?v=uTb8WgAuOIY)



# Rのインストール

公式ページからインストーラをダウンロードして，インストール先を確認後，インストールしてください．

1. 必ず，前述の「インストール前の確認」を行うこと．
2. [r-project](https://cran.r-project.org/)を開き，「Download R for windows」からインストーラをダウンロードする．
3. インストーラ `R-バージョン番号.exe`を開く
    - バージョン番号はダウンロードのタイミングによって異なるので，各自で読み替えること
4. 使用する言語:`日本語`
4. `同意する`
5. インストール先の指定が出たら，インストール先が`C:¥Program Files¥R¥R-バージョン番号`となっていることを確認する．
    - 問題無い場合は，インストール先を変更せずに次へ進む．
    - 表示されたインストール先が`C:¥Program Files¥`の配下でない場合は，使用しているアカウントに問題がある可能性が高い．前述の「インストール前の確認」を再度確認すること．
6. 残りは全て`次へ`を選択する．
7. Rを起動し，R Consolが表示されることを確認する．


### Rのインストール動画

[Youtube: RとRStudioのインストール](https://www.youtube.com/watch?v=hOq1HbtwKcs)
[![](https://img.youtube.com/vi/hOq1HbtwKcs/0.jpg)](https://www.youtube.com/watch?v=hOq1HbtwKcs)

> 補足
>
> 動画では，インストーラはC-learningのリンクから取得していますが，
> [r-project](https://cran.r-project.org/)から取得してください．


# RStudioのインストール

公式ページからインストーラをダウンロードして，インストール先を確認後，インストールしてください．

1. 必ず，前述の「インストール前の確認」を行うこと．
2. [rstudio.com](https://www.rstudio.com/products/rstudio/download/)を開き，「All Installers」からWindows10/11用のインストーラをダウンロードする．
3. インストーラ `RStudio-バージョン番号.exe`を開く（バージョン番号はダウンロードのタイミングによって変わる）
5. インストール先を選択する画面が出たら，インストール先が`C:¥Program Files¥RStudio`となっていることを確認する．
    - 問題無い場合は，インストール先を変更せずに次へ進む．
    - 表示されたインストール先が`C:¥Program Files¥`の配下でない場合は，使用しているアカウントに問題がある可能性が高い．前述の「インストール前の確認」を再度確認すること．
6. 残りは全て`次へ`を選択する．
7. RStudioを起動する．
8. Packaseg > install を開き，`Install to Library`の表示が，
    `C:/Users/ユーザ名/AppData/Local/R/win-library/バージョン番号`となっていることを確認する．
        - ユーザ名とバージョン番号は各自で異なるので，適宜読み替えること
    - ユーザ名とバージョン番号は各自で異なるので，適宜読み替えること

### R studioのインストール動画

[Youtube: RとRStudioのインストール，03:29〜](https://www.youtube.com/watch?v=hOq1HbtwKcs&t=209s)
[![](https://img.youtube.com/vi/hOq1HbtwKcs/0.jpg)](https://www.youtube.com/watch?v=hOq1HbtwKcs&t=209s)


> 補足
>
> 動画では，インストーラはC-learningのリンクから取得していますが，
> [rstudio.com](https://www.rstudio.com/products/rstudio/download/)から取得してください．
