---
title : Evernote、WorkFlowy、Scrapboxのアウトライン操作
link : 25215
date : Mon, 23 Jul 2018 02:27:24 +0000
categories : ["断片からの創造"]
tags : ["evernote","scrapbox","workflowy","≪断片からの創造≫"]
draft : false
author : 倉下忠憲
---

３つのツールのアウトライン操作を比較する。

ちなみに「アウトライン操作」とは、アウトライナー的な操作、あるいは要素（断片）の操作、ということである。

<h2>親要素</h2>

Evernoteは、ノートが情報の単位であり、その表示はソートで固定されていて、任意の順番に配列させることはできない。その代わり、ソート順は選択できる。

・更新日順
・作成日順
・題名順
・サイズ順
・参照元のURL順

それぞれ順と逆がある。

WorkFlowyは、項目が項目が情報の単位であり、すべての項目を任意の順番に配列できる。構造は再帰的で、いくらでも深く作れる。代わりに、自動的なソートは行えない。

Scrapboxは、ページが情報の単位であり、その表示はソートで固定されていて、任意の順番に配列させることはできない。その代わり、ソート順は選択できる。

・Date modified
・Data created
・Data last visited
・Trending
・MostPopular
・Most linked
・Title

逆順は存在しない。

<h2>子要素</h2>

Evernoteのノート内では、箇条書きリストを使うことでアウトライン操作が可能になる。

<a href="https://rashita.net/blog/?attachment_id=25216" rel="attachment wp-att-25216"><img src="https://rashita.net/blog/wp-content/uploads/2018/07/screenshot-22.png" alt="" width="380" height="207" class="alignnone size-full wp-image-25216" /></a>

tabを押せば段落が下がり、shift + tabを押せば段落があがる。その行であればテキストキャレットはどこに存在していても、同種の結果となる。

行の上下移動はショートカットは行えないが、冒頭のバレット（ビュレット）をマウスでドラッグすれば項目の移動は可能となる。

WorkFlowyは、──アウトライナーなので──、何もしなくてもアウトライン操作が可能である。

tab or shift + tabによる段落の上下だけでなく、(Macなら）shift + command + ↑↓での項目の上下移動もできる。上下移動の際は、その要素の子要素も一緒に連れていく。

また、冒頭のバレットのさらに前に表示される＋（あるいはー）によって下位項目表示のon/offも切り替えられる。この開閉はショートカットでも操作可能である。さらに、それぞれの項目にズームもできる。

Scrapboxのページ内では、何もしなくてもアウトライン操作が可能である。

行頭で、全角/半角のスペースかtabで一つ段落が下がり、それを削除すれば段落が一つ上がる。行頭以外のtabは機能しないが（というかtabを挿入するが）、行のどこかを選択すれば（行全体を選択しなくてもいい）同種の結果となる。

項目移動のショートカットキーもあり、control+↑↓→←で項目が移動し、alt(option)↑↓→←なら下位項目を引き連れて項目が移動する。ただし、WorkFlowyのような下位項目の開閉操作はない。

<iframe width="560" height="315" src="https://www.youtube.com/embed/jqLtvYyla1w" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<h2>さいごに</h2>

言う間でもなく、自由自在に項目を移動させられるのはアウトライナーであるWorkFlowyだ。自在な移動に加えて、項目の開閉も行える。ビューポイントを移動させるような場合はたいへん便利だ。

ただし、段落の上下移動のショートカットと、インデントを一つ落とすショートカットが別のキーなっている点はある。Scrapboxでは、control（ないしalt）+↑↓→←と統一されているのでわかりやすい（むろんtabでの操作も可能だ）。また、Scrapboxでは行単位の移動とブロック単位の移動の二種類があるのも特徴的である。

Evernoteでは、そもそも箇条書きリストに変更する必要があり、その移動もマウスのみなので非常に限定的である。

親項目については、EvernoteとScrapboxはソート固定であり、任意の配置は実現できない。ただし、Scrapboxは「pin」という固定表示機能がある。このpinは複数設定できるので、擬似的に任意の配置を実現することもできる。つまり、柔軟性がある。

私はよく、「Evernote内のノートがWorkFLowyだったらな」ということを感じるのだが、Scrapboxはそれに非常に近い感覚を与えてくれる。ページ内での断片的操作を許容してくれるのだ。特にショートカットキーで操作できるのがありがたい。

総じて言えば、WorkFlowyは極めて流動性が強い。全体が「断片」であり、移動（及び操作）可能である。Evernoteは、やや流動性が低く、ノート表示順が固定されていてページ内の断片的操作もあまり支援してくれない。Scrapboxはその間くらいの流動性で、ページはやや操作でき（pin）、ページ内はかなり断片的操作が可能である。

このようにツールにおける断片的操作の広さ（≒要素の流動性の高さ）は、結構違っている。同じように見えるツールでも、使ってみると案外違うというのはこういう操作感にも由来する。でもって、知的生産ツール（情報整理ツール）の話は、こういうところが面白いわけである。

<strong>▼7月27日発売:</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863542526/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51L7tTg9PML._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863542526/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.07.23</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2018-07-27)<br />売り上げランキング: 20,583<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863542526/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

