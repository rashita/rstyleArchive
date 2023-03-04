---
title : いっそのこと出版社名もScrapboxに取り込んでしまうブックマークレット
link : 26075
date : Mon, 05 Nov 2018 00:00:29 +0000
categories : ["scrapboxの用法"]
tags : ["amazon","scrapbox","ブックマークレット"]
draft : false
author : 倉下忠憲
---

先日「<a href="https://rashita.net/blog/?p=26063">内容紹介を含めてAmazon書籍ページからScrapboxに取り込むブックマークレット</a>」という記事を書いたら、反応を頂けました。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">ありがとうございます！！<br>ものすごくありがたいです。<br>これ、出版社とかISBNも入るようにするのって、難しいですか？</p>&mdash; yoshinon@情報管理LOG (@yoshinon) <a href="https://twitter.com/yoshinon/status/1058814885197271040?ref_src=twsrc%5Etfw">2018年11月3日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

「難しいか、簡単か」と問われれば、「若干面倒そう」という気持ちになるくらいの難易度です。やってやれなくはないな、という見通しが立つ程度。

というわけで、実際に書いてみたのですが、少し問題もありますので、ゆっくりいきましょう。

<h2>動作確認</h2>

まずコードですが、以下のページにあります。

<a href="https://scrapbox.io/rashitamemo/ISBN%E3%82%84%E5%87%BA%E7%89%88%E7%A4%BE%E3%81%AE%E6%83%85%E5%A0%B1%E3%82%82%E5%8F%96%E3%82%8A%E8%BE%BC%E3%82%80%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88">ISBNや出版社の情報も取り込むブックマークレット - 倉下忠憲の発想工房</a>

で、動作ですが、Amazonの書籍ページで発動すると、こういう感じのページをScrapboxに作成します。

<a href="https://rashita.net/blog/?attachment_id=26076" rel="attachment wp-att-26076"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-20.png" alt="" width="1100" height="619" class="alignnone size-full wp-image-26076" /></a>

前のバージョンとの違いは、出版社名、出版年月日、ISBNコードが入っていることです。

で、Kindle版はISBNではなくASINなのでですが、それもばっちり対応済みです。

<a href="https://rashita.net/blog/?attachment_id=26085" rel="attachment wp-att-26085"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-27.png" alt="" width="1091" height="616" class="alignnone size-full wp-image-26085" /></a>

で、セルフパブリッシングだと版数とかも表示されていたりするのですが、それも無事取り込めました。

<a href="https://rashita.net/blog/?attachment_id=26078" rel="attachment wp-att-26078"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-22.png" alt="" width="1080" height="622" class="alignnone size-full wp-image-26078" /></a>

で、セルフパブリッシングだと出版社名が欠落しているものもあるのですが、それはASIN番号だけの取り込みとなります。

<a href="https://rashita.net/blog/?attachment_id=26079" rel="attachment wp-att-26079"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-23.png" alt="" width="1084" height="638" class="alignnone size-full wp-image-26079" /></a>

さらに途中のコードをいじれば、簡単に出版年月にもリンクを付けられるようにしてあります。

<a href="https://rashita.net/blog/?attachment_id=26080" rel="attachment wp-att-26080"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-24.png" alt="" width="453" height="162" class="alignnone size-full wp-image-26080" /></a>

これでおおむねのニーズには対応できたかと思います。

<h2>コードが長すぎた問題</h2>

が、しかし、紙だとかKindleだとか出版社名のありなしとかで条件分岐しているので、ずいぶんコードが長くなってしまいました。たぶん、普通にやるとブックマークレットの文字数制限にひっかかりそうな勢いです。つまり、そのまま登録してもダメっぽい感じです。

だったら、どうするか。

もちろん、逃げ道はあります。

少し技術的な話になりますが、ブックマークにコードを直接登録するのではなく、「ここにあるコードを読み込んでね〜」という指定だけしておいて、実際のコードは別の場所に置いておくのです。

では、そのコードはどこに置くか？

ええ、そうですね。Scrapboxですね。

Scrapboxは、

https://scrapbox.io/api/code/$projectname/$pagetitle/script.js

というようなURLを叩けば、そのページ内にあるコードブロック記法の中身を返してくれます。この場合だと、code:script.jsブロック内に書かれているコードが返ってきます。それを利用すればいいわけです。

そこでまず、自分のプロジェクトにページを作ってください。面倒なら「<a href="https://scrapbox.io/rashitamemo/ISBN%E3%82%84%E5%87%BA%E7%89%88%E7%A4%BE%E3%81%AE%E6%83%85%E5%A0%B1%E3%82%82%E5%8F%96%E3%82%8A%E8%BE%BC%E3%82%80%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88">ISBNや出版社の情報も取り込むブックマークレット</a>」を丸々コピペでも、OKです。必要な情報だけにするなら、一番下にあるcode:script.jsブロックだけコピーしてください。
※最後の方にあるScrapboxのプロジェクトのURLは自分のものに書き換えてください。

<a href="https://rashita.net/blog/?attachment_id=26081" rel="attachment wp-att-26081"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-25.png" alt="" width="1012" height="743" class="alignnone size-full wp-image-26081" /></a>

これで準備OKです。

あとはこのページのコードを読み込むためのブックマークレットの作成です。それは以下のページを参考にしてください。

<a href="https://scrapbox.io/rashitamemo/Scrapbox%E3%81%AE%E3%82%B3%E3%83%BC%E3%83%89%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E3%81%8B%E3%82%89JavaScript%E3%82%92%E8%AA%AD%E3%81%BF%E8%BE%BC%E3%82%80%E3%82%88%E3%81%86%E3%81%AB%E3%81%99%E3%82%8B">ScrapboxのコードブロックからJavaScriptを読み込むようにする - 倉下忠憲の発想工房</a>

一応書いておくと

<code>javascript:(function(d,s){s=d.createElement('script');s.src='https://scrapbox.io/api/code/ここにプロジェクト名/ここにページタイトル/script.js';d.body.appendChild(s);})(document)</code>

という形です。もちろんこのままコピペしてもダメですよ。先ほどのページのURLをガッチャンコと埋め込んでください。

あとは、Amazonページでそのブックマークレットを発動させれば、ページのクリップが進みます。

<a href="https://scrapbox.io/thinkandcreateteck/%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88%E3%81%AE%E4%BD%9C%E3%82%8A%E6%96%B9">ブックマークレットの作り方 - 考えて、生み出す技術(TAC）</a>

<h2>年月リンクの切り替え方</h2>

最後に年月リンクの設定だけ確認しておきましょう。

年月リンクをごにゃごにゃしているのはコードの以下の部分です。

<a href="https://rashita.net/blog/?attachment_id=26082" rel="attachment wp-att-26082"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-26.png" alt="" width="816" height="97" class="alignnone size-full wp-image-26082" /></a>

デフォルトでは「年月をリンクに」になっています。もしリンクなしか、年だけリンクにしたい場合は、該当行の頭にある//を削除し、デフォルト行の行頭に//を追加してください。それでリンク表記が切り替わります。

<h2>さいごに</h2>

いささかマニアックな感じになってしまいましたが、とりあえずこれで書誌データはずいぶん拡充したと思います。

[2018年11月5日10:54 追記]
いちおうブックマークレットに直接追加できるようのバージョンも用意しておきました。<a href="https://scrapbox.io/rashitamemo/ISBN%E3%82%84%E5%87%BA%E7%89%88%E7%A4%BE%E3%81%AE%E6%83%85%E5%A0%B1%E3%82%82%E5%8F%96%E3%82%8A%E8%BE%BC%E3%82%80%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88">ISBNや出版社の情報も取り込むブックマークレット</a>のscript_min.jsがそれです。上の設定が面倒な場合は、とりあえずこちらをブックマークレットに放り込んでみてもよいでしょう。

では、楽しいScrapboxライフを。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.11.04</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 13,606<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
