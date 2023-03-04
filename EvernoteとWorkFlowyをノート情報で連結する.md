---
title : EvernoteとWorkFlowyをノート情報で連結する
link : 16367
date : Sat, 11 Jul 2015 02:11:05 +0000
categories : ["evernoteの使い方","アウトライナーで遊ぼう"]
tags : ["evernote","workflowy"]
draft : false
author : 倉下忠憲
---

最初に背景を説明します。

私はEvernoteで原稿を管理しています。たとえば、メルマガで連載している企画の原稿などです。

<a href="https://rashita.net/blog/?attachment_id=16368" rel="attachment wp-att-16368"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot3-500x260.png" alt="screenshot" width="500" height="260" class="alignnone size-medium wp-image-16368" /></a>

一つのノートに、第一回から最新回までのすべての原稿がまとまっています。こうしておけば、「ちょっと前、何書いたかな？」を振り返るのが楽ですね。連載は続きものですから、過去原稿へのアクセスを良くしておくのは悪いものではありません。

しかし、連載に必要なのは原稿だけではありません。いわゆる「アイディア」なるものも必要です。構想・ネタ・使いたいフレーズなどなどですね。

そうしたものは、非常に暫定的・流動的な存在です。構想は変わるかもしれません。ネタは増えるかもしれません。使いたいフレーズは変貌するかもしれません。そういうものは、できれば、WorkFlowyで管理しておきたいところです。

<a href="https://rashita.net/blog/?attachment_id=16369" rel="attachment wp-att-16369"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot4-500x452.png" alt="screenshot" width="500" height="452" class="alignnone size-medium wp-image-16369" /></a>

これで「落ち着く場所」は定まりました。問題はその連結です。

<H3>落ち着きが悪い連携</H3>

WorkFlowyは、それぞれの項目に個別のURLが割り振られています。

そこからストレートに考えれば、このような連結が考えられます。

<a href="https://rashita.net/blog/?attachment_id=16370" rel="attachment wp-att-16370"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot5-500x346.png" alt="screenshot" width="500" height="346" class="alignnone size-medium wp-image-16370" /></a>

Evernoteのノートに、WorkFlowyの個別URLを書き込んでおくわけですね。一見これは問題ないように思えますし、実際問題はないのですが、どうにも気持ち悪さが残ります。

連載の原稿は、いわばText（本文）です。しかし、WorkFlowyの個別URLはTextではなくメタ情報です。つまり、上のような状態は、属性の違うものが、同一のフィールドに設置されているわけです。私が覚える気持ち悪さの原因がこれです。

<H3>メタはメタに</H3>

灰は灰に、本文は本文に、メタ情報はメタ情報に。

そのような分離を望むならば、もちろんメタ情報に埋め込んでしまえばよいわけです。なんといってもEvernoteではノートのメタ情報はユーザーの管理下にあります。

ノートの情報を開き＿＿ノートの右上にある「i」ボタンから開きます＿＿URLの欄に、先ほどの個別URLを入力。

<a href="https://rashita.net/blog/?attachment_id=16371" rel="attachment wp-att-16371"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot6-500x410.png" alt="screenshot" width="500" height="410" class="alignnone size-medium wp-image-16371" /></a>

<a href="https://rashita.net/blog/?attachment_id=16372" rel="attachment wp-att-16372"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot7-500x417.png" alt="screenshot" width="500" height="417" class="alignnone size-medium wp-image-16372" /></a>

すると、ノートの上部に小さなリンクが生まれています。これをポチッとすればWorkFlowyが開きます。実に小気味良い感じです。機能的にも見た目的にも申し分ありません。

※控え目なリンク表示
<a href="https://rashita.net/blog/?attachment_id=16373" rel="attachment wp-att-16373"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot8-500x114.png" alt="screenshot" width="500" height="114" class="alignnone size-medium wp-image-16373" /></a>

<H3>逆向きの連結</H3>

Evernote→WorkFlowyはわかった。では、その逆は？

という疑問があるかもしれません。私の作業環境のベースはEvernoteなので、Evernote→Workflowyの流れさえあれば問題ないのですが、そうではない人もいるでしょう。

一応、WorkFlowy→Evernoteの流れも＿＿Macならば＿＿確立できます。

<a href="https://rashita.net/blog/?attachment_id=16374" rel="attachment wp-att-16374"><img src="https://rashita.net/blog/wp-content/uploads/2015/07/screenshot9-500x333.png" alt="screenshot" width="500" height="333" class="alignnone size-medium wp-image-16374" /></a>

このように、一番上の項目のnoteにEvernoteのノート用のリンクを埋め込めばOK。ただし、Evernoteのようにスマートな見た目にまとまってくれません。わりにこのリンクの主張が激しいです。かといって下の方に移動すると利便性が落ちるので悩ましいところです。

もしnote欄をあまり使っていないのであれば、アドオンのstylishを使って文字サイズを変える手があります。あるいは、テキスト装飾のどれかをハックして、「文字サイズを小さくする」装飾を作っても良いかもしれません。あまり、スマートなやり方ではありませんが、方法としてはありえます。

<H3>さいごに</H3>

というわけで、EvernoteとWorkflowyの役割分担およびその接続方法でした。

『Evernote豆技50選』でも紹介しましたが、ノートのURL欄はハックしがいのある要素ですので、ぜひともいろいろ探求してみてください。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/Evernote%E8%B1%86%E6%8A%8050%E9%81%B8-Espresso-Books-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00VEEJ9XU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00VEEJ9XU" target="_blank">Evernote豆技50選 (Espresso Books)</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/Evernote%E8%B1%86%E6%8A%8050%E9%81%B8-Espresso-Books-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00VEEJ9XU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00VEEJ9XU" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" border="0" alt="Evernote豆技50選 (Espresso Books)" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />倉下忠憲  2015-03-29<br />売り上げランキング : 431<br /><br /><br /><a href="http://www.amazon.co.jp/Evernote%E8%B1%86%E6%8A%8050%E9%81%B8-Espresso-Books-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00VEEJ9XU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00VEEJ9XU" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

Enjoy your Evernote life!

<strong>▼参考リンク：</strong>

<a href="http://fluentlife.jp/evernote-link-convert/" target="_blank">[Evernote]ノートリンクをhttps型からevernote型に変換する方法(Win) – cliborの自動整形機能の活用 | 流れるような一日を</a>