# R, Rstudioのインストール for windows 10


## インストール前の確認

RとRstudioをインストールする前に，使っているPCのユーザアカウントを確認し，必要であれば新しいアカウントを作成してください．

[Youtube:【Rインストール前にやること】ユーザ情報の確認](https://www.youtube.com/watch?v=uTb8WgAuOIY)

1. 現在のユーザ情報の確認
    - `Windowsマークを右クリック -> 設定 -> アカウント -> ユーザ情報`を開く 
        ![](./figs_win10/open_settings_edit.png?raw=true)
    - ユーザ名に，全角文字（ひらがな・カタカナ・漢字・全角スペース）が含まれていないかを確認する．含まれる場合は，2に進む．
    - アカウントの種類が`ローカルアカウント`かつ`管理者`であることを確認する．そうでない場合は，2に進む．
        ![](./figs_win10/user_info_edit.png?raw=true)
2. 新規ローカルアカウントの作成
    - [Microsoftサポート：Windows でローカルのユーザー アカウントまたは管理者アカウントを作成する](https://support.microsoft.com/ja-jp/windows/windows-でローカルのユーザー-アカウントまたは管理者アカウントを作成する-20de74e0-ac7f-3502-a866-32915af2a34d)に従って，ローカルのユーザアカウントを作成します．
    - 具体的には，
        - [ここから設定画面を開く](ms-settings:otherusers)か，自分で`Windowsマークを右クリック -> 設定 -> アカウント -> 家族とその他のユーザ`を開く
        - `その他のユーザをこのPCに追加`を選択
            ![](./figs_win10/add_user1.png?raw=true)
        - `このユーザのサインイン情報がありません`を選択
            ![](./figs_win10/add_user2.png?raw=true)
        - `Microsoftアカウントを持たないユーザを追加する`を選択
        - `ユーザ名，パスワード，パスワードのヒント`を入力する．
            - このとき，ユーザ名に全角文字（ひらがな・カタカナ・漢字・全角スペース）を含めないこと！
            - 例えば`Ruser`はOK
            ![](./figs_win10/input_new_user.png?raw=true)

