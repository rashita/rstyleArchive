---
title : 二冊目の電子書籍の製作手順（４）　〜zipとEPUBの行き来の注意点〜
link : 13533
date : Thu, 05 Jun 2014 04:44:33 +0000
categories : ["物書き生活と道具箱"]
tags : ["epub","でんでんコンバーター","ターミナル","電子書籍"]
draft : false
author : 倉下忠憲
---

前回まで：
<a href="https://rashita.net/blog/?p=13496" target="_blank">二冊目の電子書籍の製作手順（１）　〜EPUBファイル作りの大きな流れ〜</a>
<a href="https://rashita.net/blog/?p=13506" target="_blank">二冊目の電子書籍の製作手順（２）　〜Scrivener→「でんでんコンバーター」のちょっとしたコツ〜</a>
<a href="https://rashita.net/blog/?p=13520" target="_blank">二冊目の電子書籍の製作手順（３）　〜でんでんコンバーターを使う〜</a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg" alt="epubnised.003" width="500" class="alignnone size-full wp-image-13497" /></a>

前回はでんでんコンバーターを利用したEPUBファイルの作成法を紹介し、その中身を覗く方法も合わせて紹介しました。

今回は、そうして覗いたEPUBファイルの中身をいじるときの注意点です。

<H3>リライトは簡単</H3>

以下のページをご覧ください。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/20140605131130.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/20140605131130.png" alt="20140605131130" width="427" height="640" class="alignnone size-full wp-image-13536" /></a>

第一章の最初のページです。でんでんコンバーターは、本の扉ページを作ってはくれますが、こうした章ごとの扉ページまでは対応していません。

というわけで、私はEPUBファイルを解凍し、該当するxhtmlのページを書き換えることで上のような章扉ページを作成しました。ちなみに、デザインについてはでんでんコンバーターの扉ページのまるパクリです。

こういう対応を行うだけなら、解凍したEPUBをいじることにややこしい問題はありません。ただし、ファイルを追加した場合は、話は変わってきます。

<H3>ファイルの追加はややこしい</H3>

たとえば、デザインを変えるだけではなく、新規で章題ページを作ったとしましょう。既存のファイルをコピーして、hogehoge010.xhtmlみたいなファイルを作ったわけです。

それをそのまま放置しても、残念ながら「本」のページには組み込まれません。いくつかのファイルを更新する必要があります。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot6.png" alt="screenshot" width="400" height="546" class="alignnone size-full wp-image-13524" /></a>

上記のようなファイル構成であれば、

content.opf
nav.xhtml
toc.ncx

の３つがその対象です。

どのようにこれらのファイルを書き換えればよいのかの説明は長くなりますので、今回は割愛します。実際に上のファイルをテキストエディタで開ければ、おおよその当たりはつけられるでしょう。

もしこの辺の手順がまったくわからないなら、一度テキストファイルを作り直し、それをでんでんコンバーターに再アップすることをお勧めします。

<H3>圧縮時の注意点</H3>

さて、解凍したEPUBファイル（正確にはzipファイル）をいじり終えたとしましょう。あとは、これを圧縮して再びEPUBファイルに戻すだけです。

が、普通にフォルダを圧縮してもうまくはいきません。mimetypeが先頭かつ無圧縮な状態になっていないとEPUBファイルとしては機能しないのです＿＿と書いても意味がわかりませんね。大丈夫、心配しないでください。EPUB用にファイルを圧縮してくれるツールがあります。

<a href="https://code.google.com/p/epub-applescripts/downloads/detail?name=ePub%20Zip%20Unzip%202.0.1.app.zip&amp;can=2&amp;q=" target="_blank">ePub Zip/Unzip</a>

が、これを使わなくても、Macのターミナルからこの特殊な圧縮は可能です。

ターミナルを起動し、圧縮をかけたいフォルダにCDコマンドで移動した後、

zip -0 ../newbook.epub mimetype

を実行してから、

zip -r ../newbook.epub * -x mimetype

を実行すれば、「newbook.epub」というファイルが出来ているはずです。

簡単に解説すると、一行目に、無圧縮でmimetypeをnewbook.epubに置き、二行目でmimetypeを除くすべてのファイルを圧縮してnewbook.epubに置くコマンドです。他にも書き方はありますが、とりあえずこれで問題ないでしょう。

<H3>さいごに</H3>

以上のことが理解できていれば、何かしらのツールで作成したEPUBファイルを、自分なりにカスタマイズすることが可能になります。

もう一度、注意事項を振り返りましょう。

・ファイルを追加したらcontent.opf（nav.xhtml,toc.ncx）といったファイルを書き換える
・圧縮は、特別な方法で行う

この二つを押さえておけば大丈夫です。

次回は、作成した電子書籍のチェック方法を紹介してみます。

次：<a href="https://rashita.net/blog/?p=13540" target="_blank">二冊目の電子書籍の製作手順（５）　〜mobiとazwのプレビュー方法〜</a>
