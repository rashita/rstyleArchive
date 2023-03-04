---
title : HTMLでEvernoteのノート・テンプレートを作る　第三回
link : 6338
date : Fri, 12 Aug 2011 04:39:41 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

連載ものです。過去のエントリーはこちら。

<a href="https://rashita.net/blog/?p=6327">HTMLでEvernoteのノート・テンプレートを作る　第一回</a>
<a href="https://rashita.net/blog/?p=6335">HTMLでEvernoteのノート・テンプレートを作る　第二回</a>

ここからHTMLのタグだとかCSSについて解説していこうと思っていましたが・・・

<!-- http://twitter.com/uma_blue/status/101508375271047170 --> <style type='text/css'>.bbpBox{background:url(http://a1.twimg.com/images/themes/theme3/bg.gif) #EDECE9;padding:20px;}</style><div id='tweet_101508375271047170' class='bbpBox' style='background:url(http://a1.twimg.com/images/themes/theme3/bg.gif) #EDECE9;padding:20px;'><p class='bbpTweet' style='background:#fff;padding:10px 12px 10px 12px;margin:0;min-height:48px;color:#000;font-size:16px !important;line-height:22px;-moz-border-radius:5px;-webkit-border-radius:5px;'><a href="http://twitter.com/rashita2" target="_new">@rashita2</a> 今更ですが、第１回で紹介されたテンプレートの１つを実際に作成する過程で説明していくHow to 形式だと、とっつきやすいかも...。作るの超面倒ですが。<span class='timestamp' style='font-size:12px;display:block;'><a title='Thu Aug 11 04:20:57 ' href='http://twitter.com/uma_blue/status/101508375271047170'>Thu Aug 11 04:20:57 </a> via <a href="http://www.echofon.com/" rel="nofollow">Echofon</a></span><span class='metadata' style='display:block;width:100%;clear:both;margin-top:8px;padding-top:12px;height:40px;border-top:1px solid #fff;border-top:1px solid #e6e6e6;'><span class='author' style='line-height:19px;'><a href='http://twitter.com/uma_blue'><img src='http://a1.twimg.com/profile_images/968250306/k8LZe_normal.jpg' style='float:left;margin:0 7px 0 0px;width:38px;height:38px;' /></a><strong><a href='http://twitter.com/uma_blue'>あおのうま</a></strong><br/>uma_blue</span></span></p></div> <!-- end of tweet -->

というコメントを頂いたので、そっちの方向にシフトします。ビバ、フレキシブル！

<h3>背景の色を変えたノート</h3>
今回は、背景色を変えたノートを作っていきます。

目標とするのは次のようなノート。サンプルでは色はピンクですが、もちろん自分の好みで選択できます。

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot31.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot31.png" alt="screenshot3" title="screenshot3" width="500" height="438" class="alignnone size-full wp-image-6340" /></a>

今回使うHTMLタグは＜DIV＞です。文字列なんかを追加するのに使えるブロック要素です。

ブロック要素って何か？という質問にはお答えしませんが、インライン要素とブロック要素というのがあるということは、頭の片隅にでも置いておくとよいかもしれません。同種のタグでは＜P＞というタグがあるのですが、こいつは要素の前後に勝手に改行を追加してしまうので、テンプレ作りにはあまり活用できません。

ノートの背景色を変えるには、HTMLの骨子に＜DIV＞を追加し、その背景色を変更すればOKです。

まずは、以下のようなコードを書いてみましょう。でもって拡張子を.htmlにして適当に名前を付けて保存し、それをブラウザで開きEvernoteにクリップします。

<pre>
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Pink&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div style="background-color:FFCCFF;"&gt;テスト&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

出来上がるのは、こんな感じのノートです。全然テンプレ風ではありませんが、まずはスタート。

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot4.png" alt="screenshot" title="screenshot" width="500" height="212" class="alignnone size-full wp-image-6341" /></a>

DIVでこっから文字列を始めますよ〜と宣言して、その中のstyleで装飾を指定しています。今回使ったのはbackgroud-colorという背景色を指定するスタイルシートです。

上に書いた"#"の部分が色の指定になっています。これはRGB指定と呼ばれるものです。他にも色の指定法はありますが、今回はこの方式で行きます。

RGBはそれぞれRed、Green、Blueの頭文字です。＃以降の文字列はRRGGBBというカンジで二つの文字でそれぞれの色を担当します。ちなみに、この文字列は16進数で、９の次がA（つまり１０を意味する）、Aの次がBで、一番大きいのがFという文字です。

なので、#FF0000というのは、純粋な赤色を、#0000FFは青色を意味します。#000000と書けば黒色、#FFFFFFは白色になります。この辺は「カラーチャート」というキーワードで、グーグル先生にお伺いを立てれば、好みの色をRGB指定に置き換えるのは難しくありません。

<h3>縦幅を拡大</h3>
上記のサンプルだと、あまりにも表示が寂しいので縦幅を拡大してみます。

<pre>
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Pink&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div style="background-color:FFCCFF;height:700px"&gt;テスト&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

heightというのが縦幅を指定する部分です。７００px（ピクセル）を指定していしてみました。これを保存して、ブラウザで読み込めば色つきの部分が伸びたものが表示されるはずです。

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot11.png" alt="screenshot1" title="screenshot1" width="500" height="263" class="alignnone size-full wp-image-6342" /></a>

ご覧のように、スタイルシートの要素と要素の間はは「;」で区切ります。また要素名とその指定の間は「:」で区切ります。プログラマーでない方は、これをよく間違える注意してください。
※ちゃんとしたHTMLエディタだったら入力補助が付いているとは思いますが。

以上で完成・・・なように見えますが、上のページをクリップしたノートに直接記入してみてください。改行を押すと、ものすごい下にまでカーソルが飛ぶと思います。完全に失敗です。

これが起きる内部的な理由の説明は割愛しますが、要するに上のやり方ではノートのテンプレとしては使えません。実際は次のようにします。

<pre>
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Pink&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div style="background-color:FFCCFF;height:700px"&gt;
&lt;div&gt;テスト&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

＜DIV＞タグの中にもう一つ＜DIV＞タグを入れる。このバージョンをブラウザで表示させ、クリップしてみてください。これだと問題無く記入できるはずです。

わざわざ回りくどい説明をしたのは、自作でノートテンプレを作る場合、この特徴を踏まえておくのがとても大切だからです。＜DIV＞タグなどの中で改行された場合、どうも同じタグを複製して追加するようです。この特徴を使った工夫もありますが、それはまた別の回に譲ります。

ちなみに、ある程度HTMLの知識がある人ならば、backbround-colorを＜Body＞タグに適用すればいいんじゃないのか、という疑問を持たれるかもしれませんが、残念ながらクリップ時に＜Body＞タグは華麗にスルーされる仕様なので、その方法は不可です。逆に言うと、＜Body＞タグの代わりになる＜DIV＞タグを作るということですが、まあこのあたりの話は別にいいですね。

<h3>画面一杯にする</h3>
上の色つき用紙のテンプレートで、とりあえずは完成ですが端の方に余白が空いてしまっていると思います。これがどうにもうっとうしいということならば、それを詰めることもできます。

<pre style="overflow: scroll; ">
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Pink&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div style="background-color:FFCCFF;margin-left:-8px;margin-top:-8px;width:102.5%;height:700px"&gt;
&lt;div&gt;テスト&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

実際の数字は、画面とか解像度とかで違ってくるかもしれませんので、適当に調整してください。marginというのは余白を指定するスタイルシートで、それをマイナス方向に（余白を詰めるように）指定してあります。右に詰めると逆に左部分が空いてしまうので、幅（width)を広げることで対応してあります。

<h3>さいごに</h3>
以上で、色つき用紙のテンプレートのできあがりです。

このテンプレを使うと、ビューをサムネイルにしたときにものすごく目立つノートができます。というか具体的な効果はそれだけかもしれません。
※サマリービューでは反映されない。

しかし、ノートの数が増えてくると、「ぱっと見て分かる」というのは強力なアドバンテージになることも確かです。自分の好きな色を使って、色つき用紙のテンプレートを作ってみるのも面白いかもしれません。
