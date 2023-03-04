---
title : Evernoteの拡張ノートリンク（引用付き）スクリプトが！
link : 17304
date : Fri, 18 Dec 2015 02:27:33 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

以前、こんな記事を書きました。

<a href="https://rashita.net/blog/?p=16722">R-style » Evernoteにあったらアンビリバボーな機能３つ</a>

そうしたら、こんな記事が。

<del datetime="2015-12-19T02:08:51+00:00"><a href="http://szk3s-scripts-in.tumblr.com/post/135377161825/citation">citation - Evernoteに実装するアンビリバボーな機能 #2 - s_z_k_3's Scripts in Tumblr.com</a></del>

<a href="http://qiita.com/szk-3/items/3b98121720f766b8ea05">AppleScript - citation - Evernoteに実装するアンビリバボーな機能 #2 - Qiita</a>

Wow！

まずはやってみましょう。Mac版の話ですのであしからず。

適当なノートを開いて、コピーしたい部分を選択。

<a href="https://rashita.net/blog/?attachment_id=17305" rel="attachment wp-att-17305"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/screenshot10-500x309.png" alt="screenshot" width="500" height="309" class="alignnone size-medium wp-image-17305" /></a>

しかる後に、スクリプトを発動。んでもって、別のノートにペリッと貼り付け。

<a href="https://rashita.net/blog/?attachment_id=17306" rel="attachment wp-att-17306"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/screenshot11-500x213.png" alt="screenshot" width="500" height="213" class="alignnone size-medium wp-image-17306" /></a>

<a href="https://rashita.net/blog/?attachment_id=17307" rel="attachment wp-att-17307"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/screenshot12-500x225.png" alt="screenshot" width="500" height="225" class="alignnone size-medium wp-image-17307" /></a>

ばっちりです。コンテキストから日本経済新聞のノートを引用したのとまったく同じスタイルになっています。ノート名だけでなく、ノートブック名も表記されているのが、ワンポイントですね。

仮に、これをノートリンク＋コピーアンドペーストで実行したらこうなります。

<a href="https://rashita.net/blog/?attachment_id=17308" rel="attachment wp-att-17308"><img src="https://rashita.net/blog/wp-content/uploads/2015/12/screenshot13-500x346.png" alt="screenshot" width="500" height="346" class="alignnone size-medium wp-image-17308" /></a>

ダッサださですね。しかも、「ノートリンクをコピー→該当ノートに貼り付け→ノートに戻る→選択テキストをコピー→該当ノートに貼り付け」と、二倍以上のノート移動の手間がかかってしまいます。スクリプトなら、これが１回で済むわけです。まじビバ。

実際の設定方法などは、<a href="https://twitter.com/s_z_k_3">@s_z_k_3</a>さんの記事に書いてあるので、そちらをご覧ください。

とりあえず、スクリプトエディタ.appを開き、記事中のソースコードをまるっとコピペすればOKです。コンパイルしてエラーが出るなら、改行文字（"¬"）を消すと通るかと思います。

ちなみに、メニューバーに表示されるスクリプトメニューに自作のスクリプトを表示させる場合は、「ユーザ・スクリプト・フォルダ」に保存すればOKです。で、「ユーザ・スクリプト・フォルダ」は、スクリプトメニューから表示できますので、とりあえずは、スクリプトメニューの表示からですね。

あるいはコマンドランチャー系のツールでHOTキーに設定しておいても良いでしょう。それはそれでノート間の引用が捗りそうです。

