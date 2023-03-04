---
title : Evernoteの標準機能としてぜひ欲しい「Add NoteLink」
link : 23337
date : Thu, 16 Nov 2017 22:00:55 +0000
categories : ["evernoteの使い方"]
tags : ["applescript","evernote"]
draft : false
author : 倉下忠憲
---

まず、状況の説明からいきます。その次に書いたコードを紹介します。

<h2>状況とニーズ</h2>

私は、「その年に読んだ本の一覧表」をEvernoteに作っています。一年分の日付を書き込み、その日に読了した本の名前を書き込む。それを続けていけば、「一年間の読了リスト」が年末には完成する、とあいなるわけです。

で、私は買った本についてはすべてメディアマーカー経由でEvernoteにノートを作っているので、その「読んだ本の一覧表」に書き込む書名は、単なるテキストでなく、本のノートのノートリンクにしたいと願うのは、別段人外の願望というものではないでしょう。

さて、その「読んだ本の一覧表」に記入するシチュエーションを想像してみましょう。

たとえば、朝起きて、「そうだ、昨日あの本読み終えたんだ。リスト更新しなきゃ」と思う。そう思ったら、最初にアクセスするノートは何でしょうか。そうですね。「読んだ本の一覧表」ノートです。で、そのノートに書名を記入しようとして、はっと思い出します。「そうだ、ノートリンクにしないと」

こうなると今度は、読み終えた本のノートが入っているノートブックに移動し、そこで対象のノートのノートリンクを取得して、再び「読んだ本の一覧表」に帰ってきて、該当箇所を探してそこにペーストすることになります。おわかりでしょうか。この面倒くささを。

しかも、そうして記入している間に、「そうだ、あの本もちょっと前に読んだんだった」とかなった日には、再びノートブックの往復作業が始まります。

これは、由々しき状態なのですが、「まあ、そういうもんだな」と長年諦めていました。

そう、Scrapboxに触れるまでは。

Scrapboxであれば、ノートの記入中であっても、別のノートへのリンクが簡単に書けます。記法があるだけなく、入力をサポートしてくれる機能すらあります。すいすいと快適に、ノート間のつながりを生み出してくれます。

そうした体験を一度してしまうと、その他のツールもこういう形であって欲しいと思うだけでなく、むしろこうあるべきなのではないか、という感覚すら強まります。簡単に言えば、ノートリンクを取得するためだけのノートブックの移動に嫌気がさしはじめた、ということです。

<h2>コードと動き</h2>

そこで、ちょっとしたAppleScriptを書いてみました。

<a href="https://rashita.net/blog/?attachment_id=23338" rel="attachment wp-att-23338"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-23.png" alt="" width="246" height="285" class="alignnone size-full wp-image-23338" /></a>

たとえば、このように日付の下に書名を入れたいとしましょう。そこで、スクリプトを起動します。すると、

<a href="https://rashita.net/blog/?attachment_id=23339" rel="attachment wp-att-23339"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-24.png" alt="" width="486" height="699" class="alignnone size-full wp-image-23339" /></a>

上記のようなダイアログが立ち上がります。特定のノートブックに入っている最近のノートから規定数分だけリストアップしたダイアログです。ここで、追加したい書名を選択してOKを押せば、

<a href="https://rashita.net/blog/?attachment_id=23340" rel="attachment wp-att-23340"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-25.png" alt="" width="252" height="128" class="alignnone size-full wp-image-23340" /></a>

上記のようにスルリとノートリンクが追加されます。この間、ノートブックの移動は一切ありません。ノート記入中にショートカットでスクリプトを立ち上げ、あとは必要なノートを選択するだけです。これはもう、名古屋弁で言えば、「どえりゃーべんり」な状況です。はい。

というか、なんで標準にこの機能がついていないのかちょっとわからないくらいです。

とは言え、最初にEvernoteのノートを「検索」するので、少し待たされますが、次回以降はノートの情報を使い回すので起動は速いです。もし、指定したノートブックにノートの増減があれば、また「検索」が発動して、やや待たされます。でもまあ、ノートブックを行ったり来たりすることに比べれば非常に快適です。

もう少しこのスクリプトを改良して、速度アップ＆利便性の向上に取り組みたいところですが、まずはその快適さをお伝えするために、記事に起こしてみました。とりあえず、現時点のコードは以下においておきます。

<script src="https://gist.github.com/rashita/c097530303ce1808bf6b9abb5fd30bb0.js"></script>


スクリプトの作成においては、「<a href="https://qiita.com/szk-3/items/ada884e10d4fe88eef2e" title="Cocoaの機能を使ってHTML文字列をコピーするAppleScriptハンドラ - Qiita">Cocoaの機能を使ってHTML文字列をコピーするAppleScriptハンドラ</a>」がたいへん参考になりました。というか、そのまま使わせていただきました。ありがとうございます。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.16</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 309<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>



