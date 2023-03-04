---
title : 二冊目の電子書籍の製作手順（５）　〜mobiとazkのプレビュー方法〜
link : 13540
date : Fri, 06 Jun 2014 01:54:13 +0000
categories : ["物書き生活と道具箱"]
tags : ["azw","epub","kindleプレビュー","mobi","電子書籍"]
draft : false
author : 倉下忠憲
---

前回まで：
<a href="https://rashita.net/blog/?p=13496" target="_blank">二冊目の電子書籍の製作手順（１）　〜EPUBファイル作りの大きな流れ〜</a>
<a href="https://rashita.net/blog/?p=13506" target="_blank">二冊目の電子書籍の製作手順（２）　〜Scrivener→「でんでんコンバーター」のちょっとしたコツ〜</a>
<a href="https://rashita.net/blog/?p=13520" target="_blank">二冊目の電子書籍の製作手順（３）　〜でんでんコンバーターを使う〜</a>
<a href="https://rashita.net/blog/?p=13533" target="_blank">二冊目の電子書籍の製作手順（４）　〜zipとEPUBの行き来の注意点〜</a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg" alt="epubnised.003" width="500" class="alignnone size-full wp-image-13497" /></a>

いよいよ最終回。

前回でEPUBファイルが完成しました。今回は、そのプレビュー作業についてです。

<H3>EPUBファイルならiBooksでOKだが</H3>

確認したいファイルがEPUBなら、MacのiBooksで問題なく確認できます。

しかし、KDPは一筋縄ではいきません。

KDPにEPUBファイルをアップロードすると、mobiファイルという別の形式に変換されてしまうのです。EPUB形式で表示が問題無ければ、おおよそmobiでも大丈夫ですが完璧とは言えません。

さらにやっかいなのはiOS版のKindleアプリは、このmobiからさらにazkという別の形式に変換されます。これまたEPUBとまったく同じというわけにはいきません。それぞれの確認が必要です。

<H3>僕らの見方「Kindleプレビュー」</H3>

とりあえずmobiファイルを確認してみましょう。

といっても、ややこしいことは何もありません。Amazonが提供してくれている「Kindleプレビュー」というツールを使えば一発です。「Kindleプレビュー」は、以下のページから無料でダウンロードできます。

<a href="https://kdp.amazon.co.jp/help?topicId=A3IWA2TQYMZ5J6" target="_blank">KDPツールとリソース</a>（KDP）

このアプリを立ち上げると、次のようなウィンドウが立ち上がるので、ここに変換したいEPUBファイルをドロップすればOKです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot7.png" alt="screenshot" width="500" class="alignnone size-full wp-image-13541" /></a>

もしEPUBファイルに何も問題がなければ、mobiファイルに変換した上で、擬似的なプレビューを表示してくれます。ファイルに不具合があるならば、簡易的に警告も提示してくれます。

<H3>さらにiOS版も</H3>

上記の「Kindleプレビュー」で、表示を確認して「やれやれ、これで大丈夫」と安心してはいけません。擬似的なプレビューで確認できるのは、PaperWhiteとKindle Fire系だけです。iOS版はまた別なのです。

実際、今回作成した本もPaperWhiteでは問題なかったのに、iOS版で目次ページのリンクが機能していないという不可思議な事態に遭遇しました。あげくのはてに、読者さんからそれを指摘されるまで、私自身まったく気がついていなかった、という残念な状態でもありました（※）。
※現在発売されているものは、問題なく機能しています。

mobiからazkに変換されるときに、微妙な不具合が発生していたのでしょう。が、チェック不足であったことは確かです。

では、iOS版の表示を確かめるにはどうすればいいのかというと、これが少しだけ手間がかかります。

まず使うのは先ほども登場した「Kindleプレビュー」。

このアプリの「設定」を「iPhone用Kindle」に変えておきます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot8.png" alt="screenshot" width="331" height="196" class="alignnone size-large wp-image-13542" /></a>

そして、変換したいEPUBをドロップ。すると、mobiに変換した上で、さらにazkファイルに変換してくれます。

あとはこのファイルの中身を確認すればよいのですが、Macでは閲覧不可能です。ということで、iOSデバイスに転送が必要なのですが、Dropboxとかメールではなく、iTunesによるやりとりが必要です。

iTunesを立ち上げ、Appタブを選択して、Kindleアプリを選択。後はファイルの「追加」から、先ほど変換されたazwファイルを指定すれば、OKです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot9-1024x246.png" alt="screenshot" width="500" class="alignnone size-large wp-image-13543" /></a>

その後、iOS端末でKindleアプリを起動すると、先ほど送り込んだファイルが表示されるはずです。それをくまなくチェックしてください。

<H3>さいごに</H3>

というわけで、かなり駆け足でしたが、EPUBファイルの作成、カスタマイズ、そしてプレビュー方法について紹介してみました。

実のところ、あまり難しい作業はありません。ただただ手間がかかるだけです。もし、電子書籍を作ろうと計画を立てられているなら、作業時間は多めに見積もっておいた方がよいでしょう。

一応、しばらくはこのスタイルで制作を続けてみようと思います。「月刊くらした」計画終了後にこのスタイルがどのように変化しているのか。それも楽しみの一つではあります。

<strong>▼こんな一冊も：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">KDPではじめる セルフパブリッシング</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51XYQ5BxD0L._SL160_.jpg" border="0" alt="KDPではじめる セルフパブリッシング" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-12-21<br />売り上げランキング : 268791<br /><br /><br /><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

