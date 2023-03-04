---
title : org-modeのタスク表示をカスタマイズすること
link : 29286
date : Wed, 07 Aug 2019 02:34:56 +0000
categories : ["「タスク」の研究"]
tags : []
draft : false
author : 倉下忠憲
---

emacsのorg-modeには、項目をタスクとして扱うための機能がある。

たとえば、以下のオレンジが見出しで、白が本文だが、オレンジ行でshift + → するとTODOが付与される。

<a href="https://rashita.net/blog/?attachment_id=29287" rel="attachment wp-att-29287"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-3.png" alt="" width="687" height="229" class="alignnone size-full wp-image-29287" /></a>

<a href="https://rashita.net/blog/?attachment_id=29288" rel="attachment wp-att-29288"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-4.png" alt="" width="567" height="214" class="alignnone size-full wp-image-29288" /></a>

さらに、もう一度shift + → すると、今度はDONEになる。

<a href="https://rashita.net/blog/?attachment_id=29289" rel="attachment wp-att-29289"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-5.png" alt="" width="569" height="215" class="alignnone size-large wp-image-29289" /></a>

しかも、終了時刻まで自動的に記録される。実に便利だ。

さらに、単に行にTODOが付与されるだけでなく、ファイル全体からTODOがついたものだけを表示させることもできる。さらに、複数ファイルでそれを行うこともできる。これも、なかなか便利である。

が、そういう話はまた別の回に譲るとして、私は上の機能を観てふと思った。これをタスク管理寄りではなく、原稿管理的に使えないか、と。

<h2>TODOを書き換える</h2>

下準備はごく簡単である。下の行をそのファイルの行頭にでも追加するだけだ。


#+TODO: MEMO DRAFT | DONE

<a href="https://rashita.net/blog/?attachment_id=29290" rel="attachment wp-att-29290"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-6.png" alt="" width="573" height="389" class="alignnone size-full wp-image-29290" /></a>
※設定を読み込む必要があるので、再起動するかバッファの再読み込みを実行されるとよいだろう。

こうしておけば、shift + →で、次が順々に表示される。

<a href="https://rashita.net/blog/?attachment_id=29291" rel="attachment wp-att-29291"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-7.png" alt="" width="519" height="240" class="alignnone size-full wp-image-29291" /></a>

<a href="https://rashita.net/blog/?attachment_id=29292" rel="attachment wp-att-29292"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-8.png" alt="" width="553" height="332" class="alignnone size-large wp-image-29292" /></a>

<a href="https://rashita.net/blog/?attachment_id=29293" rel="attachment wp-att-29293"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-9.png" alt="" width="674" height="299" class="alignnone size-large wp-image-29293" /></a>

MEMO→DRAFT→DONE。項目が一つ増えて、一つの項目名が変わっただけだ。ほとんど大差ない。が、私の使い方にはこの三段階が合っている。言い換えれば、しっくりくる。

私は別に、ここで org-mode 最高！とアピールしたいわけではない。もちろん、いろいろすごい点はあるのだが、万人向けツールなのかの確証はまだない。ただ、このカスタマイズ性は注目に値すると思う。なにせ、表示を変えただけではなく、「新しい項目の追加」という機能面のカスタマイズまでできているのだ。そのカスタマイズによって、自分にフィットした使い方が実現できた。コンピュータを「自分の道具」にすることができた。それが持つ可能性とはいかほどか。

<h2>さいごに</h2>

与えられた機能に自分を合わせるのではなく、与えられた機能をベースにしながら自分なりの使い勝手を作っていける。それって、結構大切なことなのではないか。

私が注目しているのは、単にエディタ（やタスク管理ツール）の話だけではない。そこに潜む基本的なマインドセットがここでは議論の舞台に上がっている。与えられたものに自分を合わせるのか、それとも自分の目的に向けてカスタマイズするのか。

この点については、次の更新でもう一度別の観点から検討してみたい。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4065151562/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer"><img src="https://images-fe.ssl-images-amazon.com/images/I/31yz41bTULL._SL160_.jpg" alt="「やること地獄」を終わらせるタスク管理「超」入門 (星海社新書)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4065151562/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">「やること地獄」を終わらせるタスク管理「超」入門 (星海社新書)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank" rel="noopener noreferrer">amazlet</a> at 19.08.07</div></div><div class="amazlet-detail">倉下 忠憲 <br />講談社 <br />売り上げランキング: 26,130<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4065151562/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
