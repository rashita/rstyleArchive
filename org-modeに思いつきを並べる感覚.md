---
title : org-modeに思いつきを並べる感覚
link : 29235
date : Sat, 27 Jul 2019 01:56:16 +0000
categories : ["物書き生活と道具箱"]
tags : ["emacs","org-mode","spacemacs","アウトライナー"]
draft : false
author : 倉下忠憲
---

最近「<a href="https://scrapbox.io/rashitamemo/Spacemacs">Spacemacs</a>」でorg-modeを使っている。

たとえば、こんな画面だ。

<a href="https://rashita.net/blog/?attachment_id=29236" rel="attachment wp-att-29236"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-32-700x600.png" alt="" width="700" height="600" class="alignnone size-large wp-image-29236" /></a>

白地で表示されている部分は本文レベルで、上の <2019-07-27 土>に属している。その見出し行でtabキーを押せばシュッと隠れる。

<a href="https://rashita.net/blog/?attachment_id=29237" rel="attachment wp-att-29237"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-33-700x600.png" alt="" width="700" height="600" class="alignnone size-large wp-image-29237" /></a>

アウトライナー的な操作である。

<h2>見出しを立てる</h2>

たとえば、その日のページを作って、たらたらと思いついたことを書く。数行で終わるようなものもあれば、ちょっと膨らむようなものもある。膨らむようなものは、案外大切かもしれない。どこかに原稿で書くかもしれない。デイリーの中に没させておくのはもったいない。

そういうときは、タイトルにあたる行の頭に*を一つ追加してやる。それでそこが見出しへと化ける。

<a href="https://rashita.net/blog/?attachment_id=29238" rel="attachment wp-att-29238"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-34-700x571.png" alt="" width="700" height="571" class="alignnone size-large wp-image-29238" /></a>

が、このままだとブロックの下にある行まで巻き込まれてしまうので、適当に順番を移動させて、一番下にでも移動させる。

<a href="https://rashita.net/blog/?attachment_id=29239" rel="attachment wp-att-29239"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-35-700x383.png" alt="" width="700" height="383" class="alignnone size-large wp-image-29239" /></a>

これでバッチリだ。tabキーを押せば、下がまるっと隠れる。しかし、 <2019-07-27 土>の中身を隠しても、このブロックは隠れない。

<a href="https://rashita.net/blog/?attachment_id=29240" rel="attachment wp-att-29240"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-36.png" alt="" width="612" height="459" class="alignnone size-full wp-image-29240" /></a>

無事、独立したわけだ。あとは、折を見てこのブロックの中身を肉付けしたり、どこかの原稿で利用したりと、あとは何とでもなる。普段は一行だけの地味な存在だが、tabキーを押せばパッと開く。なかなか快適だ。

もちろん、これだけであれば、アウトライナーでもできるし、他のツールでもできる。が、org-modeは、もう一段ディープだ。

画面を分割させ、そのブロックがどこに位置づけられそうなのかを、じっくりと検討ができる。

<a href="https://rashita.net/blog/?attachment_id=29242" rel="attachment wp-att-29242"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-37-700x390.png" alt="" width="700" height="390" class="alignnone size-large wp-image-29242" /></a>

アウトライナーで長い項目を扱う場合は、要素のドラッグをキープしつつスクロールで行ったり来たりしなければいけない。これが存外に落ち着かない。かといって、普通にスクロールしたただけだと、今度は移動すべき項目をもう一度見つけ直す手間がある。画面分割は、そういう細かい操作は必要ない。

というか、あらゆるアウトライナーは画面分割を備えるべきである。これはもう、本当に声を大きくして主張したい。ある程度要素が増えたり、階層が増えたりすると、一画面ではとても収まらないので、一度に扱える情報が限定されてしまう。単に備忘録として使うならともかく、知的操作するには非常に不便だ。

でもまあ、アウトライナーに不満を言っても仕方がない。ともかく、この操作がなかなか快適だ、という話だ。

日ごとのページを書き、よさげなものは見出しを立てる（あるいは見出しのレベルを上げる）。それで目に触れるようにして中身を加筆していき、必要とあれば、どこかのプロジェクトへと移す。しかも画面分割で全体を俯瞰しながら、移動先を決定できる。

構成する機能としてはごくごく単純なもので、現代の目新しいツールに比べると驚くことはほとんどない。でもこれが、驚くほど快適なのである。

が、ここで「じゃあ皆さんorg-modeを使いましょう」と訴えかけないのが、当ブログである。とりあえず、「デイリーにつらつら書いて、必要とあれば、新しく見出しを立てる」という運用方法の快適さは折り紙付きなので、このやり方から採用されると良いだろう。

また、気が向けばorg-modeについては書くかもしれない。なにしろ、私もぜんぜんわかっていないので、書けることに限りがあるのが難点である。

<strong>▼こんなコンテンツも:</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer"><img src="https://images-fe.ssl-images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank" rel="noopener noreferrer">amazlet</a> at 19.07.27</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 21,336<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<a href="https://note.mu/rashita/n/n11129ad00f40">タスク管理の目指すもの/コマンドラインの静かなる執筆/断片的な思いつきの扱い方｜倉下忠憲｜note</a>