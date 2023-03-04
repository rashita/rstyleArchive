---
title : とりあえず、Feedlyの表示をカスタマってみた
link : 10938
date : Wed, 03 Jul 2013 22:59:06 +0000
categories : ["0-知的生産の技術"]
tags : ["feedly","情報摂取の作法"]
draft : false
author : 倉下忠憲
---

歯医者に連れて行かれる子どものように、嫌々な気分でGoogleリーダーからの乗り換え先を模索しています。

とりあえず、現段階でメインにしているのが「Feedly」。

ちょこっと触ってみて、「なんか使いにくいんだよな〜」と感じていました。「使いにくければ、カスタマイズすればいいじゃない」とアントワネットは言わなかったでしょうが、できる限りのことをやってみましょう。

今回は、Feedlyの表示回りのカスタマイズについてです。
<H3>違和感のもと</H3>まず最初に、感じた違和感について。

私のフィードは、以下のようにフォルダリング（フォルダー分けする、という動詞）されています。

<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot5.png" alt="screenshot" width="234" height="154" class="alignnone size-full wp-image-10939" /></a>

Newsはニュース系フィード、Sometimeは読んだり読まなかったり、Importantは読む率高い、Egosarchはその名の通りエゴサーチの結果です。

で、違和感を感じていたのは、どうもsometimeのフォルダ消化時にあるようです。たとえば、次のようにフィードが表示されるわけですが、

※フィード表示の例
<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot6.png" alt="screenshot" width="500" height="360" class="alignnone size-full wp-image-10940" /></a>

どうも、フィードを流し読みしているとき、私の視点は「発信元」を求めているようなのです。つまり、「どのブログの更新なのか」が気になるのです。

「気になる」というのは少し違うかもしれません。ある情報を読むかどうかを判断するときに、「発信元」が一つの鍵になっているというのが近いでしょう。ある意味では、タイトルよりも先に「発信元」をチェックしたいのです。

それは、「ここのブログの更新ならとりあえず読むでしょう（でも野球記事以外は）」みたいなことがあるということです。あるいは、その他のブログならば飛ばすけれども、「〜〜な５つ方法」というタイトルの記事を、普段書かないようなブログが書いていたらチェックする。そういう判断です。

しかし、Feedlyの表示だと、発信元の表記は非常に小さくなっています。このデザインはある種の思想の現れなのですが、その点については今回はスルーしておきましょう。

※発信元の表示が小さい
<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot-2.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot-2.png" alt="screenshot-2" width="500" height="360" class="alignnone size-full wp-image-10941" /></a>

ともかく、ここが違和感の素です。

逆に、チェックするときに発信元を気にせず、見出しだけで判断するNewsフォルダの消化はまったく違和感がありません。むしろスムーズなぐらいです。

<H3>プレファ</H3>「じゃあ、この発信元の表示を大きくできればいいんじゃね？」と思って、表示変更ボタンを探してみると「Preference」なる項目を発見。どうやら、ここからいろいろイジれそうです。

ざっと変更可能箇所を覗いてみるも、「発信元表示のフォントサイズを変更する」ことはできなさそう。その代わり、「Default View」で根本的な表示スタイルを変更できるようです。

※四つの選択項目
<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot7.png" alt="screenshot" width="407" height="151" class="alignnone size-full wp-image-10942" /></a>

それぞれの表示スタイルは

<strong>Titles Only (Google Reader) </strong>

<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot8.png" alt="screenshot" width="500" height="70" class="alignnone size-full wp-image-10943" /></a>

<strong>Magazine </strong>

<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot9.png" alt="screenshot" width="500" height="300" class="alignnone size-full wp-image-10944" /></a>

<strong>Cards </strong>

<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot10.png" alt="screenshot" width="500" height="320" class="alignnone size-full wp-image-10945" /></a>

<strong>Full Articles </strong>

<a href="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/07/screenshot11.png" alt="screenshot" width="500" height="260" class="alignnone size-full wp-image-10946" /></a>

という感じ。

「Magazine」は標準のもの。「Titles Only」だとGoogle Readerと同じように使えますね。が、今回は「Cards」を選択してみました。Evernoteのカードビューっぽい、というただそれだけの理由です。

とりあえず、しばらくこのビューで使ってみて、ダメだったら「Titles Only」にしましょう。

<H3>さいごに</H3>日常的な行為だと、その中に潜む差異は見えにくくなります。一度ツールを変えてみることで、その差異の手触りを発見できたりするのです。

今回は「発信元」という自分の中のフィルターに気がつくことができました。ようするに「誰かが書いているから読みたい情報」と「そんなことは気にならない情報」の二つがあるということです。

さらにTwitterなどのソーシャルメディアにまで視点を広げれば、「誰かが紹介しているから読みたい情報」も加わってきます。なかなか、ややこしいですね。

ともあれ、今回のカスタマイズで少しだけFeedlyとの距離が縮まりました。不思議なのですが、たとえそれがどのようなものであれ、少しでも「カスタマイズ」すると、ツールとの心理的距離が縮まることがあります。やはり愛着というのは、手間から生まれてくるのかもしれません。