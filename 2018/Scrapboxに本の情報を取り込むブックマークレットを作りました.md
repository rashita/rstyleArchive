---
title : Scrapboxに本の情報を取り込むブックマークレットを作りました
link : 24448
date : Thu, 12 Apr 2018 01:36:27 +0000
categories : ["0-知的生産の技術"]
tags : ["scrapbox","ブックマークレット","自作ツール"]
draft : false
author : 倉下忠憲
---

二つあります。

一つがメディアマーカーのページから取り込むもの。

	<ul><li><a href="https://scrapbox.io/thinkandcreateteck/%E3%83%A1%E3%83%87%E3%82%A3%E3%82%A2%E3%83%9E%E3%83%BC%E3%82%AB%E3%83%BC%E3%81%AE%E5%80%8B%E5%88%A5%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%8B%E3%82%89Scrapbox%E3%81%AB%E3%82%AF%E3%83%AA%E3%83%83%E3%83%97%E3%81%99%E3%82%8B%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88" title="メディアマーカーの個別ページからScrapboxにクリップするブックマークレット - 考えて、生み出す技術(TAC） - Scrapbox">メディアマーカーの個別ページからScrapboxにクリップするブックマークレット - 考えて、生み出す技術(TAC） - Scrapbox</a></li></ul>



メディアマーカーの「個別ページ」を開いて、ブックマークレットを発動すると取り込まれます。これはまあ、私がメディアマーカーを愛用しているから作ったツールです。

もう一つが、Amazonのページから取り込むもの。

	<ul>
<li><a href="https://scrapbox.io/thinkandcreateteck/Amazon%E3%81%8B%E3%82%89Scrapbox%E3%81%AB%E3%82%B9%E3%82%AF%E3%83%A9%E3%83%83%E3%83%97%E3%81%99%E3%82%8B%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88" title="AmazonからScrapboxにスクラップするブックマークレット - 考えて、生み出す技術(TAC） - Scrapbox">AmazonからScrapboxにスクラップするブックマークレット - 考えて、生み出す技術(TAC） - Scrapbox</a></li></ul>





上のページにも書きましたが、「<a href="https://yoshikiito.net/blog/archives/1325" title="Amazonの書籍商品ページからScrapboxに、書籍の画像付きページを作るブックマークレット | ひびテク">Amazonの書籍商品ページからScrapboxに、書籍の画像付きページを作るブックマークレット | ひびテク</a>」のコードを参考にさせていただきました。ありがとうございます。

<h2>ぜひどうぞ</h2>

さてさてさ〜て、ここからが本題です。

メディアマーカーの方はまったく私専用っぽいですが、Amazonの方は汎用性が高いだろうと判断しました。

で、<a href="https://twitter.com/scrasobox">まどべさん</a>が、

<a href="https://scrapbox.io/scrasobox/%E8%A6%8B%E3%81%9F%E3%81%BE%E3%82%93%E3%81%BE%E3%82%B9%E3%82%AF%E3%83%A9%E3%83%83%E3%83%97" title="見たまんまスクラップ - Scrapboxとあそぶ - Scrapbox">見たまんまスクラップ - Scrapboxとあそぶ - Scrapbox</a>

において、非常にユーザーライクにブックマークレットを提供されていたので、一念発起して私も真似してみました。ええ、半日仕事でしたよ。

<a href="http://honkure.net/tool/sandbox/bookmarklet01.html" title="bookmarkletメーカー">bookmarkletメーカー</a>

使い方は簡単です。プロジェクト名を放り込んで、「生成ボタン」をぽちっと。リンクが生成されるので、それをブックマークツールバーにでも放り込む。完了です。

<a href="https://gyazo.com/f8d7565e9dd89537f9590ec5a77ea8da"><img src="https://i.gyazo.com/f8d7565e9dd89537f9590ec5a77ea8da.gif" alt="https://gyazo.com/f8d7565e9dd89537f9590ec5a77ea8da" width="1000"/></a>

で、これを実際に使ってみると、

▼紙の書籍
<a href="https://gyazo.com/9049115e99aa0b3c0a1b99cc8b444804"><img src="https://i.gyazo.com/9049115e99aa0b3c0a1b99cc8b444804.gif" alt="https://gyazo.com/9049115e99aa0b3c0a1b99cc8b444804" width="960"/></a>

▼Kindle
<a href="https://gyazo.com/3fcbab86d23bf438abc97df49c3627b0"><img src="https://i.gyazo.com/3fcbab86d23bf438abc97df49c3627b0.gif" alt="https://gyazo.com/3fcbab86d23bf438abc97df49c3627b0" width="960"/></a>

と、無事どちらで動きます。

タイトルと表紙画像だけでなく、著者名や翻訳者名なども貼りつけられます。ついでに#本のハッシュタグも入ります。あと本のタイトルであることを明示するためにページタイトルには『』が入ります。

気に入らなければ、コードのそれっぽいところを削除してください。一応参考までに書いておくと、

タイトル:
title = '『'+ title +'』'

改行してハッシュタグ本:
'\n#本'

著者情報など:
pub.join(' ')

あたりをごにゃごにゃすればなんとかなると思います。

あと、MacのFirefoxとChromeでは動作確認しましたが、それ以外がまったくわかりませんので、あしからず。


それでは、楽しいScrapboxライフを。
