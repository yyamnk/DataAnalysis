# 新規アカウントの作成（Windows 11）

新規ユーザアカウントの作成は，2つの選択肢がある．

- [方法1（推奨）: Microsoftアカウントと連携したPCアカウントを作成する](win11_add_account.md#方法1)
- [方法2: ローカルアカウントを作成する](win11_add_account.md#方法2)


方法1を推奨するが，何らかの理由で困難な場合は方法2で作成すること．


# 方法1

Microsoftアカウントと連携したPCアカウントを作成する

1. `Windowsマークを右クリック -> 設定 -> アカウント -> 家族とその他のユーザ`を開く
    ![](./figs_win11/add_user1.png?raw=true)
2. `その他のユーザを追加`を選択
    ![](./figs_win11/add_user2.png?raw=true)
3. Microsoftアカウントの有無によって以下のいずれかを選ぶ
    - Microsoftアカウントを持っている場合，登録したメールアドレスを入力する
        ![](./figs_win11/add_user3_exist.png?raw=true)
    - Microsoftアカウントを持っていない場合，以下から新規登録する
        ![](./figs_win11/add_user3.png?raw=true)
4. 以降は指示に従って進める．
5. 新しいアカウントが作成ができたら，[アカウントの種類の変更] から [管理者] を選択し、[OK] を選択する．
    - ユーザ名は適宜読み替えること
    ![](./figs_win11/add_user5.png?raw=true)
6. サインアウトして，新規作成したアカウントでログインする


# 方法2

ローカルアカウントを作成する

[Microsoftサポート：Windows でローカルのユーザー アカウントまたは管理者アカウントを作成する](https://support.microsoft.com/ja-jp/windows/windows-でローカルのユーザー-アカウントまたは管理者アカウントを作成する-20de74e0-ac7f-3502-a866-32915af2a34d)
に従って，ローカルのユーザアカウントを作成する．

1. `Windowsマークを右クリック -> 設定 -> アカウント -> 家族とその他のユーザ`を開く
    ![](./figs_win11/add_user1.png?raw=true)
2. `その他のユーザを追加`を選択
    ![](./figs_win11/add_user2.png?raw=true)
3. `このユーザのサインイン情報がありません`を選択
    ![](./figs_win11/add_user3.png?raw=true)
4. `Microsoftアカウントを持たないユーザを追加する`を選択
5. `ユーザ名，パスワード，パスワードのヒント`を入力する．
    - このとき，ユーザ名に全角文字（ひらがな・カタカナ・漢字・全角スペース）を含めないこと！
    - 例えば`Ruser`はOK
    ![](./figs_win11/add_user4.png?raw=true)
6. 作成したアカウントについて，[アカウントの種類の変更] から [管理者] を選択し、[OK] を選択します。
    ![](./figs_win11/add_user5.png?raw=true)
7. サインアウトして，新規作成したアカウントでログインする
