---
title : Logseq、こんにちは　その１
link : 30951
date : Wed, 20 Apr 2022 02:52:45 +0000
categories : ["1-情報ツール考察"]
tags : ["logseq"]
draft : false
author : 倉下忠憲
---

Logseq（ログシーク）は、最近はやりのネットワーク型ノートアプリである。きわめて簡単に言えば、ローカルファイルで使えるRoam Researchだ。mdファイルを使う点はObsidianに似ている。ともかく、Scrapboxのように「リンク」ベースで話を進めるツールである。

デスクトップアプリは、以下からダウンロードできる。

<a href="https://logseq.com/">Logseq: A privacy-first, open-source knowledge base</a>

iOS版もつい最近配信された。

<a href="https://apps.apple.com/jp/app/logseq/id1601013908?uo=2">「Logseq」をApp Storeで</a>

とりあえず、私はMac版を用いるが、他のバージョンでも大差はないだろう。

<h3>画面とフォルダ</h3>

<a href="https://rashita.net/blog/?attachment_id=30952" rel="attachment wp-att-30952"><img src="https://rashita.net/blog/wp-content/uploads/2022/04/8fe93477c674e6e58ae4fc1afcaea9a6-700x1020.png" alt="" width="640" height="933" class="alignnone size-large wp-image-30952" /></a>

上記がLogseqの画面である（私はウィンドウ幅を狭くしてツールを使うのが好きだ）。

上部に日付があり、その下にエディタ領域がある。この時点で二つわかることがある。まず、「日付ベース」のファイル管理が為されている、という点。もう一つは、エディタ領域が「アウトライナーっぽく」なっているという点。どちらもなかなか興味深い。

logseqのデータを保存するフォルダには、以下の三つのフォルダが作成される。

<a href="https://rashita.net/blog/?attachment_id=30953" rel="attachment wp-att-30953"><img src="https://rashita.net/blog/wp-content/uploads/2022/04/27eb675a11d8057ac9d60ab63074eee8-700x535.png" alt="" width="640" height="489" class="alignnone size-large wp-image-30953" /></a>

「journal」には上記の日付のファイルが、「logseq」には設定周りのファイルが、「pages」には日付以外のファイルが保存される。つまり、日付のファイルが他のページのファイルとは別に管理されているわけだ。これは結構重要である。

ちなみに、日付表記のフォーマットは設定から変更できる。ページ上部の右側にある「…」から「設定」に入り、「エディタ」の「日時の表示形式」を変更すればいい。私は「yyyy-MM-dd」を好んで使っている（英語の月名表記はどうも性に合わない）。

<h3>基本的な操作：Home</h3>

さて、メイン画面に戻ろう。覚えておきたい操作は二つだ。Homeと前後の移動。どちらも上部メニューから行える。

<a href="https://rashita.net/blog/?attachment_id=30954" rel="attachment wp-att-30954"><img src="https://rashita.net/blog/wp-content/uploads/2022/04/3c38662baa2cfbcc1229db0d275e4da6-700x190.png" alt="" width="640" height="174" class="alignnone size-large wp-image-30954" /></a>

上部にある家のアイコンが「Home」である。これを押すとHomeに移動する。Homeとは何か？　すべての日付ファイルが一列に並んでいる状態だ。使い始めたときは、その日のページしかないのであまり意味はわからないだろうが、数日使えばわかる。下にスクロールしていくと、今日から昨日、昨日から一昨日というように日付が戻っていく。手帳のページを逆向きにくっているような感じだ。

その状態で、どこかの日付をクリックすると、該当の日付ファイルだけが表示される。そうなると、上下にスクロールしても特に変化はない。個別表示状態というわけだ。こうした個別状態のときだけHomeに戻るボタンが表示される。そのボタンがなければ、Homeにいると確認できるという寸法である。

ちなみにHome状態であっても、個別の日付ファイルを編集できる。だったら常にHome表示でいいじゃん？　と思われるかもしれないが、やっぱり違いがあるのである。その辺はタスク処理周りの話をするときに確認しよう。

とりあえず、Homeで日付一覧に移動し、日付をクリックでその日に移動する、という操作が覚えておきたい第一操作だ。

<h3>基本的な操作：「戻る」と「進む」</h3>

覚えておきたい第二操作は、go back と go foward である。それぞれ上部メニューの ← と → が対応している。もちろん、直感的に理解できるように「戻る」と「進む」だ。ブラウザのそれを思い浮かべればいい。

なぜこの操作を覚えておきたいかというと、最初に述べたようにLogseqが「リンク」ベースで話を進めるからだ。

たとえば、例示したページにはLogseqというリンクがある（リンクの作り方はまた説明する）。そのリンクをクリックすると、Logseqというページにジャンプする。そりゃまあ、当然だ。

<a href="https://rashita.net/blog/?attachment_id=30957" rel="attachment wp-att-30957"><img src="https://rashita.net/blog/wp-content/uploads/2022/04/d35ded404df7ff8c259ccdc435beba6c-700x835.png" alt="" width="640" height="763" class="alignnone size-large wp-image-30957" /></a>

で、たいていの場合、そうしてジャンプしたページで用事を終えたら「もといたページ」（つまり日付のページ）に戻りたくなるものである。そこで「戻る」が活躍するのだ。

Logseqは、リンクベースで話を進めるが、あちらこちらに縦横無尽にジャンプするという感じではなく、むしろ「その日のページ」をキャンプ地にしながら、必要なページに出かけて戻ってくる、という使い方が多くなる。なので「戻る」が使えるときわめて便利なのだ。

ちなみに、わざわざマウスで ← や → をクリックしなくても、ショートカットキーで command + [ やcommand + ]を押せば戻ったり進んだりできるのもWebブラウザと同じである。

<h3>さいごに</h3>

まずは、Logseqの「基本のき」を確認してみた。他にもいろいろ面白い要素があるツールなので、続けて紹介していきたい。

（蛇足になるが、Homeに戻るのもショートカットキーでいける。気になる人は自分で探してみるとよいだろう）