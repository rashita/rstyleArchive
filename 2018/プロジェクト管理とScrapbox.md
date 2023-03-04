---
title : プロジェクト管理とScrapbox
link : 25684
date : Tue, 25 Sep 2018 05:00:32 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

まずは以下の記事。

<a href="https://cyblog.jp/34311">Scrapboxについて分かってきたことと未だ分からないことまとめ | シゴタノ！</a>

<blockquote>
とはいえ、Scrapboxは万能ではなく、たとえばプロジェクト管理にはまったく使えない。
Scrapboxをプロジェクトリストとして使おうとすると、
　階層整理の概念がないのでプロジェクトが見渡せない
　日時情報がないので期限管理ができない。
</blockquote>

でもって、以下のツイート。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">これは誤りです。実際scrapbox自体の開発には、プロジェクト管理にscrapboxだけを使っています<a href="https://t.co/Z0M54i6agN">https://t.co/Z0M54i6agN</a><br>&gt; とはいえ、Scrapboxは万能ではなく、たとえばプロジェクト管理にはまったく使えない。<br><br>管理という概念を完全に捨てて、共感と協力だけで協調動作しているからな気もするが</p>&mdash; Sho Hashimoto (@shokai) <a href="https://twitter.com/shokai/status/1044228233334468613?ref_src=twsrc%5Etfw">2018年9月24日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

今回は、ちょいとこの問題を。

<h2>「プロジェクト管理」が指すもの</h2>

まず、両者の指している「プロジェクト管理」が同じものなのか、という疑問がありますね。たとえば、内と外です。

何かしらのプロジェクトがあり、そのプロジェクトをどのように進めていくのかを考えるのもプロジェクト管理と言えるでしょうし、複数のプロジェクトをいかにバランスを取って進めていくのかをマネジメントするのもプロジェクト管理でしょう。もちろん、両方を含む大きな概念もありそうです。

で、「プロジェクトリスト」を用いるのは、主に複数のプロジェクトをマネジメントする視点だと思います。

<blockquote class="twitter-tweet" data-conversation="none" data-lang="ja"><p lang="ja" dir="ltr">&gt; 階層整理の概念がないのでプロジェクトが見渡せない<br><br>階層はリンク構造の一形態なので、必要であれば作れば良い。例えばwikipediaではリンクだけで階層構造を表現しています <a href="https://t.co/L2DDRrcwnp">pic.twitter.com/L2DDRrcwnp</a></p>&mdash; Sho Hashimoto (@shokai) <a href="https://twitter.com/shokai/status/1044232787602006016?ref_src=twsrc%5Etfw">2018年9月24日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

たとえばですが、プロジェクト一つひとつにページを当てたとします。で、それぞれのページに#projectのリンクを設置したとします。で、そのprojectのページを開けば、一応一覧はできます。

<a href="https://rashita.net/blog/?attachment_id=25685" rel="attachment wp-att-25685"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-43.png" alt="" width="1122" height="626" class="alignnone size-full wp-image-25685" /></a>

が、これだけだと「どんなプロジェクトがあるのか」しかわかりません。そこで仮に、これらをページの中にリンクとして加えてみましょう（ドラッグでいけます）。

<a href="https://rashita.net/blog/?attachment_id=25686" rel="attachment wp-att-25686"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-44.png" alt="" width="939" height="442" class="alignnone size-full wp-image-25686" /></a>

これでプロジェクトのリストができあがりました。ここからは自由に階層化できます。

<a href="https://rashita.net/blog/?attachment_id=25687" rel="attachment wp-att-25687"><img src="https://rashita.net/blog/wp-content/uploads/2018/09/screenshot-45.png" alt="" width="527" height="509" class="alignnone size-full wp-image-25687" /></a>

これでOKでしょうか。そういう場合もあるでしょうし、そうでない場合もあるでしょう。たとえば、これだけではそれぞれのプロジェクトの次の行動（※）が何なのかがわかりません。それは、それぞれのプロジェクトのページに「入る」までわからないのです。
※こうした行動を総合的に管理するのがプロジェクト・ページの役割です。

かといって、それぞれのページタイトルの下に具体的な行動（タスク）を書いてしまうと、今度はプロジェクトページの中身との整合性が問題になります。片方を書き換えたときに、もう片方が書き換わらないのです。

この辺は、一般的なタスク管理ツール、あるいはアウトライナーならば詳細までを含めた一覧性が確保できます。で、そうした一覧のもとで、「ふむふむ現状はこうなっているのだな」と確認できるわけです。

粒度も、重要性も、規模も、処理の仕方も異なるさまざまなプロジェクト（これはGTD的な意味です。つまり、複数のタスクによって達成される目的ということ）の指針を得るためのダッシュボード。そういう使い方は若干Scrapboxでは難しいかもしれません。
※そんなダッシュボードなど必要ない、という仕事の進め方ももちろんあるでしょう。

理念的に言えば、プロジェクトページの中に行動（タスク）を書き込んでいくのではなく、行動そのものをページにして、そこにプロジェクトへのページリンクを付け加えていく方法であれば、「プロジェクトページの中にあるか、外にあるか」ということは考えなくてもよくなります。

先ほどのリストも、

　・[${projectName1}]
　　・[${taskName1}]
　　・[${taskName2}]
　・[${projectName2}]
　　・[${taskName3}]
　　・[${taskName4}]

のようになり、詳細行動を含めた一覧性は確保できます。

ただ、プロジェクトリストで扱う行動は、本当に些細で日常的なものも含まれうるので（特にGTDでは）、さすがにそのやり方は煩雑すぎるでしょう。逆に言えば、プロジェクトの行動として記載される情報がそれほど多くなく、一定の粒度を持っているならば、行動＝ページ、というやり方は可能だと思います。

■

とは言え、「日時情報」が扱えない問題は依然として残ります。タスク管理ツールでは、「9月25日にどんなタスクを実行しなければならないか」が一覧できるわけですが、Scrapboxでそれをやろうと思うと、やはりすべての行動をページ化して、それぞれのページに期限となる日付をページリンクの形で与えていかなければなりません。

また、その場合でも、前後の日付にどんな行動が入っているのか、その一週間にどんな行動が入っているのかは、そのままでは展望できません。「○日に○○の締切があり、それを絶対に仕上げないと編集さんに怒られるんだけど、その前の日に別の原稿の締切があるので、ということはその前の日にあれとこれを片付けておいて……」みたい思考は、あまり促進されない形式だと感じます。

もちろん、そういう思考はほとんどなくてもいい、という仕事の進め方もあるでしょうし、何が正解とは私にも言えませんが、「ある種のタスク管理のやり方は、Scrapboxではほとんど不可能か、すさまじく面倒」ということは（実体験として）言えると思います。

■

が、それはそれとして、私はタスク周りの情報も徐々にScrapboxに移行しつつあります。ようするに、タスク管理ツール・アウトライナー的な「詳細を含めた一覧性」の要求を手放してしまえば、だいたいはなんとかなるのです。

ただし、今は「もうこれで完璧」のレベルにはまったく辿り着いていません。その辺は、鋭意試行錯誤の真っ最中です。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.09.25</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 2,463<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


