# RStudioの設定

このページでは，授業で必要なRStudioの設定についてまとめます．
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
