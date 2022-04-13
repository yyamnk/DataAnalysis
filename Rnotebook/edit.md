# Rnotebookの使い方


## 作成と変換

### 新規作成と保存

1. Rnotebookの新規作成
    - File -> New File -> R notebook
        ![](./figs/new_notebook.png?raw=true)
2. Rnotebookの保存
    - File -> Save As ...
    - 保存先は，作成した授業用のディレクトリ`DataAnalysis`の中とする．
    - ファイル名は，適当な名前，例えば`sample_nbook`とする．
    - エラーが生じる場合があるので，ファイル名に全角文字は含めないこと．
        ![](./figs/save_notebook.png?raw=true)

### Word変換

レポート課題はPDFで提出してください．
ここでは，Rnotebookから，Rnotebook -> Word -> PDFの順に変換してみましょう．

1. Rnotebookを開いている状態で，`Preview`とあるアイコンをクリック（2回目以降の人は，Kintと書いてある場合あり）
2. `Kint to word`を選択
    ![](./figs/convert1.png?raw=true)
3. 上手くいけば，Wordに変換されたRnotebookが表示される．
    - RStudio上のRnotebookと，Wordの変換結果を見比べて，正しく変換されているか確認する．
    ![](./figs/convert2.png?raw=true)

### PDF変換

Wordに変換できたら，PDFとして保存してください．

1. Wordのメニューバーより，`ファイル`
2. 名前を付けて保存
3. ファイルの種類を`PDF`として保存



## 編集

- タイトル・著者の変更
    - Rnotebookの文頭にある`title`, `author`を変更する

- 文字の入力
    - 通常のテキストは，単純に入力すれば良い
    - セクション見出し（太字）は，`# ` （シャープ + 半角スペース）を文頭につける
    ![](./figs/edit1.png?raw=true)

- コードの入力
    - 下図のとおり，RのコードChunkを挿入する
    ![](./figs/edit2.png?raw=true)

## Rnotebookの実行

- 各コードChunkの実行は，コードChunkにある再生ボタンを押す
    ![](./figs/edit3.png?raw=true)

- Rnotebookの全コードChunkを実行するときは，Run -> Run All を選択する．
    ![](./figs/edit4.png?raw=true)
