---
title : 二冊目の電子書籍の製作手順（２）　〜Scrivener→「でんでんコンバーター」のちょっとしたコツ〜
link : 13506
date : Tue, 03 Jun 2014 02:35:15 +0000
categories : ["物書き生活と道具箱"]
tags : ["epub","scrivener","でんでんコンバーター","電子書籍"]
draft : false
author : 倉下忠憲
---

前回まで：

<a href="https://rashita.net/blog/?p=13496" target="_blank">二冊目の電子書籍の製作手順（１）　〜EPUBファイル作りの大きな流れ〜</a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg" alt="epubnised.003" width="500" height="376" class="alignnone size-full wp-image-13497" /></a>

今回は、Scrivenerからでんでんコンバーターへの流れを紹介します。

<H3>テキストファイルの準備</H3>

まずは、送り先の「<a href="http://conv.denshochan.com/">でんでんコンバーター</a>」から確認してみましょう。

ちなみに、ここからのお話は公式ページでも紹介されているので、そちらも参考にしてみてください。

<a href="http://conv.denshochan.com/tutorial" target="_blank">Tutorial チュートリアル</a>（でんでんコンバーター）

さて、でんでんコンバーターでEPUBファイルを作る場合、必要になってくるのがテキストファイル(.txt)です。ごくごく普通のプレーンなテキストファイル。
※文字コードは「UTF-8」推奨。

つまり、特別なツールを使わなくてもテキストエディタで原稿を書けば問題ありません。でも、Scrivenerを使っているのにもそれなりに理由があります。それは後ほど紹介するとして、まずはどのようなテキストファイルにすればよいのかを確認していきましょう。

でんでんコンバーターは、でんでんマークダウンに対応しています。マークダウンってなんじゃらほい？　という方もいらっしゃるでしょうが、原稿にかけるちょっとしたおまじない程度に認識してください。そのおまじないによって電子書籍になったときの見え方が変わってくるのです。

でんでんマークダウンの書き方については以下のページをご覧ください。

<a href="http://conv.denshochan.com/markdown" target="_blank">マークダウンの記法</a>（でんでんマークダウン）

上のページを丹念に読み込めればベストですが、さすがに厳しいでしょう。自分の原稿に必要そうなものだけをピックアップしてみてください。

私の場合であれば、「段落」「見出し」「ハイパーリンク」「改ページ」の4つを押さえればなんとかなりました。

特に重要なのが「見出し」です。

エッセイ集であれば、そのエッセイのタイトルが「見出し」にあたります。また章題なども「見出し」です。これが他の文章と同じスタイルだと、少々見づらいですね。あと目次上の問題もあるわけですが、ここではスルーしておきましょう。

ともかく普通に原稿を書いた後、見出しにあたる部分にマークダウンを当てていく作業が必要になります。

具体的には、

<blockquote>
エッセイのタイトル
</blockquote>

を

<blockquote>
## エッセイのタイトル
</blockquote>

に書き換えていくわけです。

こうすることによって、

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/20140603103928.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/20140603103928.png" alt="20140603103928" width="427" height="640" class="alignnone size-full wp-image-13509" /></a>

上記のようにタイトル部分がタイトル部分らしく表示されるようになります。たんに「表示される」以上の意味もあるのですが、それはまた回を改めて書きましょう。

<H3>Scrivenerのコンパイル機能</H3>

エッセイ集には全部で32編のエッセイが収められていたので、上のような書き換え作業を32回は行わなければいけません。32回ぐらいならなんとかなりますが、もし巨大エッセイ集で100編になるなら、この作業だけでもなかなか大変です。

そこで活躍するのがScrivenerのコンパイル機能。

Scrivenerは、ファイルをtxtなりpdfなりdocなりに出力できるのですが、その際、ちょっとした「付け足し」を自動的に行わせることができます。

具体例から入りましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot.png" alt="screenshot" width="245" height="349" class="alignnone size-full wp-image-13511" /></a>

これがエッセイ集の原稿プロジェクトです。ご覧のように全体が一つのフォルダに入っており、その下に各章のフォルダがあり、その中にそれぞれのエッセイデータが入っています。

各エッセイのデータはこんな感じ。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot1.png" alt="screenshot" width="500" class="alignnone size-large wp-image-13512" /></a>

ここには普通のテキストが入っています。さらにいうと、本文内にエッセイのタイトルは入っていません。しかし、完成品のエッセイ集にはエッセイの中にタイトルが入っています（少し上にある画像を確認ください）。

つまり、Scrivenerでコンパイルするときに、自動的にそのエッセイのタイトルを埋め込んだわけです。しかも「## 」付きで。

<H3>Formatting</H3>

これはコンパイルのFormattingを使用しました。対象としたいファイルレベルを指定し、「tittle」にチェックを付けて、「selection Layout」から「## 」（※）を追記します。これで完了。
※##の後には半角空白が入っていますので、ご注意ください。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot3.png" alt="screenshot" width="381" height="345" class="alignnone size-full wp-image-13514" /></a>
※こう入力すると

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot2.png" alt="screenshot" width="500" class="alignnone size-full wp-image-13513" /></a>
※こうなる

あとはコンパイルを完了させれば、各エッセイにそのタイトルが「## 」付きで入ったtxtファイルが完成というわけです。

同じように、改ページを入れたい箇所＿＿たとえば新しい章のはじまり＿＿には「=======================================」（※）といった記号を入れておきます。 
※やたら長いのは視認性をあげるため。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/screenshot4.png" alt="screenshot" width="500" height="281" class="alignnone size-full wp-image-13515" /></a>

これも同様にFormattingから指定できます。実にイージーですね。

<H3>さいごに</H3>

今回は、ScrivenerのFormattingを使った、「でんでんコンバーター」への対応を紹介しました。

この方法の良いところは、たとえば「## 」を後から「### 」に変えたくなっても、まったく手間がかからないことです。「selection Layout」に#を一つ打ち込めば、それで完了。

また、以前書きましたが、この「## 」を「（見出し）」に変えれば、かんたんEPUBにも対応させられます。グレイトですね。
※<a href="https://rashita.net/blog/?p=12662" target="_blank">Scrivener→「EPUB3::かんたん電子書籍作成」のちょっとしたコツ</a>

もちろん、そんなことは一切無視して、普通のテキストエディタでコツコツ##を追記していく方法でも可能です。手間さえ惜しまなければ、Scrivenerを使う必要はありません。そのあたりは、自分の環境を考えて判断してください。

次回は、実際にでんでんコンバーターでファイル変換するときのお話を紹介します。

次回：<a href="https://rashita.net/blog/?p=13520" target="_blank">二冊目の電子書籍の製作手順（３）　〜でんでんコンバーターを使う〜</a>