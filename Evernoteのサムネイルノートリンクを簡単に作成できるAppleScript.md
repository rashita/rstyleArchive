---
title : Evernoteのサムネイルノートリンクを簡単に作成できるAppleScript
link : 7471
date : Wed, 22 Feb 2012 03:26:45 +0000
categories : ["物書き生活と道具箱"]
tags : ["applescript","evernote"]
draft : false
author : 倉下忠憲
---

どうも、こんにちはEvernoteマニアック研究会会長のRashitaです（嘘です）（二回目）。

Mac上でEvernoteをマニアックに使うためには、AppleScriptをある程度使える必要があります。

そのAppleScriptの個人的ししょーと仰いでいる<a href="https://twitter.com/#!/s_z_k_3">@s_z_k_3</a>さんが、<a href="https://rashita.net/blog/?p=7464">昨日のエントリー</a>に対して次のようなリプライをくださりました。

<blockquote class="twitter-tweet" data-in-reply-to="171830112742940675" lang="ja"><p>@<a href="https://twitter.com/rashita2">rashita2</a> これにピッタリなスクリプトがあったり…</p>&mdash; スズキさんさん (@s_z_k_3) <a href="https://twitter.com/s_z_k_3/status/171831184018505730" data-datetime="2012-02-21T05:38:41+00:00">2月 21, 2012</a></blockquote>
<script src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

ほほぅ・・・。

<blockquote class="twitter-tweet" data-in-reply-to="171831246652063744" lang="ja"><p>@<a href="https://twitter.com/rashita2">rashita2</a> 公開してないんですが、「 &lt;a href="ノートリンク"&gt;&lt;img src="ノートサムネール"&gt;&lt;/a&gt;」がクリップボードに入る感じです。ちょっと公開用に編集してきますε≡≡ﾍ( ´Д`)ﾉ</p>&mdash; スズキさんさん (@s_z_k_3) <a href="https://twitter.com/s_z_k_3/status/171832392242315265" data-datetime="2012-02-21T05:43:29+00:00">2月 21, 2012</a></blockquote>
<script src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

やだもう、私の使い方にぴったりじゃないですか〜、みたいなノリです。というか、そのスクリプトを自分で書こうと思っていたところです。

で、公開用に編集してくださったのが、こちら。

<blockquote class="twitter-tweet" data-in-reply-to="171834435061293056" lang="ja"><p>@<a href="https://twitter.com/rashita2">rashita2</a> とりあえずこれで→ <a href="http://t.co/qu6CH0oD" title="http://bit.ly/yuhRfD">bit.ly/yuhRfD</a> Evernoteで選択中のノートのサムネールつきリンクがクリップボードに入ります。適当にペーストしてください。画像サイズの変更等は、スクリプト中身の「HTMLTemplate」を変更です。</p>&mdash; スズキさんさん (@s_z_k_3) <a href="https://twitter.com/s_z_k_3/status/171840876279107586" data-datetime="2012-02-21T06:17:12+00:00">2月 21, 2012</a></blockquote>
<script src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
<br>
使い方は簡単。

サムネイルノートリンク（勝手に命名）を作成したいノートを選択し、スクリプトを実行するだけ。クリップボードに画像が入るので、それをノートに貼り付けるだけです。簡単でしょ。

複数のノートを選択した状態で実行すれば、複数のノートのサムネイルノートリンクが生成されます。いやはやすごい。

調子に乗って、遊んでみた図。

<a href="https://rashita.net/blog/wp-content/uploads/2012/02/window-grab2.png"><img src="https://rashita.net/blog/wp-content/uploads/2012/02/window-grab2.png" alt="" title="window-grab" width="500" height="435" class="alignnone size-full wp-image-7474" /></a>

一つ一つの画像をドラッグで移動させることができますし、画像をクリックすれば対象のノートに移動します。
※＜戻る＞ボタンで、元のノートに戻れます。

前回エントリーで紹介したような、Evernoteにストックした情報を使って発想を行う、という場合に効果を発揮しそうです。他にもいろいろな使い方がありそう。

<h3>ちなみに</h3>
ちなみに、EverWikiの以下のページでししょーが作成されたその他のスクリプトが公開されています。

<a href="http://everwiki.ogaoga.org/gao_nori">s_z_k_3's Scripts</a>

ついでに、宣伝しておくと、

<a href="http://szk3s-scripts-in.tumblr.com/">s_z_k_3's Scripts in Tumblr.com</a>

がししょーのブログです。ノートブック10万上限問題の記事でご存じの方も多いかも知れません。

<h3>さいごに</h3>
というわけで、便利なスクリプト＆ししょーの宣伝記事でした（ステマではありません）。

ちなみに、私もいくつかEvernote用のAppleScriptを作成しております。

「<a href="https://rashita.net/blog/?p=5376">Mac中にEvernoteにメモを送るためだけのアプリ『goEvernote』（仮）</a>」とか、「<a href="https://rashita.net/blog/?p=6777">Evernote小ネタ集vol.1</a>」をご覧くださいませ。

goEverとノートブック名を一括で変更するスクリプトは日々役に立っております。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 80875<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

