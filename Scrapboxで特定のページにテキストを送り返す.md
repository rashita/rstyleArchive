---
title : Scrapboxで特定のページにテキストを送り返す
link : 24824
date : Tue, 29 May 2018 01:18:31 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

何言っているのかちょっとわかんないと思いますので、簡単に説明を。

まず、以下のUserScriptがありました。

<a href="https://scrapbox.io/shokai/%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%AE1%E9%83%A8%E5%88%86%E3%82%92%E5%88%A5%E3%81%AE%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%AB%E5%88%87%E3%82%8A%E5%87%BA%E3%81%99UserScript">ページの1部分を別のページに切り出すUserScript - 橋本商会</a>

ページの一部分を切り出して、新規ページを作成するスクリプトです。ようするに、splitですね。で、これがメッチャ便利で、しかもScrapbox的な使い方に実にマッチしているんですが（とりあえず書いて、大きくなったら分割的な）、現在ではUserScriptではなく標準機能として取り込まれています。

で、人間ですので、splitを見かけたらmergeについても考えたくなります。mergeはあまりScrapbox的ではありませんが、Scrapboxの中で書籍の原稿を書いていたりすると、ちょっと欲しいかもと思ってしまうわけです。もし、splitとmergeの両方が可能ならば、これはもうすんばらしいことになるのでは？

しかし、テキストを選択して、送信先のページを選択するのは合理的ではありません。なにせページはたくさん存在しうるからです。そんなものの中からいちいち選択できません。

<strong>だったら、選択しなきゃいいのでは？</strong>

シナプスがつながりました。おなじスクリプトでいけることに気がついたのです。

もともとのスクリプトでは、一行目が新しいページタイトルとして使われます。であれば、その一行目を既存の、つまり送りたいページにすればいいのでは？

多少アレンジしたスクリプトでやってみると、こうなります。

※送りたいページ。
<a href="https://rashita.net/blog/?attachment_id=24825" rel="attachment wp-att-24825"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-23.png" alt="" width="1082" height="291" class="alignnone size-full wp-image-24825" /></a>

※送る内容が含まれたページ。
<a href="https://rashita.net/blog/?attachment_id=24826" rel="attachment wp-att-24826"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-24.png" alt="" width="1097" height="405" class="alignnone size-full wp-image-24826" /></a>

※送りたいページのタイトルを追加。

<a href="https://rashita.net/blog/?attachment_id=24827" rel="attachment wp-att-24827"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-25.png" alt="" width="1076" height="397" class="alignnone size-full wp-image-24827" /></a>

※テキストを選択し、「Append」を。
<a href="https://rashita.net/blog/?attachment_id=24828" rel="attachment wp-att-24828"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-26.png" alt="" width="1064" height="384" class="alignnone size-full wp-image-24828" /></a>

※無事追記された。
<a href="https://rashita.net/blog/?attachment_id=24829" rel="attachment wp-att-24829"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-27.png" alt="" width="1086" height="391" class="alignnone size-full wp-image-24829" /></a>

既存のスクリプトだと、いくつか情報が追加されてしまうので、多少改変を加えました。あと、送信した後のテキストも残るようになっています。この辺は消した方がいいのか、それとも、send とかの文言を追加した方がいいのかは、まだあんまり使っていないのでわかりません。

とりあえず、スクリプトは以下においておきます。

<a href="https://scrapbox.io/scrapboxlab/%E7%89%B9%E5%AE%9A%E3%81%AE%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%AB%E3%83%86%E3%82%AD%E3%82%B9%E3%83%88%E3%82%92%E9%80%81%E3%82%8A%E8%BF%94%E3%81%99">特定のページにテキストを送り返す - Scrapbox研究会</a>

もう一度言いますが、これはあまりScrapbox的ではありません。だって、オブジェクト指向で一つのクラスをどんどん大きくしていきましょう、みたいなことは言わないですよね。むしろ分割が強く意識されるはずです。で、Scrapboxも似たようなものなのですが、もしめちゃくちゃ小さな断片がたくさんあり、それらを後から統合したい場合なんかには使ってみてください。

あるいは、newPageによって分割した内容を戻したい場合は、一行目の「from 」部分を消してAppendを発動すればOKです。

<a href="https://rashita.net/blog/?attachment_id=24831" rel="attachment wp-att-24831"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-28.png" alt="" width="275" height="116" class="alignnone size-full wp-image-24831" /></a>

という意味合いも込めて、本記事のタイトルは「テキストを送る」ではなく「テキストを送り返す」になりました。

