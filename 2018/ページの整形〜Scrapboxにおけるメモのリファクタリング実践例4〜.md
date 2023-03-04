---
title : ページの整形〜Scrapboxにおけるメモのリファクタリング実践例4〜
link : 25882
date : Thu, 18 Oct 2018 00:00:27 +0000
categories : ["scrapboxの用法"]
tags : ["scrapboxリファクタリング","scrapbox","≪断片からの創造≫","「メモ」の研究","メモの育て方"]
draft : false
author : 倉下忠憲
---

昨日「<a href="https://rashita.net/blog/?p=25874">思考は転々とする</a>」という記事を書いたら、Twitterでコメントをもらえた。

<blockquote class="twitter-tweet" data-conversation="none" data-lang="ja"><p lang="ja" dir="ltr">ただこのページ、分割しようと思うとすげえ大変な気が（して、たぶん私はそのままにしてしまう）。<br>三分割と仮定して、①は②の具体例になっているし、②が③の前説明になっているし、③と①は対比関係にあるし……。</p>&mdash; いっき (@ikkiTime) <a href="https://twitter.com/ikkiTime/status/1052408139222540288?ref_src=twsrc%5Etfw">2018年10月17日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

嬉しい限りだ。何を隠そう、私は記事にコメントをもらえるのが三度のサンドイッチより大好きなのだ。

で、コメントの中身はまさにその通りだと思う。だから私も（手を付けずに）そのままにしておいたのだが、せっかくコメントを頂いたことだし、分割の青写真まで頂いたので、それに背中を押されて、<a href="https://scrapbox.io/rashitamemo/%E4%BD%8E%E4%BE%A1%E6%A0%BC%E8%B7%AF%E7%B7%9A%E3%81%AE%E5%B0%8F%E5%A3%B2%E6%A5%AD%E3%81%AE%E6%9C%80%E8%BF%91%E3%81%AE%E5%AE%A2%E5%8D%98%E4%BE%A1%E3%82%A2%E3%83%83%E3%83%97">このページの</a>リファクタリングを進めてみる。

<a href="https://rashita.net/blog/?attachment_id=25883" rel="attachment wp-att-25883"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-46.png" alt="" width="1097" height="784" class="alignnone size-full wp-image-25883" /></a>

まず、思いつきをたらたら書き出しただけなので、全体的に文章がタルい。これを締めていかなければならない。まずは、冒頭部分からだ。

<a href="https://rashita.net/blog/?attachment_id=25884" rel="attachment wp-att-25884"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-47.png" alt="" width="896" height="456" class="alignnone size-full wp-image-25884" /></a>

ある程度整形したのち、リンクを追加する。

<a href="https://rashita.net/blog/?attachment_id=25885" rel="attachment wp-att-25885"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-48.png" alt="" width="725" height="434" class="alignnone size-full wp-image-25885" /></a>

よし。とりあえずはこんなところだろう。ここでのポイントは、このブログのように「文章を書こう」などとは努々思わないことである。辞書的というか、プログラミングのコードを整形しているような気分で取りかかるのがいい（でないと文章をスリムにできない）。

で、次だ。

<a href="https://rashita.net/blog/?attachment_id=25886" rel="attachment wp-att-25886"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-49.png" alt="" width="878" height="490" class="alignnone size-full wp-image-25886" /></a>

自然と「なぜか？」というフレーズが出てきた。上と下を接続するための語句だ。でもって、この部分のうまいまとめかたはわからなかったので、とりあえず「所得の二極化」という部分だけをリンクにして、先に進むとする。あんまり考えすぎてもよろしくはない。

go to next block.

<a href="https://rashita.net/blog/?attachment_id=25887" rel="attachment wp-att-25887"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-50.png" alt="" width="1041" height="501" class="alignnone size-full wp-image-25887" /></a>

ここがやっかいだ。情報も多いし、入り組んでいる。

<a href="https://rashita.net/blog/?attachment_id=25888" rel="attachment wp-att-25888"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-51.png" alt="" width="1001" height="503" class="alignnone size-full wp-image-25888" /></a>

まず、ぱっと眺めて思ったのが、ブロック全体を何かの言葉で言い表したい、ということだった。そもそも、この情報は、このページの中身には直接関係はない。このページは「小売業」のことが書かれているべきである。異なる二つのものをまとめるためにページ全体の粒度を上げる必要はない。むしろ、この部分を切り出して、参考情報的に添えておくのがいいだろう。

切り出したページはこうなった。

<a href="https://rashita.net/blog/?attachment_id=25889" rel="attachment wp-att-25889"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-52.png" alt="" width="1002" height="753" class="alignnone size-full wp-image-25889" /></a>

元のページもずいぶんスッキリした。

<a href="https://rashita.net/blog/?attachment_id=25890" rel="attachment wp-att-25890"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-53.png" alt="" width="810" height="242" class="alignnone size-full wp-image-25890" /></a>

残るは、中央部分のブロックである。

どうも作ったリンクに違和感があったので、少しリンク名を変えてみた。

<a href="https://rashita.net/blog/?attachment_id=25891" rel="attachment wp-att-25891"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-54.png" alt="" width="786" height="297" class="alignnone size-full wp-image-25891" /></a>

そして、そのページを書き出す。

<a href="https://rashita.net/blog/?attachment_id=25892" rel="attachment wp-att-25892"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-55.png" alt="" width="996" height="541" class="alignnone size-full wp-image-25892" /></a>

これでだいたい落ち着いた。

<a href="https://rashita.net/blog/?attachment_id=25893" rel="attachment wp-att-25893"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-56.png" alt="" width="792" height="773" class="alignnone size-full wp-image-25893" /></a>

ついでに、別のところで作っておいたメモへのリンクを書き足しておく。

<a href="https://rashita.net/blog/?attachment_id=25894" rel="attachment wp-att-25894"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-57.png" alt="" width="939" height="753" class="alignnone size-full wp-image-25894" /></a>

うん、まあ、とりあえずはこれでいいだろう。

最初に書き出したものが、あまりにも大きかったので、まだリファクタリングしきれていない感じはある。が、あまり大きく考え過ぎると身動きが取れなくなる。これくらい分割できただけで、現状は良しとしておこう。新しいページもいくつか増えたことだし。

<strong>▼こんな記事も：</strong>

<a href="https://rashita.net/blog/?p=25700">ページの抽出〜Scrapboxにおけるメモのリファクタリング実践例3〜</a>
<a href="https://rashita.net/blog/?p=25525">知識をリンクでたぐり寄せる〜Scrapboxにおけるメモのリファクタリング実践例2〜</a>
<a href="https://rashita.net/blog/?p=25300">光る言葉をリンク化する　〜メモのリファクタリング実践例〜</a>

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.10.17</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 5,041<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

