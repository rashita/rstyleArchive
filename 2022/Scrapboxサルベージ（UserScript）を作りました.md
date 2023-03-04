---
title : Scrapboxサルベージ（UserScript）を作りました
link : 30923
date : Sat, 26 Mar 2022 09:17:20 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox","userscript"]
draft : false
author : 倉下忠憲
---

以前、自作のUserScriptを紹介しました。

<a href="https://rashita.net/blog/?p=25829">ScrapboxからWorkFlowyへのブリッジング</a>

この改造版がドドンと登場です。

<a href="https://scrapbox.io/rashitamemo/Scrapbox%E3%82%B5%E3%83%AB%E3%83%99%E3%83%BC%E3%82%B8%EF%BC%88UserScript%EF%BC%89">Scrapboxサルベージ（UserScript） - 倉下忠憲の発想工房</a>

以前のものはハッシュタグページ（ページの中身がないページ）で使用するものでしたが、こちらは中身がある通常ページで使えます。そのページからリンクしているページの本文を取得し、まとめたテキストとして表示してくれます。

つまり、あるテーマに応じたページをいくつもまとめるページを作っておけば、その中身を一覧できるようになるわけですね。

（以下のページで実行）

<a href="https://rashita.net/blog/?attachment_id=30925" rel="attachment wp-att-30925"><img src="https://rashita.net/blog/wp-content/uploads/2022/03/0e71c7508a98ab18e127ef6225c07045-700x468.png" alt="" width="640" height="428" class="alignnone size-large wp-image-30925" /></a>

（以下のような出力）

<a href="https://rashita.net/blog/?attachment_id=30926" rel="attachment wp-att-30926"><img src="https://rashita.net/blog/wp-content/uploads/2022/03/f4af5f5163a26b8a6c9d2d3fb9f89978-700x605.png" alt="" width="640" height="553" class="alignnone size-large wp-image-30926" /></a>

使い方としては、「自分のページ」に上記ページのscript.jsをコードブロックごとコピペし、さらにページをリロードして、UserScriptを読み込めば、右側のメニューに「リンクページ取得ボタン」が表示されると思います。あとは、それをポチッと押すだけです。

ただし、「関連ページ」を取得するUserScriptも一緒に入れていると微妙に動作してくれません。同じ名前の関数があるからなのですが、その場合はどちらかの関数を消すか、あるいは一旦「関連ページ」の方のUserScriptを消してしまう手があります。

いっそのこと、両方の機能を持っていて、自動的に切り替わるようなScriptに改造してしまうのがよいのですが、とりあえずはこのままにしておきましょう。ある程度は使えるはずです。

<p style="text-align: center;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" target="_blank" rel="noopener noreferrer" name="amazletlink"><img class="aligncenter" style="border: none;" src="https://m.media-amazon.com/images/I/51yMZ+QU40L._SY346_.jpg" alt="" /></a></p>