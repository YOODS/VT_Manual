# VTマニュアル

本マニュアルは *Gitbook* によって書かれています。

## Gitbookのインストール  
npmを使うのが一番簡単
~~~
npm install gitbook-cli -g
~~~

## オンライン閲覧  
このディレクトリ(VT_Manual/)にて、Gitbookのローカルサーバを起動
~~~
gitbook serve
~~~
ブラウザにて、 *localhost:4000* に接続する。

## PDF化  
PDFにするには[Calibre](https://calibre-ebook.com/)をインストールする必要があります。
以下にてPDFファイルが生成されます。
~~~
gitbook pdf
~~~
