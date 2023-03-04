---
title : ページの抽出〜Scrapboxにおけるメモのリファクタリング実践例3〜
link : 25700
date : Thu, 27 Sep 2018 02:26:47 +0000
categories : ["scrapboxの用法"]
tags : ["scrapboxリファクタリング","scrapbox"]
draft : false
author : 倉下忠憲
---

先日ふと、「ゲームプレイヤーにもいろいろあるな」と思いついた。

たとえば、取扱説明書をプレイする前にしっかり読む人と、とりあえず始めてみて困ってから取説を参照する人、という最低二つのタイプは想定できるだろう。で、それぞれのプレイヤー向けに「最適」な情報提供の形は違うな、と思ったわけである。

それをScrapboxのページに書いていたら、そういえば、こんな分類もあるぞ、というのがいくつか出てきた。で、それも合わせて書いておいた。

<a href="https://rashita.net/blog/?attachment_id=25702" rel="attachment wp-att-25702"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-49.png" alt="" width="797" height="693" class="alignnone size-full wp-image-25702" /></a>

情報としては間違ってはいない。ここに含まれているのは、たしかに「ゲームプレイヤーにもいろいろある」という話である。しかし、どうもまぜこぜになっている感覚はある。文字数は少ないが、情報の幕の内弁当感が出てしまっている。

そこで、切り出しだ。

まず、一番上から取りかかる。見出しになるものを考えて、それを追加した。

<a href="https://rashita.net/blog/?attachment_id=25703" rel="attachment wp-att-25703"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-50.png" alt="" width="763" height="556" class="alignnone size-full wp-image-25703" /></a>

さらにそのブロックを選択して、New page機能で切り出す。

<a href="https://rashita.net/blog/?attachment_id=25704" rel="attachment wp-att-25704"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-51.png" alt="" width="787" height="414" class="alignnone size-full wp-image-25704" /></a>

とりあえず、これはまあこれでいいだろう。もとのページに戻ってみる。

<a href="https://rashita.net/blog/?attachment_id=25706" rel="attachment wp-att-25706"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-52.png" alt="" width="603" height="579" class="alignnone size-full wp-image-25706" /></a>

「万人向けのうんぬん」の扱いが不明瞭だが、決めきれないのでそのままにして先に進む。「デッキの作り方」はそのまま切り出せそうだ。

<a href="https://rashita.net/blog/?attachment_id=25707" rel="attachment wp-att-25707"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-53.png" alt="" width="817" height="423" class="alignnone size-full wp-image-25707" /></a>

ついでに細かい情報もつけ足しておいた。もとのページに戻る。

<a href="https://rashita.net/blog/?attachment_id=25708" rel="attachment wp-att-25708"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-54.png" alt="" width="631" height="540" class="alignnone size-full wp-image-25708" /></a>

最後の段落が一番ごちゃっとしている。少し考えて、冒頭を行にバラすことにした。

<a href="https://rashita.net/blog/?attachment_id=25709" rel="attachment wp-att-25709"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-55.png" alt="" width="601" height="327" class="alignnone size-full wp-image-25709" /></a>

そして、二行目移行をNew pageで切り出す。

<a href="https://rashita.net/blog/?attachment_id=25710" rel="attachment wp-att-25710"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-56.png" alt="" width="1058" height="730" class="alignnone size-full wp-image-25710" /></a>

かなり説明を追加しておいた。さすがにこれをもとのページで展開するのは大きすぎる。たとえば、最初のページに[サイコグラフィック]というページリンクがあっても、ページの粒度が大きすぎるので、関係性が見えづらいだろう。やはり切り分けが大切である。

というわけで、もとのページはこうなった。

<a href="https://rashita.net/blog/?attachment_id=25711" rel="attachment wp-att-25711"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-57.png" alt="" width="696" height="545" class="alignnone size-full wp-image-25711" /></a>

こうなると、さらに整えられるようになる。

<a href="https://rashita.net/blog/?attachment_id=25714" rel="attachment wp-att-25714"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-59.png" alt="" width="741" height="499" class="alignnone size-full wp-image-25714" /></a>

「いろいろある」のその「いろいろ」を少し上の観点から整理できた。

となると、タイトルも変えたくなるが、最初に私は「ゲームプレイヤーにもいろいろある」と思いついたので、そのままがいいかもしれない。あるいは、「多様性」というキーワードが脳内で思い出されるかもしれない。そこで、「あるいは、」のバージョンのタイトルも書き加えておく。

<a href="https://rashita.net/blog/?attachment_id=25713" rel="attachment wp-att-25713"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-58.png" alt="" width="755" height="549" class="alignnone size-full wp-image-25713" /></a>

うむ。これでずいぶんと整理ができた。こうしておけば、「どんな風にゲームにトライするのか？」というので別項目を思いついても、新しく付け加えていける。その数がさらに膨らむなら、それを１つのページとして切り出してもいいだろう。

が、今のところ、私の脳内ではそこまで大きな概念にはなっていないので、この状態で良しとしておく。

<strong>▼その他記事：</strong>
<a href="https://rashita.net/blog/?p=25300">光る言葉をリンク化する　〜メモのリファクタリング実践例〜 – R-style</a>
<a href="https://rashita.net/blog/?p=25525">知識をリンクでたぐり寄せる〜Scrapboxにおけるメモのリファクタリング実践例2〜 – R-style</a>

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.09.27</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 3,968<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

