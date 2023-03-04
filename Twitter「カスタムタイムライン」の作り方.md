---
title : Twitter「カスタムタイムライン」の作り方
link : 11996
date : Thu, 05 Dec 2013 03:25:35 +0000
categories : ["0-知的生産の技術"]
tags : ["twitter","カスタムタイムライン"]
draft : false
author : 倉下忠憲
---

Twitterに「カスタムタイムライン」という機能があります。

名前の通り、自分でタイムラインを作れる機能で、現状は「TweetDeck」というクライアントツールから作成可能なようです。APIやらなんちゃらの話もありますが、１ユーザーには今のところ関係ないので、気になる方は下にあげた参考リンクの記事を読んで下さい。

「自分でタイムラインを作れる」というと、ぱっと思い浮かぶのが「<a href="http://togetter.com/" target="_blank">togetter</a>」。私もときどき使わせていただいております。ただしこれは日本語のツールなので、今回のTwitter公式機能とは少し切り分けて考えた方がいいかもしれません。

ともあれ、いろいろ言ったり・考えたりするのは実際に使ってみてからですね。
<H3>カスタムタイムラインの作成</H3>こちらはTweetDeckのブラウザ版。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot2.png" alt="screenshot" width="363" height="730" class="alignnone size-full wp-image-11997" /></a>

下の方にある歯車アイコンの上のリストっぽいボタンが「Custom timeline」です。ぽちっと。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot3.png" alt="screenshot" width="500" height="498" class="alignnone size-full wp-image-11998" /></a>

説明は不要でしょうが「Create custom timeline」で作成開始。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot4.png" alt="screenshot" width="324" height="754" class="alignnone size-full wp-image-11999" /></a>

まっさらなカラムが登場します。カラム内に書いてあるように、ここにツイートをドラッグすることで、取り込めます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/Pasted-Graphic.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/Pasted-Graphic.png" alt="Pasted Graphic" width="440" height="106" class="alignnone size-full wp-image-12001" /></a>

どんどん取り込んでいきましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot5.png" alt="screenshot" width="315" height="735" class="alignnone size-full wp-image-12000" /></a>



適当に、この原稿を書いているときにやりとりしたリプライを並べてみました（中身は気にしないでください）。ツイートはカラムに追加した順に並んでいきます（新規追加分が上にくる）。

並んでいるツイートの上にある「Add descriptiion」をクリックすれば、このタイムラインの説明を記入することができます。ただし160文字以内でお願いします。

カラム右上にある「設定」っぽいボタンから「Share」をクリックすると、このタイムラインのURLが確認できます。そう、これはWeb上に公開されるんですね。

（上のとは違って）真面目に作った奴だと、たとえば

<a href="https://twitter.com/rashita2/timelines/401176601456410624" target="_blank">仕事：自分のできることを、一生懸命すること</a>

こんな感じになります。

あと、Webページにタイムラインを埋め込むこともできるようです。

 <a class="twitter-timeline" data-dnt="true" href="https://twitter.com/rashita2/timelines/408418491817930752"  data-widget-id="408420427254341633">New Custom Timeline</a>
    <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>

<H3>どう使う？</H3>作成自体はとてもお手軽です。特に普段からTweetDeckを使っている人なら、外部ツールを起動させる必要がありません。

ただし機能面で言うと、やはりtogetterの方が少し上です。「時系列に整列」などがボタン1つで実行可能ですからね。また「何人に閲覧されたのか」というフィードバックが返ってくる点もtogetterは優秀です。総合的に考えれば、「日本人だったらtogetter使っておけばいいんじゃね？」という結論に達しそうですが、単純に言い切れない部分もあるでしょう。

たとえば、私はTwitterで「今日の一言」というのをつぶやいていますが、それをピックアップしたタイムラインを作るのは、カスタムタイムライン向きかもしれません。

<a href="https://twitter.com/rashita2/timelines/408421163275001856" target="_blank">Today's Word</a>

TweetDeckのカラムにドラッグすれば、すぐにTwitterのWebでも反映されるのがポイントです。TweetDeckでツイートして、それをそのままドラッグしてカスタムタイムラインに加える。こういう作業はtogetterだとちょっと面倒ですからね。

え？

ハッシュタグ使えばいいじゃん？

それはまあ、そうなんですが、たとえば「今日の一言」と「今日訓」（※以下参照）を一緒にまとめたタイムラインを作りたい、という場合にはこの方法が使えますね。一緒のハッシュタグを使っているわけでもありませんし。

<blockquote class="twitter-tweet" lang="ja"><p>今日訓 1034：記録がほぼそのまま計画に転用できるのは予行演習や模擬試験のことを考えればすぐにわかる。やってみて初めてわかることを次回に活かす。リハーサルで「ばみる」のも同様。 <a href="https://twitter.com/search?q=%23dailyremark&amp;src=hash">#dailyremark</a></p>&mdash; しごたの (@shigotano) <a href="https://twitter.com/shigotano/statuses/408370601892806657">2013, 12月 4</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

むろん、これをファボでやろうとすると、その他のファボツイートに紛れてしまうか、あるいはファボするものを限定する必要があります。それはそれでやっかいです。

TweetDeckでタイムラインを追い掛けて、誰かのダジャレツイートを見つけたら、即座にカスタムタイムラインに追加するなんて、ストーカー的使い方もできますね。

<H3>さいごに</H3>「ツイートのまとめ」としては、togetterで良いかと思いますが、こまかく追加していく使い方ならカスタムタイムラインもありではないでしょうか。

ただ、TweetDeckだけなのが、今のところやっぱりしんどいですね。他のクライアントでも、ユーザーをリストに追加できるみたいに、ツイートを指定したカスタムタイムラインに追加できるようになれば、もうちょっとこの機能も盛り上がるかもしれません。

<strong>▼参考リンク：</strong>
<a href="http://japan.cnet.com/news/service/35039817/" target="_blank">Twitter、カスタムタイムラインを発表--ユーザーによるタイムライン作成と共有を可能に</a>（CNET japan）

<a href="http://itpro.nikkeibp.co.jp/article/NEWS/20131113/517682/" target="_blank">Twitter、カスタムタイムラインの作成・共有を可能に</a>（ITpro）

<a href="http://headlines.yahoo.co.jp/hl?a=20131113-00000021-mycomj-sci" target="_blank">米Twitter、まとめページ機能「カスタム・タイムライン」を発表</a>（Yahoo!ニュース）

<a href="https://about.twitter.com/products/tweetdeck‎">TweetDeck</a>
