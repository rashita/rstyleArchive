---
title : ScrapScriptsを改造してみて思ったこと
link : 26290
date : Mon, 03 Dec 2018 03:10:16 +0000
categories : ["1-情報ツール考察"]
tags : ["scrapbox","scrapscripts","情報ツール","情報整理"]
draft : false
author : 倉下忠憲
---

Scrapbox用のブラウザ拡張にScrapScriptsがある。

<a href="https://scrapbox.io/daiiz/ScrapScripts">ScrapScripts - daiiz</a>

これを導入すると、リンクにホバーしただけで「関連ページ」を表示してくれたり、

<a href="https://gyazo.com/a7eb23eff8cd333bddf933f772158215"><video alt="Video from Gyazo" width="500" autoplay muted loop playsinline><source src="https://i.gyazo.com/a7eb23eff8cd333bddf933f772158215.mp4" type="video/mp4" /></video></a>

リンク先のページの中身を表示してくれたりする。

<a href="https://rashita.net/blog/?attachment_id=26291" rel="attachment wp-att-26291"><img src="https://rashita.net/blog/wp-content/uploads/2018/12/screenshot-1.png" alt="" width="645" height="561" class="alignnone size-full wp-image-26291" /></a>


これが、ときとばあいによっては、たいへん便利だ。

で、一つアイデアがあった。

■

Scrapboxでは、下に関連ページが表示されるが、それを「次々に」見ていきたいとき、若干もどかしさを感じる。リンクを踏めばいいだけなのだが、ページを移りたくない、という気持ちが湧いてくることがあるのだ。

それは新しくタブを開くのもなんとなくシャクだし、というようなよくわからない抵抗感があるのかもしれないし、ぜんぜん別の何かがあるのかもしれない。

ともかく、「そのページ」で関連ページの中身を閲覧したいと感じた。

そこで、ScrapScriptsを改造して、それを実現してみた。

ソースコードは以下で公開されているので、それに手を加える。

<a href="https://github.com/daiiz/ScrapScripts">daiiz/ScrapScripts: Unofficial browser extension for Scrapbox</a>

これをコピーし、「text-bubble.b.js」の中身を少しだけ書き換えた。具体的には、a.page-linkをli.page-list-itemに置き換え、keywordに放り込むものを、$a[0].innerTextから$a[0].innerText.split(/\r\n|\r|\n/)の[0]番目の要素に変えた。

で、そこからnpm run bulidとかいろいろやって、Chromeに放り込むことができた（なにせはじめて拡張をいじっているので、わからないことが多い）。

それを動かしたものが以下だ。

<a href="https://gyazo.com/1fb528f048de35de0bb3b08577eaff31"><video alt="Video from Gyazo" width="500" autoplay muted loop playsinline><source src="https://i.gyazo.com/1fb528f048de35de0bb3b08577eaff31.mp4" type="video/mp4" /></video></a>


あくまでプロトタイプとして作ったので、細かく気になる点はいくつかあるが（たとえば重なって読めない部分が出てくるなど）、それでも動作感は確認できた。

で、この動作は、一見楽しそうに思えるのだが、二つ大きな問題がある。

一つは、ページを「見るだけ」になってしまうこと。Scrapboxは閲覧したついでにちょこっと書き換えるというような細かいリファクタリングが肝になるのだが、この「閲覧方法」だと見るだけで、触れない。触るためにはリンクをクリックする必要があり、だったら初めからそうすればいいじゃん、ということになる。

が、その点は、簡易閲覧なのだからと割り切るとしても、もう一つの問題は、「そのページ」の本文が見えないことである。

私がやりたいのは、そのページの概念を中心として、その周辺の概念も巻き込みながら、何かを考えることである。が、関連ページは画面の下の方にあるし、新しく開くページの本文も下方向に表示される。結果、それらを綺麗に表示させると、そのページの本文は視野からまったく消えてしまう。

これはどう考えてもよろしくない、というか、あまり意味のない行為である。唯一効果があるとすれば、ハッシュタグ的に使っているページ、つまりページの本文がないページでの動作なのだが、それは今のコードの書き方だと不具合が多いので、どんな感触がするのかは確かめられていない。

■

とりあえず、上記のような感触から、私はこうして新しく開いたページを「移動」させたいと思った。マウスで摑み、ドラッグで移動させられる。そのような動作を欲した。そうすれば、重なりは気にならなくなるし、上の方にドラッグしていけば、本文と並べて表示もできる。

しかし、そうすれば本文周りはごちゃごちゃしてくるだろう。それに合わせてページのCSSも変える？　どんどん迷宮に嵌っていきそうだ。

これは単純に関連ページの本文を表示させるためのUIがまだ検討不足なのか、そもそも関連ページの本文を並べて表示させたいという欲求そのものが実際性を欠いているのか、そのどちらなのだろうか。少なくとも、私は情報カードのメタファーに引きずられ過ぎている可能性は否定できない。

それでも、と思うのだ。情報を並べて表示させたい欲求はそんなに間違ったものではないだろう、と。

というわけで、現状はvivaldiを使ってタブをタイリングするのが最適解であるという残念な結論にいたった。情報整理ツールの設計というのは、かくも難しいものなのである。

<strong>▼Scrapboxの入門書：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.12.03</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 5,003<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


