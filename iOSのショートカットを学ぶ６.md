---
title : iOSのショートカットを学ぶ６
link : 28584
date : Fri, 14 Jun 2019 22:00:02 +0000
categories : ["プログラミング"]
tags : ["ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=28561">iOSのショートカットを学ぶ５</a>

さて、さっとメモを送るだけの「FastEverもどき」はできた。ただし、ノートのタイトルが本文すべてになっている。これをなんとかしたい。

今回はその改造をやってみよう。
<h2>流れ</h2>
まず、イメージする。やりたいのは、入力したテキストの一行目だけを取り出すことだ。どうすればいいか。

そこでいったん検索ボックスに「テキスト」と入れてみる。

<a href="https://rashita.net/blog/?attachment_id=28585" rel="attachment wp-att-28585"><img class="alignnone size-full wp-image-28585" src="https://rashita.net/blog/wp-content/uploads/2019/06/C087A7B9-D549-4530-BC10-AA402015F292.jpg" alt="" width="320" height="568" /></a>

すると「テキストを分割」と「テキストを置き換える」が目に入った。テキストを行単位で分割できれば光明が差しそうだし、あるいは一行目以降をすべて消してしまう、というような置き換え（置換）ができれば、それでも目的は達成できそうだ。

両方道筋はありそうだが、とりあえずは「テキストを分割」を軸に進めてみよう。それが行き止まりだったら、今度は置換で考えればいい。
<h2>サンプル</h2>
まず、簡単にやってみる。

<a href="https://rashita.net/blog/?attachment_id=28586" rel="attachment wp-att-28586"><img class="alignnone size-full wp-image-28586" src="https://rashita.net/blog/wp-content/uploads/2019/06/2F5EF987-B750-432E-813A-C7CF7471EBD5.jpg" alt="" width="320" height="568" /></a>

最初に「入力を要求」を設置し、その次に「テキストを分割」を置く。そして、実行ボタン。

<a href="https://rashita.net/blog/?attachment_id=28587" rel="attachment wp-att-28587"><img class="alignnone size-full wp-image-28587" src="https://rashita.net/blog/wp-content/uploads/2019/06/2705EE17-CAC3-4D0B-B40D-8DFC2EDDA2A2.jpg" alt="" width="320" height="568" /></a>

<a href="https://rashita.net/blog/?attachment_id=28588" rel="attachment wp-att-28588"><img class="alignnone size-large wp-image-28588" src="https://rashita.net/blog/wp-content/uploads/2019/06/71267C87-E7B1-4BEE-A872-3116FD5E7CEC.jpg" alt="" width="320" height="568" /></a><a href="https://rashita.net/blog/?attachment_id=28589" rel="attachment wp-att-28589"><img class="alignnone size-large wp-image-28589" src="https://rashita.net/blog/wp-content/uploads/2019/06/D3A16065-569E-41FE-A67C-9980C099D0B7.jpg" alt="" width="320" height="568" /></a>

どうやら、うまく分割できたようだ。出力が2ページになっている。でもって、このように一つの変数の中に複数個のテキストが入っているものは「リスト」と呼ばれる。ようするに、今回は入力したテキストを分割して、リストにしたわけだ。

あとは、ここから一つめを取り出せればいい。そこで、今度は入力ボックスに「リスト」と入れてみる。

<a href="https://rashita.net/blog/?attachment_id=28590" rel="attachment wp-att-28590"><img class="alignnone size-full wp-image-28590" src="https://rashita.net/blog/wp-content/uploads/2019/06/65190F22-EDF5-4878-818A-85460997CF06.jpg" alt="" width="320" height="568" /></a>

ビンゴ。「リストから項目を取得」が求めているものだろう。とりあえず、これを置いてみる。すると、デフォルトで「最初の項目」が選択されていた。まさにそれがやりたかったのだ。

ちなみに他には「最後の項目」や「ランダム項目」や「項目のインデックス」や「Rangeの項目」などといったものが並ぶ。

最後二つはわかりにくいかもしれないが、要するに「n番目の項目を取得」と「n~m番目の項目を取得」という意味である。とりあえず今は、そういうこともできるんだなと軽く記憶に留めておくだけでいい。
<h2>データがつながる問題</h2>
というわけで、入力したテキストの一行目だけを取得することができた。あとは、Evernoteにノートを作成すれば……とはいかないのが、今回の難関ポイントである。

なぜかというと、そのまま直後にEvernoteのノート作成を置いてしまうと、直前のアクション、つまり「リストから項目を取得」からデータが渡されてしまうからだ。結果、ノートの本文すらも一行目だけになってしまう。それは意図する動作ではない。

<a href="https://rashita.net/blog/?attachment_id=28591" rel="attachment wp-att-28591"><img class="alignnone size-full wp-image-28591" src="https://rashita.net/blog/wp-content/uploads/2019/06/F2D91C3A-008A-43FE-BF69-E8CAF4D0A73F.jpg" alt="" width="320" height="568" /></a>

では、どうするか。

やりたいことは、入力したテキスト全体をEvernoteアクションに手渡しつつ、一行目だけを取り出したものをページタイトル部分に手渡すことだ。

ヒントは「変数」である。勘所のいい人なら、この言葉を検索ボックスに入れれば、自力で解決できるかもしれない。が、とりあえずここはややこしくなるので、いったん回を改めるとしよう。