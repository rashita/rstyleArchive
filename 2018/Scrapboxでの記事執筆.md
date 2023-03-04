---
title : Scrapboxでの記事執筆
link : 24459
date : Fri, 13 Apr 2018 04:31:18 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

最近、Scrapboxで執筆できないかを実験中です。

その一環をご紹介。

<h2>init()</h2>

まず、その日のノートを作ります。デイリータスクリストみたいなものですが、ここでは簡易にデイリーノートと呼んでおきましょう。

で、そこに今から執筆を始めようと思う原稿のリンクを作ります。えっ、書き始める前にタイトルなんてわからない？　ですよね。ですから、企画名とか何かそういうものを当てます。で、リンクをクリック。

※仮で良い
<a href="https://rashita.net/blog/?attachment_id=24461" rel="attachment wp-att-24461"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-59.png" alt="" width="529" height="260" class="alignnone size-full wp-image-24461" /></a>

※リンクにする
<a href="https://rashita.net/blog/?attachment_id=24460" rel="attachment wp-att-24460"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-58.png" alt="" width="462" height="270" class="alignnone size-full wp-image-24460" /></a>

※リンクをクリック
<a href="https://rashita.net/blog/?attachment_id=24462" rel="attachment wp-att-24462"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-60.png" alt="" width="1051" height="256" class="alignnone size-full wp-image-24462" /></a>

さっそく執筆をスタートしましょう！……という前に、軽くメモを作ります。具体的に書くことは決まっていなくても、何か漠然としたアイデアとか方向性は見えているかもしれません。それを書きます。リンクにして。

※リンクを書けば
<a href="https://rashita.net/blog/?attachment_id=24470" rel="attachment wp-att-24470"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-67.png" alt="" width="501" height="62" class="alignnone size-full wp-image-24470" /></a>

※ページが出てくる
<a href="https://rashita.net/blog/?attachment_id=24463" rel="attachment wp-att-24463"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-61.png" alt="" width="1076" height="255" class="alignnone size-full wp-image-24463" /></a>

そうですね。そうすると、下に別のページが表示されますね。もしかしたら、そこで見つかったノートが何かヒントになるかもしれませんし、しれないかもしれません。ヒントになったらラッキー程度の感触で大丈夫でしょう。

あるいは、その原稿が何かしらの連載ならば、その連載名をハッシュタグとして添付してもいいでしょう。そうですね。そうすると、過去に書いた原稿が下に表示されます。昔書いたことがヒントになることもあるでしょう。うまくいけばもうけものです。

<h2>main()</h2>

あとは、本文を書いていきます。

ここは普通のエディタで書くのと一緒です。

ただ、文中に何かキーワードっぽいものが現れたら、それをリンクにすることで、これまた下にページが表示されます。それもヒントになるかもしれません。

あと、私はこのブログでは書籍を紹介するのですが、結構同じような本を取り上げます。で、そのたびごとにアフィリエイトリンクを作っていたのですが、単に書籍名を入力してそれをリンクにすれば、

<a href="https://rashita.net/blog/?attachment_id=24464" rel="attachment wp-att-24464"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-62.png" alt="" width="748" height="511" class="alignnone size-full wp-image-24464" /></a>

下にページが出てきますし、それをクリックすれば、ばっちりアフィリリンクが取得できますね。もちろん、事前にそういうページを作っているからできることですが、一度作っておけば、後からの再利用は簡単です。

<a href="https://rashita.net/blog/?attachment_id=24465" rel="attachment wp-att-24465"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-63.png" alt="" width="1081" height="668" class="alignnone size-full wp-image-24465" /></a>

というように、リンクを使うことで、過去に蓄積した情報へのアクセスルートが簡単に生まれる点がポイントです。ここで重要なことは「検索」という一手間が必要ないこと。同じページ上に表示されるので認識感覚における「移動」が発生しません。

ただ、別のページのデータを利用するためには、ページを「移動」する必要がある点は多少ネックです。ぜいたくかもしれませんが。

一応、Chromeを使っていて、<a href="https://scrapbox.io/customize/daiiz%E8%A3%BD%E3%81%AEChrome%E6%8B%A1%E5%BC%B5%E6%A9%9F%E8%83%BD" title="daiiz製のChrome拡張機能 - Scrapboxカスタマイズコレクション - Scrapbox">daiiz製のChrome拡張機能</a>をインストールしている場合は、そのページから移動することなく別のページのデータをコピーできるのですが、htmlタグが解釈されてしまうので、テンプレートの種類によってはうまく使えないこともあります。

<a href="https://rashita.net/blog/?attachment_id=24466" rel="attachment wp-att-24466"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-64.png" alt="" width="584" height="600" class="alignnone size-full wp-image-24466" /></a>

あと、私は生粋のFirefoxユーザーなのでそもそも無理ゲーです。

<h2>close()</h2>

とりあえず、そうして文章を書き上げたとしましょう。

すると、タイトルを決定する必要がありますね。

本文の中身合わせてタイトルを改変しましょう。そうですね。Scrapboxではタイトルを書き換えたら、それをリンクとして持つ別のページの中身もきちんと書き換えてくれます。

※こちらを変えれば
<a href="https://rashita.net/blog/?attachment_id=24467" rel="attachment wp-att-24467"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-65.png" alt="" width="941" height="468" class="alignnone size-full wp-image-24467" /></a>

※こちらも変わる
<a href="https://rashita.net/blog/?attachment_id=24468" rel="attachment wp-att-24468"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-66.png" alt="" width="481" height="238" class="alignnone size-full wp-image-24468" /></a>

だからこそ、最初にページを作るときは仮タイトルでよいのです。このフレキシブルさがいいですね。

で、書き終えた原稿については、キーワードなどをリンクにしておけばOKでしょう。もしかしたら、別の原稿のヒントになるかもしれないので。

もし、執筆中に総文字数が気になるなら、「<a href="https://scrapbox.io/scrasobox/%E8%A6%8B%E3%81%88%E3%82%8B%E6%96%87%E5%AD%97%E6%95%B0%E3%82%AB%E3%82%A6%E3%83%B3%E3%82%BF%E3%83%BC" title="見える文字数カウンター - Scrapboxとあそぶ - Scrapbox">見える文字数カウンター - Scrapboxとあそぶ - Scrapbox</a>」を導入してみるのもよいでしょう。右下の方にクールに総文字数を表示してくれます。

とりあえずは、こんなところで。