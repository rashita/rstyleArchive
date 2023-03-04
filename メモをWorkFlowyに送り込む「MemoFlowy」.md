---
title : メモをWorkFlowyに送り込む「MemoFlowy」
link : 17210
date : Fri, 04 Dec 2015 01:53:10 +0000
categories : ["アウトライナーで遊ぼう","物書き生活と道具箱"]
tags : ["iphoneipad","memoflowy","workflowy"]
draft : false
author : 倉下忠憲
---

「WorkFlowyにはAPIがない」

と書くと、まるで一昔前のラノベのタイトルみたいだが、実際にその通りなのだから仕方がない。今のところ公式のAPIはない。

よってWorkFlowyのデータにアクセスするには、公式のアプリを使うかブラウザから飛んでいくかの二つしかなかったのだが、新しい選択肢が増えた。嬉しい限りだ。とは言え、正確に言うとちょっと違う。

<span class="appIcon"><img class="appIconImg" height="60" src="http://is4.mzstatic.com/image/thumb/Purple69/v4/4b/e0/01/4be00170-fd68-d76e-7d1e-8076e1b579c2/source/60x60bb.jpg" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/memoflowy/id1052582668?mt=8&uo=4&at=11l4y8" target="itunes_store">MemoFlowy</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, ユーティリティ</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/memoflowy/id1052582668?mt=8&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_appstore-sm.png) no-repeat;width:61px;height:15px;"></a></span><br style="clear:both;">

「MemoFlowy」は二つの画面からなる。一つはメモ入力画面。もう一つはメモ貼り付け画面。この二つを行き来して、WorkFlowyに新規メモをどんどん貼り付けていく。

ソリューションはおどろくほど単純で、いっそ力技感が漂うくらいだ。APIがないので直接WorkFlowyのサイトで書き込むしかない。だったら、それをできるだけ省力で行えるようにしよう。こういうコンセプトである。

どういうことだろうか。

<a href="https://rashita.net/blog/?attachment_id=17211" rel="attachment wp-att-17211"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/IMG_6404-500x750.png" alt="IMG_6404" width="500" height="750" class="alignnone size-medium wp-image-17211" /></a>

メモ画面は普通のメモエディタだ。違うのは行頭のスペースが「→」で表示されること（※）。この矢印一つが、WorkFlowyでの階層一つを意味している。
※矢印表示を消すこともできるようだが、おそらくそうしない方がいい。

まずはこの画面でパシパシメモを入力する。そして、その後右下の「WorkFlowy」を押す。

<a href="https://rashita.net/blog/?attachment_id=17212" rel="attachment wp-att-17212"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/IMG_6405-500x750.png" alt="IMG_6405" width="500" height="750" class="alignnone size-medium wp-image-17212" /></a>

すると画面が切り替わる。この画面は要するにWebViewで、つまりはブラウザだ。そこでWorkFlowyのページが開いていると思ってもらって構わない。で、さっき入力したメモをペシっと貼り付ける。これで、擬似的に公式アプリ以外からでも新規のメモ作成（というか挿入）が可能になった。

<a href="https://rashita.net/blog/?attachment_id=17213" rel="attachment wp-att-17213"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/IMG_6406-500x750.png" alt="IMG_6406" width="500" height="750" class="alignnone size-medium wp-image-17213" /></a>

<a href="https://rashita.net/blog/?attachment_id=17214" rel="attachment wp-att-17214"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/IMG_6407-500x750.png" alt="IMG_6407" width="500" height="750" class="alignnone size-medium wp-image-17214" /></a>

基本的にはただそれだけなのだが、「省力」という点にかなりこだわっている。メモ画面からWorkFlowyの画面に切り替わるとき、メモ画面の内容が自動的にクリップボードに保存されているのだ。だから切り替わった画面で、ペーストを選択すればそれだけで事足りる。つまり手順はこうだ。

<ol>
<li>メモ画面でメモの入力</li>
<li>WorkFlowy画面に移動</li>
<li>貼り付けたいところにペースト</li>
</ol>

移動先のWorkFlowy画面は定位置に固定できる。とりあえずはそこに貼り付けておき、その後適切な項目の下に移動すればいいだろう。つまりは、inboxというわけだ。項目の移動が自由に行えるWorkFlowyとinboxという概念はとても相性が良い。

また、このアプリは簡易のWorkFlowyビューアーとしても使える。

好きな項目を「お気に入り」（ブックマーク）にできるので、よく参照する項目を指定しておくと良いだろう。


<a href="https://rashita.net/blog/?attachment_id=17215" rel="attachment wp-att-17215"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/IMG_6408-500x750.png" alt="IMG_6408" width="500" height="750" class="alignnone size-medium wp-image-17215" /></a>


<a href="https://rashita.net/blog/?attachment_id=17216" rel="attachment wp-att-17216"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/IMG_6409-500x750.png" alt="IMG_6409" width="500" height="750" class="alignnone size-medium wp-image-17216" /></a>

アプリの紹介はここまでなのだが、思ったことを一つ。どうやらこのアプリは、WorkFlowyのユーザーに好評なようである。なによりだ。APIが使えないという制約の中で、見事に工夫を発揮させている。すばらしい。

が、私はこうも思う。もしWorkFlowyが簡易なものであれAPIを開放したらどうなるのだろうか、と。おそらく今のWorkFlowyはカバーしきれていないユーザーのニーズやウォンツがある。それもたくさんある。

もちろん、それを公式がすべてフォローすることはできないし、すべきでもない。が、所詮はツールは使うものであり、その主導権は使い手にある。その意味で、WorkFlowyのもう一段階の普及にはユーザーやサードパーティーを巻き込んでいく姿勢が必要だろう。まあ、現状でも十分便利なツールなのではあるが。