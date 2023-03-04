---
title : Scrapboxで、行頭の字下げを実現するCSS
link : 22843
date : Mon, 04 Sep 2017 02:39:28 +0000
categories : ["物書き生活と道具箱"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

Ulyssesの代替をいろいろ探していて、そうだScrapboxはどうだろう、と思い立ちました。クラウドですし、文章単位で管理できます。さらに、文章同士のリンク機能もあるので、Ulyssesとはひと味違った文章管理ができるかもしれません。

そこで、今進めている原稿群をScrapboxに移動してみたのですが、ちょっとしたトラブルが。

こういう原稿をそのままペーストすると、

<a href="https://rashita.net/blog/?attachment_id=22844" rel="attachment wp-att-22844"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-11-500x192.png" alt="" width="500" height="192" class="alignnone size-medium wp-image-22844" /></a>

以下のようになってしまいます。

<a href="https://rashita.net/blog/?attachment_id=22845" rel="attachment wp-att-22845"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-12-500x132.png" alt="" width="500" height="132" class="alignnone size-medium wp-image-22845" /></a>

バレット？

そうでした。Scrapboxでは、行頭にスペースを入れると、自動的にリストにしてくれるのです。入力の簡素化の面ではたいへんありがたいのですが、小説のように一文字下げる文章を扱うには不向きな機能と言えるでしょう。まあScrapboxは別に小説を管理するために生まれてきたわけではないのですから、そこはこちら側で工夫するしかありません。

いろいろ試した結果、以下のUerCSSを適用すれば、一文字字下げを表現できることがわかりました。

[css]
 .line-img { display: none }
 .line .dot {
       visibility:hidden !important;
      margin-right:1em !important;
    		}
  .indent {
         text-indent: 1em !important;
         margin-left:0px !important;
         }  
[/css]

※無事字下げが発生。バレットもありません。
<a href="https://rashita.net/blog/?attachment_id=22846" rel="attachment wp-att-22846"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-13-500x147.png" alt="" width="500" height="147" class="alignnone size-medium wp-image-22846" /></a>

むろん、これを適用してしまうと、今度はリストが使えなくなる点には注意です。

ちなみに、UserCSSの使い方は、以下のヘルプページをどうぞ。

<a href="https://scrapbox.io/help/UserCSS">UserCSS - Scrapbox ヘルプ - Scrapbox</a>

で、Scrapboxをエディタ的に使ってみた感想ですが、なかなか悪くありません。アウトライナーと同じように行単位の上下移動もショートカットキーから行えますし、個々のページをまとめるプロジェクトページ（リンク集のようなもの）も簡単に作れるので、小規模なもの、あるいは文章的構造を必要としないものなら大丈夫そうです。逆に、文章（ページ）の配置を自由移動できないので、Ulyssesとまったく同じ使い方は難しいでしょう。

後は、総文字数の表示と、目標文字数の設定なんかをJavaScriptで実現してみたいところです。