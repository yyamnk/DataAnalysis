# proxy環境下でRStudioにパッケージをインストールする方法

[Rのパッケージインストール時のプロキシ設定](https://qiita.com/ch7821/items/9f526985c8ff1b90e426)
を参考に設定する．


```sh
# RStudioのコンソールで
$ file.edit('~/.Rprofile')
```

エディタが開いたら，以下を追記して保存＆閉じる

```sh
options(download.file.method = "libcurl")
```

```sh
# RStudioのコンソールで
$ file.edit('~/.Renviron')
```

エディタが開いたら，以下を追記して保存＆閉じる

```sh
http_proxy="http://proxy.cc.utsunomiya-u.ac.jp:8080"
https_proxy="http://proxy.cc.utsunomiya-u.ac.jp:8080"
```

RStudio再起動
