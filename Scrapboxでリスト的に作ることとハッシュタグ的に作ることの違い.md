---
title : Scrapboxでリスト的に作ることとハッシュタグ的に作ることの違い
link : 25963
date : Fri, 26 Oct 2018 02:37:47 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

Scrapboxで情報をまとめてやるぜ、と思いつくと、二つの道筋があることに気がつきます。

まず、所属元のページを作り、そこにリスト的に項目を加えていくこと。いわゆるアウトライナー的な操作です。

次に、個々の要素のページを作っておいて、そこに共通する属性をリンクで付け加えていくこと。いわゆるハッシュタグ的な操作です。

<a href="https://rashita.net/blog/?attachment_id=25964" rel="attachment wp-att-25964"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-65.png" alt="" width="788" height="601" class="alignnone size-full wp-image-25964" /></a>

基本的にこの二つはほとんど同じなのですが、違いもあります。

実際例を交えて見ていきましょう。

<h2>リスト的な場合</h2>

まずは、リスト的な場合から。「読みたい本」を管理しようとしているとイメージしてください。

このとき「読みたい本」というページを先に作り、そこにしかるべき項目を放り込んでいく形になります。

<a href="https://rashita.net/blog/?attachment_id=25965" rel="attachment wp-att-25965"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-66.png" alt="" width="895" height="567" class="alignnone size-full wp-image-25965" /></a>

上のサンプル画像は実際にあるプロジェクトのページのものですので、すべての項目がすでにリンクになっていますが、実際はテキストの書きだし→それをリンク化して、各々のページを拡充していく、という流れになるでしょう。

このようになっているとき、個々のページは、たとえばこのようになりえます。

<a href="https://rashita.net/blog/?attachment_id=25966" rel="attachment wp-att-25966"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-67.png" alt="" width="1049" height="763" class="alignnone size-full wp-image-25966" /></a>

おおもとのページからこのページにリンクが貼ってあるので「Links」に「読みたい本」が出ています。このリンクを辿ることで、他の読みたい本にもアクセス可能です。

ということは、個々のページを操作することなく、ただ「読みたい本」ページでリンクを操作する（追加する/削除する）だけで、このリンクネットワーク構造を操作できる、ということです。

難しい言い方をしましたが、日常的な読了管理において、個々のページを開く必要はなく、ただこの「読みたい本」ページでリンク操作すればOK。という意味合いです。

また、このやり方の場合、すべての要素をページ化する必要はない（テキストのまま残しておいても大丈夫）、という効果もあります。


<h2>ハッシュタグ的な場合</h2>

では、ハッシュタグ的な場合はどうでしょうか。

まず、最初に個々の要素のページを作り、そこに「読みたい本」というリンクを追加することになります。わかりやすいようにハッシュタグ記法で記入してみました。

<a href="https://rashita.net/blog/?attachment_id=25967" rel="attachment wp-att-25967"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-68.png" alt="" width="1021" height="755" class="alignnone size-full wp-image-25967" /></a>

で、この「読みたい本」というハッシュタグをクリックすると、次のページが表示されます。

<a href="https://rashita.net/blog/?attachment_id=25968" rel="attachment wp-att-25968"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-69.png" alt="" width="1017" height="504" class="alignnone size-full wp-image-25968" /></a>

さて、この二つ、やはり似ているようで違いがあります。

まず第一に、個々のページの関連ページに直接他の「読みたい本」が表示されている点です。

リスト方式の場合、個々のページは大元のページからリンクを貼られているだけなので、兄弟ページに当たるページは表示されません。しかし、ハッシュタグ方式だと、個々のページがおおもとのページにリンクを貼っているので、その他のページが表示されるわけです。

<a href="https://rashita.net/blog/?attachment_id=25970" rel="attachment wp-att-25970"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-70.png" alt="" width="804" height="610" class="alignnone size-full wp-image-25970" /></a>

また、ハッシュタグ方式の場合は、おおもとのページ（サンプルでは「読みたい本」のページ）は、実体化されていません（見た目がやや薄いページ、ということです）。

で、実体化されていないページは、Links欄には表示されず、またHome画面（≒ページリスト画面）にも表示されません。

ハッシュタグ的に使う場合は、Links欄に表示されない方が便利なので、それは良いのですが、後者に関しては、Home画面から、「読みたい本」のページを見つけて、それをクリックして、リストを閲覧する、という動線が取れないことを意味します。
※Homeの検索からページを見つけてアクセス、は可能です。

つまり、この二つやり方の差異の多くは、ページの実体化の有無に影響されていると言ってもいいでしょう。

<h2>どちらがいいのか？</h2>

もちろん、他にも違いはあります。

リスト形式で並べた場合、その順番を制御できます。「読みたい本」であれば、もっとも読みたい本（≒次に読もうと思っている本）を上位に持ってくることができます。そういう操作が簡便なのもScrapboxの特徴なので、是非とも活かしたい気持ちはあります。

現状、Scrapboxでは関連ノートの表示順を任意で操作できないので、ハッシュタグ方式ではこれができません。逆にその操作が可能になれば、二つの方式の差異は小さくなります。

また、ハッシュタグ方式では、関連ページに直接他の本が並ぶという動線の良さと、さらに「未読/読了」などを変更しようとした際に、必ず個々のページを開かなければならない、という動線の設定が活きます。これは一見不便なようですが、そうして読了管理をする際に、コメントなどをついつい書き込んでしまう、というトリガー効果が期待できるので、これはこれで見えないメリットではあるでしょう。

もちろん、ハイブリッド方式もありえます。個々のページにハッシュタグをつけつつ、そのハッシュタグページを実体化するのです。そして、そこでリストも作ってしまう。リストへの項目の追加は、下に表示されている関連ページをエディタ内にドラッグするというやり方で簡易化できるでしょう。

これで両方の特徴が得られるわけですが、未読→読了の際に、二つのページを操作しなければならない問題は残ります。たぶん、そういうやり方はなかなか続かないのではないかと想像します。

ということを踏まえた上で、どちらが良いのか？　もちろんそれは管理する対象によって適宜判断してもらうしかありません。

とりあえず、特徴をまとめれば、

・個々の要素をすべてページにしたいわけではない→リスト
・並ぶ順番を操作したい→リスト
・Home画面に並べたい（Pinを打ちたい）→リスト
・個々のページに直接兄弟要素を表示させたい→ハッシュタグ

とはなるでしょう。ちなみに、ハッシュタグページを作り、単にそれを実体化させる、という折衷案もあります。

<a href="https://rashita.net/blog/?attachment_id=25971" rel="attachment wp-att-25971"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-71.png" alt="" width="1029" height="488" class="alignnone size-full wp-image-25971" /></a>

これならば、ハッシュタグの使い方をしながらHome画面にも表示されるので、用途によって便利に使えるかもしれません。というか、これが一般的なScrapboxのページの作り方でもあります。

というわけで、今回は、リストによる管理とハッシュタグ（≒リンク）による管理の違いを紹介してみました。

よければ、以下の本もご覧ください。

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.10.26</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 22,196<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

