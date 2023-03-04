---
title : さっそく「でんでんエディター」を使ってEPUBを作ってみた
link : 12689
date : Fri, 14 Feb 2014 03:01:56 +0000
categories : ["物書き生活と道具箱"]
tags : ["でんでんエディター","でんでんコンバーター","電子書籍"]
draft : false
author : 倉下忠憲
---

ついに来ました。

<a href="http://densho.hatenablog.com/entry/dendeneditor" target="_blank">電子書籍の執筆ツール「でんでんエディター」を公開しました</a>(電書ちゃんねる)

拙著新刊でも紹介した「<a href="http://conv.denshochan.com/" target="_blank">でんでんコンバーター</a>」は、平のテキストファイルにちょちょいと細工をするだけで、EPUBファイルへと変換してくれるCoolなツールなんですが、いかんせんその「ちょちょいと細工」で躓いてしまう人もいます。

実際の難しさではなく、「難しそう」という感じだけで敬遠されてしまうのです。特に、マークアップ式の文章に慣れていない人であればなおさらでしょう。そこには無視できない壁が、たしかに存在しています。

「でんでんエディター」は、その壁を乗り越えるツールになってくれそうです。

<H3>概要</H3>使い方は、とても簡単。

【でんでんエディター】: <a href="http://edit.denshochan.com/">http://edit.denshochan.com/</a>

にアクセスするだけ。

すでにサンプル用の文章が入力されていますので、それを見れば細かい解説は必要ないでしょう。

<H4>4つのモード</H4>エディタは大きく４つのモードがあります。

<ul>
	<li>「Edit」</li>
	<li>「Preview」</li>
	<li>「Code」</li>
	<li>「Custom CSS」</li>
</ul>

「Edit」は文章を入力する場所、それを「Preview」で確認できます。「Code」は実際に生成されるコードが表示され、「Custom CSS」ではオリジナルのCSSを入力することができます。が、この辺りは触らなくてもOK。

※Edit
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot23.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot23-1024x651.png" alt="screenshot" width="500" height="320" class="alignnone size-large wp-image-12694" /></a>

※Preview
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot24.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot24.png" alt="screenshot" width="500" height="447" class="alignnone size-large wp-image-12695" /></a>

※Code
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot25.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot25.png" alt="screenshot" width="500" height="369" class="alignnone size-large wp-image-12696" /></a>

※Custom CSS
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot26.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot26.png" alt="screenshot" width="500" height="358" class="alignnone size-large wp-image-12697" /></a>

まずは「Edit」で入力→「Preview」で確認、という流れだけ押さえておきましょう。

<H4>入力サポート</H4>「Edit」では、でんでんマークダウン方式のサポートが用意されています。

レベル６までの「見出し」、斜体(em)と太字(storng)の「強調」、ルビ（ruby）、リンクの挿入(a)、画像の挿入(img)。これらはすぐ使えるようにエディタ上部にボタンが配置されています。また、右サイドバーにも入力補助のボタンが準備されていますが、こちらは「準備中」。

もちろん入力補助を使わなくても、サンプルのテキストを参考にしたり、「<a href="http://conv.denshochan.com/markdown" target="_blank">でんでんマークダウン</a>」のページをちらちら見ながら直接書くことも可能です。ただ、シンプルな小説であれば、すでに実装されているボタンだけでも結構いけるはずです。おそらくブログ感覚で作業を進めていけるでしょう。それ以外の文章であれば、「引用」の表記（※）だけ覚えておけば対応できそうです。
※これもサンプルの文章にあります。

こうした入力補助を使いながら、文章を完成させたら「ファイルに保存」ボタンをポチリ。テキストファイルをダウンロードするか、自分のDropboxに保存するかが選択できます。

ちなみに、画像の挿入もDropboxのフォルダから可能なようです。

<H3>やってみた</H3>「細けぇ話はいいんだよ。実際の使い勝手はどうなんだ？」

という自分の奥の方にある声に従って、EPUBファイルを作ってみました。

ごくシンプルなテキストを入力し、軽くマークダウンを使って、しかるのちにテキストファイルをダウンロード。それをさらに「<a href="http://conv.denshochan.com/" target="_blank">でんでんコンバーター</a>」にアップ、という流れです。変換されたEPUBファイルの確認はiBooksで行いました。

あと、テキストだけだと寂しいので、頭に表紙っぽい画像も入れてみます。

「でんでんエディター」で入力し、
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot19.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot19.png" alt="screenshot" width="500" height="451" class="alignnone size-full wp-image-12690" /></a>

「でんでんコンバーター」にテキストファイルをアップ。
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot20.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot20-1024x534.png" alt="screenshot" width="500" height="250" class="alignnone size-large wp-image-12691" /></a>

iBooksで表示。
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot21.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot21-1024x771.png" alt="screenshot" width="500" height="370" class="alignnone size-large wp-image-12692" /></a>

問題ありません。マークダウンで指定したルビもちゃんと振られていました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot22.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot22.png" alt="screenshot" width="493" height="453" class="alignnone size-full wp-image-12693" /></a>

難しい操作はどこにもありません。プレビューで確かめながら作業を進められるのもよいですね。

<H3>さいごに</H3>「使う人が難しいことを考える必要がない」

というツールの存在は、その対象が普及していく上で重要だと思います。

パソコン周りの知識は格差が激しく、ある人にとっては空気のように当たり前のことでも、別の人にとっては宇宙人語検定一級ぐらいの近寄りがたさがあります。

その点、「でんでんエディター」＋「でんでんコンバーター」は、ブログを更新できる人ならば、EPUBファイルにたどり着くことができそうです。

<strong>▼告知:</strong>
2月17日に、八重洲ブックセンターさんで以下の新刊に関するブックセミナーを行います。

電子書籍の最初の一歩を踏み出せていない方はぜひご来場ください。参加料は無料ですが、事前に登録が必要ですのでご注意ください。

<a href="http://www.yaesu-book.co.jp/events/talk/2919/" target="_blank">倉下忠憲さん講演会　「セルフ・パブリッシングの最初の一歩」</a>

<a href="https://rashita.net/blog/?p=12536" target="_blank">[告知] 2月17日に八重洲ブックセンター本店さんで新刊イベントを行います</a>