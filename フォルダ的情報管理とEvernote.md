---
title : フォルダ的情報管理とEvernote
link : 19224
date : Tue, 01 Nov 2016 23:01:34 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernoteについて書きたいことが二つある。少し長くなりそうなので、わけて書くことにする。

まずは、フォルダ的な情報管理について。

<h3>情報の性質と関係ない要件</h3>

WindowsでもMacOSでも、情報は「ファイル」という単位で管理される。さらにそのファイルは「フォルダ」という単位で管理され、フォルダには別のフォルダを入れることが可能だ。つまりこれは、入れ子状であって、さらにツリー状である。

難しいことは何もない。

project/project_a/企画案.txt

このフォルダ構造（ファイル構造）は、情報を「分類」していて、なおかつファイルに「一つの場所」を与えている。イノセントに考えれば、情報管理においてそれらの要素は必要ないはずである。分類をまったく行わなかったり、一つの情報が同時に複数の場所に存在していても構わないだろう。

が、そうはなっていない。

<h3>もしかしたら、の理由</h3>

「一つの場所」は、おそらく二つの要因から発生したのだろう。

一つは物理的な要素だ。情報はメモリなりハードディスクなり書き込まれる。その０と１の羅列は、具体的な一つの場所を占めることになる。本来情報はその羅列とは直接関係ないはずである。しかし、概念を運用する上では、その制約はメタファー的に効いてくる。

もう一つは、私たちの脳の事情である。私たちの脳は、すでに「場所」を認知し、概念操作するニューロンを備えている（幼児からなのか、自我が芽生えてからなのかはわからないが）。よって、情報というつかみ所のないものを扱う場合に、「場所」という慣れた概念を適用することはなんらおかしいことではない。

とびっきりの暗記術として知られる「記憶の宮殿」も、結局「場所」という概念装置を用いて記憶（つまり情報）を管理している。全文化において普遍的に見られる傾向であるかはわからないが、すでに獲得している脳の機能の流用は珍しい話ではない。

あるいは、こういう言い方ができるかもしれない。

フォルダ管理的なものをミームとして捉える。そして、そこに自然淘汰を持ち込む。つまり、「もし、パソコンなるものが生まれたときに、それがフォルダ的な情報管理方法に準拠していなければ、ここまでパソコンが一般的になることはなかったのではないか」。

とまあ、こうなった理由はいろいろ考えられるだろうが、ともかく今のパソコンはすでに「そうなってしまっている」ことだけはたしかだ。

<h3>新しい世代と、新しいUI</h3>

しかし、これをそのまま継承していかなければいけない理由はないだろう。そもそもとして、情報は別に「一つの場所」に縛りつける必要はないし、あらかじめproject/project_a/企画案.txtに分類する必要もない。そうした行為は、システム側からの要請であって、情報からの要請ではないのだ。

それに私たちの脳も、もうすっかり慣れてしまった。何に？

インターネットとスマートフォンにだ。

今の若い世代は、「フォルダなにそれ？」な感じで、スマートフォンやタブレットを操作し、インターネットを駆け巡る。もうパーソナルなコンピューティングシステムと仲良くなるために、「既存の概念」を流用する必要はなくなりつつある。Yahoo!のディレクトリ型（電話帳的システム）からGoogleの検索型への移行は、はっきりそれを支援している。Googleが後ろでどれだけフォルダ的管理を行っているのかはわからないが、それを使う私たちにとってはたいした意味がない。

同じことはクラウドにも言える。「保存する」という概念すら消失しつつある中、情報と「一つの場所」の感覚は明らかに遠ざかっている。

<h3>そしてEvernote</h3>

そこでEvernoteである。

Evernoteは、データベースシステムである。一つひとつの情報は「ノート」という形で管理される。ノートにはタグをつけたり、付けなかったりできるので、情報をまったく分類しないこともできるし、複数に分類したりもできる。後からの変更も可能だ。

しかし、である。

Evernoteは、ノートブックを持つ。これは何か？　機能的には＿＿ノートが持つメタ情報の一つという意味では＿＿タグと同じなのだが、タグと違って「１つ」オンリーである。Evernoteのノートは、複数のノートブックに所属することはできないし、また、どこのノートブックに属さない、という選択もできない。

これは何か？

「場所」である。Evernoteのノートブックは、ノートの「場所」を管理するための手法であり、その意味ではフォルダ的思想に基づいている。ああ、Evernoteよ。お前もか。

と大げさに嘆いてみたところで、実際このノートブックが使いにくいわけではない。タグとは別の管理単位を作ることで、二軸による情報検索が行える。これは一つの発明と言っていいだろう。

が、それでも私は思ってしまう。もっと別の形はないのだろうか、と。Evernoteが裏側でノートブックやタグを持つのは良いとして、UIとして「ノートブック」を土台としたもの＿＿言い換えれば、フォルダ的思想を土台としたもの＿＿とは別の形にはなりえないのか、と。

たとえば、そう、Wikiシステムのようなハイパーリンクベースの。

<h3>さいごに</h3>

ということを考えながら、最近Evernoteの使い方（実際的な運用法）をアレンジしている。

まだ完全に固まっているわけではないが、個人的に面白い形になりつつある。それについては次回書こう。

次回：<a href="https://rashita.net/blog/?p=19227">R-style » リンク駆動式Evernote運用術</a>

<strong>▼こんな一冊も</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.11.01</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 893<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/515rWUhPqbL._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.11.01</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 41,273<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4774138975/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51psMmyTdWL._SL160_.jpg" alt="パターン、Wiki、XP ~時を超えた創造の原則 (WEB+DB PRESS plusシリーズ)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4774138975/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">パターン、Wiki、XP ~時を超えた創造の原則 (WEB+DB PRESS plusシリーズ)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.11.01</div></div><div class="amazlet-detail">江渡 浩一郎 <br />技術評論社 <br />売り上げランキング: 386,401<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4774138975/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


