---
title : Scrapboxでハッシュタグを書き換える工程
link : 29663
date : Sat, 02 Nov 2019 03:48:29 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

Scrapboxに「良い言葉」をコツコツ集めています。そしてそこに、「#引用」というハッシュタグ（ページリンク）を付けていました。

#引用をクリックすれば、以下のように集めた「良い言葉」が一覧できます。

<a href="https://rashita.net/blog/?attachment_id=29664" rel="attachment wp-att-29664"><img src="https://rashita.net/blog/wp-content/uploads/2019/11/screenshot-700x430.png" alt="" width="700" height="430" class="alignnone size-large wp-image-29664" /></a>

でも、問題があることに気がつきました。「引用」（という概念）について言及したいときに、こうして集めた言葉とバッティングしてしまうのです。たとえば、「[引用]とは、特定の条件を満たすことで、無許可で行うことができる」という文章を書くと、集めた「良い言葉」たちがページ下にずらっと並んでしまいます。それは意図するコンテキストとはズレています。

そういうときはページの書き換えです。先ほどの「引用」の一覧ページにて、ページのタイトルを別のものにします。ここでは「名言ノート」にしました。コンテキストを表すものとしてはこちらの方が合うでしょう。

<a href="https://rashita.net/blog/?attachment_id=29665" rel="attachment wp-att-29665"><img src="https://rashita.net/blog/wp-content/uploads/2019/11/screenshot-1-700x427.png" alt="" width="700" height="427" class="alignnone size-large wp-image-29665" /></a>

Scrapboxではページタイトルの書き換え時に、他のページに存在するページリンク（ハッシュタグも含む）も一緒に書き換えてくれる機能があるので、それを発動させれば一瞬で終わります。

で、書き換え作業が終わったあとに、もう一度#引用というハッシュタグを作って、それを覗いてみると、きちんとリンクが切れていることがわかります。

<a href="https://rashita.net/blog/?attachment_id=29666" rel="attachment wp-att-29666"><img src="https://rashita.net/blog/wp-content/uploads/2019/11/screenshot-2-700x378.png" alt="" width="700" height="378" class="alignnone size-large wp-image-29666" /></a>

で、これで万事OKかというと、若干気になる点は残ります。以下のページをご覧ください。

<a href="https://rashita.net/blog/?attachment_id=29668" rel="attachment wp-att-29668"><img src="https://rashita.net/blog/wp-content/uploads/2019/11/screenshot-4-700x499.png" alt="" width="700" height="499" class="alignnone size-large wp-image-29668" /></a>

集めた「良い言葉」の一つですが、Linksに「名言ページ」が表示されています。そしてその後に、名言の一覧が表示されています。なんとなく、このLinksが邪魔ですね。

で、なぜこんなことになっているかというと、先ほどページタイトルを書き換えたときに、「名言ノート」のページ（旧「引用」ページ）が実体化しているからです。この「実体化したページ」とは、薄い字でタイトルだけが表示されているページ<strong>ではない</strong>、ページのことです。そういうページへのリンクがあると、Links欄に表示されることになります。逆に言えば、実体化していないページへのリンクがあっても、それはLinks欄には表示されません。

ということで、、先ほど改タイトルした「名言ページ」を、ページメニューの「deleta this page」から削除してしまいます。もちろん、そのページを削除しても、既存ページに存在する「#名言ノート」が消えて無くなるわけではありません。きちんと残り、リンクとして機能します。

で、そういう状態にすると、以下のようにLinksからは消えてすっきりした状態になります。

<a href="https://rashita.net/blog/?attachment_id=29669" rel="attachment wp-att-29669"><img src="https://rashita.net/blog/wp-content/uploads/2019/11/screenshot-5-700x470.png" alt="" width="700" height="470" class="alignnone size-large wp-image-29669" /></a>

これはまあ細かいテクニックではありますが、Links欄に表示されるものと、そうでないものの違いは気に留めておくとよいでしょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank" rel="noopener noreferrer">amazlet</a> at 19.11.02</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 80,819<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
