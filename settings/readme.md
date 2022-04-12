# RStudioの設定

このページでは，授業で必要なRStudio等の設定についてまとめます．
複数の項目がありますが，次の2つに大別されています．
- （must）: 必ず設定してください
- （optional）: 必ずしも設定する必要はありませんが，あると便利です


## スタートメニューに追加する (optional, for windows)

RStudioの起動をショートカットする設定です．

1. スタート(Windowsマーク)
2. 検索窓に`rstudio`と入力
3. 検索結果のRStudioを右クリック
4. スタートにピン留するを選択
    ![](./figs/add_start_menu.png?raw=true)
5. 以後，スタートメニューにRStudioのショートカットが登録される
    ![](./figs/add_start_menu_result.png?raw=true)


## RStudioのテキストエンコーディング設定（must, for all OS）

C-Learningからダウンロードした授業のスクリプトを開くために必須です．

1. RStudioのToolsメニューを開く
2. Global Options
    ![](./figs/encoding1.png?raw=true)
3. Code
4. Saving
5. Default text encoding の`Change`
    ![](./figs/encoding2.png?raw=true)
6. `UTF-8` を選択
    ![](./figs/encoding3.png?raw=true)
7. Default text encodingが`UTF-8`になっていることを確認
8. Apply
    ![](./figs/encoding4.png?raw=true)


## ファイル拡張子の表示（must, for windows）

Windowsでは，デフォルトでファイルの拡張子が表示されません．
これでは不便なので，拡張子を表示するように変更します．

- for Wisdows 11
    1. Explorerを開く
    2. 表示
    3. 表示
    4. ファイル名拡張子にチェック
        ![](./figs/explorer_win11.png?raw=true)

- for Wisdows 10
    1. Explorerを開く
    2. 表示
    3. ファイル名拡張子にチェック
        ![](./figs/explorer_win10.png?raw=true)

