# VTマニュアル

本マニュアルは *Gitbook* によって書かれています。

## Gitbookのインストール  
npmを使うのが一番簡単
~~~
npm install gitbook-cli -g
~~~

## オンライン閲覧  
このディレクトリ(VT_Manual/)にて、Gitbookのローカルサーバを起動。ブラウザにて、 *localhost:4000* に接続する。  
機種ごとの違いは環境変数を指定して起動する。例えばMotomanであれば
~~~
Motoman=true gitbook serve
~~~

## PDF化  
PDFにするには[Calibre](https://calibre-ebook.com/)をインストールする必要があります。
以下にてPDFファイルが生成されます。
~~~
gitbook pdf
~~~
