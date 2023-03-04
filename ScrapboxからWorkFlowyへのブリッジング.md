---
title : ScrapboxからWorkFlowyへのブリッジング
link : 25829
date : Thu, 11 Oct 2018 02:16:21 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox","workflowy"]
draft : false
author : 倉下忠憲
---

将来を見据えて、ちょっとだけ準備しておきました。

<a href="https://scrapbox.io/scrapboxlab/%E9%96%A2%E9%80%A3%E3%83%9A%E3%83%BC%E3%82%B8%E3%82%92%E4%B8%80%E6%B0%97%E3%81%AB%E5%8F%96%E5%BE%97%E3%81%99%E3%82%8BUserScript">関連ページを一気に取得するUserScript - Scrapbox研究会</a>

たとえば、Scrapboxに以下のようなページがあったとしましょう。

<a href="https://rashita.net/blog/?attachment_id=25830" rel="attachment wp-att-25830"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-30.png" alt="" width="1157" height="542" class="alignnone size-full wp-image-25830" /></a>

中身は空っぽで、linkedをたくさん持つページ。いわゆるタグ（ハッシュタグ）的なページです。ずらりと関連ページが並びます。

<a href="https://rashita.net/blog/?attachment_id=25831" rel="attachment wp-att-25831"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-31.png" alt="" width="1157" height="775" class="alignnone size-full wp-image-25831" /></a>

で、Scrapboxに書いたものは、基本的にScrapboxで読んでもらうのが一番だという認識もありながら、ここに書き留めたものからツリー構造物（つまり、本）を作りたくなるときが訪れるかもしれません。そのとき、1ページずつ開いてコピペしていく、というのは、そうですね。地獄ですね。

というわけで、その作業を簡略化するのが冒頭で紹介したUserScritpです。

<h2>使い方</h2>

ハッシュタグページを開いた状態で、ページメニューの「関連ページ取得」ボタン（ランダムボタンの下）をポチッと押します。

<a href="https://rashita.net/blog/?attachment_id=25832" rel="attachment wp-att-25832"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-32.png" alt="" width="255" height="239" class="alignnone size-full wp-image-25832" /></a>

そして、温かいお茶を入れてそれを啜ります。おせんべいなんかをポリポリやってもいいかもしれません（意：かなり長く待たされます）。

しばらくすると、新しいウィンドウがオープンします。

<a href="https://rashita.net/blog/?attachment_id=25833" rel="attachment wp-att-25833"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-33.png" alt="" width="1046" height="783" class="alignnone size-full wp-image-25833" /></a>

この中身を全文選択→コピーしたのち、WorkFlowyの適当な場所にペースト。

<a href="https://rashita.net/blog/?attachment_id=25835" rel="attachment wp-att-25835"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-35.png" alt="" width="956" height="717" class="alignnone size-full wp-image-25835" /></a>

はい、見事に移動できました。

一応変換時の処理として、

・[]（ブラケット）を削除します
・各ページについているおおもとの#hashtag（上の例なら情報摂取の作法）を削除します

という二つの工程が入っています。スクリプトをいじれば、削除しないようにすることもできます。逆に、おおもとだけでなくあらゆるハッシュタグも削除させられますが、その辺は、個人的なオプションには想定されていないので、コードには入っていません。頑張ってカスタマイズしてください。

<h2>さいごに</h2>

どう考えても、使用頻度は非常に低いスクリプトです。

地道にScrapboxでリゾームを成長させ、一定の規模になったらそれを整える為にWorkFlowyに移動させる。そのような収穫祭のときにのみ活躍します。よって、こういうのもあったな、くらいに覚えていただけば幸いです。ぜんぜん日常的な用途ではありませんので。

あと、テキストの処理次第では、付箋系ツールに読み込ませられる形になるかもしれません。そういうニーズもどこかにはあるでしょう。まあ、今の所の私にはありませんが。

もちろん、私が使っているのがWorkFlowyなだけで、Dynalistでも同じようにペーストして使えます。他のアウトライナーでもできるものは多いでしょう。

Scrapboxで育てて、WorkFlowyで整える。そういう流れのブリッジングになれば幸いです。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.10.11</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 15,662<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
