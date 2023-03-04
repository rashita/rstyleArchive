---
title : Scrapboxのスーパーハッシュタグ構想
link : 25845
date : Sat, 13 Oct 2018 02:01:44 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

Scrapboxの「<a href="https://scrapbox.io/comic-forum/">おすすめ漫画</a>」は非常に楽しいプロジェクトで、私も参加させていただいているが、一つ困ったことがあった。

それは、<a href="https://scrapbox.io/rashitaobj/">Kurashita's Object Collection</a>で、もうすでに漫画を並べてしまっている、という点だ。心理的な観点から言って、Aの場所に並んでいる情報を別の場所Bに移動させることには、面倒さを感じる。

単にコピペしていけばいいだけのことだが、そうはいっても何かしら心にコスト的な感覚が生じてしまう。だって、もうそこにあるのに、という感じがするのだろう。

でもって、似たような話は別の領域でもあるかもしれない。

基本的にScrapboxでは、自分のプロジェクトに情報を置いておきたい。その方がリンクをつなげやすくなるからだ。しかし、一方で共通のクラスタで情報を持ち寄る共有（共同）プロジェクトも面白いし、それが簡単に作れるのもScrapboxの魅力である。

個人的な構想でも、○○さんとか▼▼さんを誘って、知的生産についていろいろ書き込んでいくプロジェクトを作ろうかなと思いつつ、それらの人はもう自分の公開プロジェクトを持っているし（だからこそ、その人を誘おうと決意できたわけだ）、そうなると、あっちに書こうかこっちに書こうか的問題は生じることになる。

少し具体的に書こう。たとえば、<a href="https://scrapbox.io/nishio/">西尾泰和のScrapbox</a>プロジェクトには知的生産にまつわる面白い話が多い。一方で一応（一応だ）私も知的生産系の著作がある。二人の観点は重なるところもあるし、異なるところもある。発想が生まれる土壌としては極めて良好だと推測できる。

だったら、声を掛けて知的生産の技術ついて議論するプロジェクトを立ち上げたらどうなるかを考えると、やっぱりそれぞれが自分のプロジェクトに書きたい気持ちが強くなるのではないか、という気がしてくる。こうなると新プロジェクトの育成はおぼつかない。

まったく新しいことを書き込んでいく場合ならば、こうした問題は生じないのかもしれないが、公開されているプロジェクトを閲覧し、「そこに書かれているようなことの一部」をまとめて、融合知に向けて進んでいきたい、というような思いのとき、あっちに書くかこっちに書くか問題は生じてしまうだろう。

あるいは、そもそもの新プロジェクトの方向性が不明瞭であることが問題なのかもしれない。具体的なプロダクトに向けて知見を集めていく、という指針があるともう少しプロジェクトごとの役割分担は明確になるだろう。しかし、それでうまくいくかどうかはわからない。

■

以上が、現状抱えている課題というかなんというかである。

これはもしかしたら解決しなくてもいい課題なのかもしれない。私が抱く新構想のようなものは実はまったく空虚なもので、どうやっても頓挫する類のものかもしれない。

そういう仮説を受け容れつつも、少し考えてみたい。たとえば、ハッシュタグの活用だ。

Scrapboxでは#付きの言葉はハッシュタグに使われる（あるいはそのように使うことができる）。しかし、その実体は普通のページリンクである。表記が違うだけだ（ただし、表現も異なるのでCSSで別のスタイルを当てられる特徴はある）。

そして、ハッシュタグ的なものは、便利な反面デメリットも抱えている。記述が増えない、という問題だ。

そうであればいっそのこと別の使い方をしたらどうだろうか。

たとえば、あるページに#知的生産の技術というハッシュタグが書き込まれていたとする。すると、https://scrapbox.io/hashtag/#知的生産の技術とかいったURLにアクセスすると、Scrapboxの全プロジェクトに存在する、#知的生産の技術が書き込まれたページが閲覧できるのだ。ようするに、Twitter的なハッシュタグということである。

こうすることで、私は自分のプロジェクトに書き込みながら、#知的生産の技術の話題に参加することができる。そして、そのような話題を扱っている面白そうな別のプロジェクト（あるいはそのオーナー）を見つけ出すことができる。

しかし、さすがに全プロジェクトが対象だと処理的にハードかもしれない。だったら、groupという概念を作り、そこにメンバーとして参加している人のプロジェクトを対象とするのはどうか。その場合、メンバーが所属する全プロジェクトではなく、指定したプロジェクトに限定する。

つまり、粒度を一つ上げるわけだ。Scrapboxのプロジェクトには、人がメンバーとして所属する。そしてgroupには、プロジェクトがメンバーとして所属する。そうして、プロジェクト同士の知をつなげていく。

■

もちろん、粗があることは承知である。たんなるブレスト的思いつきにすぎない。

それでも、複数のプロジェクトの知をつなげていく、という視点はたぶん面白いだろう。どういう形で実装されるのが現実的なのかは私にはまったくわからないが、何かしらそういう仕組みができたら楽しいと思う。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.10.13</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 12,768<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

