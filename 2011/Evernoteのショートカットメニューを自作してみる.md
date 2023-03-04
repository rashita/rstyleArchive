---
title : Evernoteのショートカットメニューを自作してみる
link : 6974
date : Tue, 29 Nov 2011 02:55:32 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

以下のようなつぶやきを目にしました。

<!-- http://twitter.com/sawonya/status/140765854680887300 --> <style type='text/css'>.bbpBox{background:url(http://a0.twimg.com/profile_background_images/207268090/________mini_normal.png) #ebebeb;padding:20px;}</style><div id='tweet_140765854680887300' class='bbpBox' style='background:url(http://a0.twimg.com/profile_background_images/207268090/________mini_normal.png) #ebebeb;padding:20px;'><p class='bbpTweet' style='background:#fff;padding:10px 12px 10px 12px;margin:0;min-height:48px;color:#000;font-size:16px !important;line-height:22px;-moz-border-radius:5px;-webkit-border-radius:5px;'>ショートカットを備えているソフトは、ショートカット一覧へのショートカットメニューをメニューに用意しておいてくれよ！！といつも思う…<span class='timestamp' style='font-size:12px;display:block;'><a title='Sun Nov 27 12:16:09 ' href='http://twitter.com/sawonya/status/140765854680887300'>Sun Nov 27 12:16:09 </a> via <a href="http://www.tweenapp.org/" rel="nofollow">Tween</a></span><span class='metadata' style='display:block;width:100%;clear:both;margin-top:8px;padding-top:12px;height:40px;border-top:1px solid #fff;border-top:1px solid #e6e6e6;'><span class='author' style='line-height:19px;'><a href='http://twitter.com/sawonya'><img src='http://a3.twimg.com/profile_images/1449782004/_____normal.png' style='float:left;margin:0 7px 0 0px;width:38px;height:38px;' /></a><strong><a href='http://twitter.com/sawonya'>やまもとさをん</a></strong><br/>sawonya</span></span></p></div> <!-- end of tweet -->

<!-- http://twitter.com/sawonya/status/140767780541698050 --> <style type='text/css'>.bbpBox{background:url(http://a0.twimg.com/profile_background_images/207268090/________mini_normal.png) #ebebeb;padding:20px;}</style><div id='tweet_140767780541698050' class='bbpBox' style='background:url(http://a0.twimg.com/profile_background_images/207268090/________mini_normal.png) #ebebeb;padding:20px;'><p class='bbpTweet' style='background:#fff;padding:10px 12px 10px 12px;margin:0;min-height:48px;color:#000;font-size:16px !important;line-height:22px;-moz-border-radius:5px;-webkit-border-radius:5px;'>そもそもショートカットというのは「便利に使おうぜ機能」なはずで、「便利に使ってね★」って意味であるのであろうのに、その便利機能を便利に使ってもらうためのショートカットへのショートカットメニューがないというのは、便利機能のイイトコつぶしじゃないんかーぬぉー<span class='timestamp' style='font-size:12px;display:block;'><a title='Sun Nov 27 12:23:48 ' href='http://twitter.com/sawonya/status/140767780541698050'>Sun Nov 27 12:23:48 </a> via <a href="http://www.tweenapp.org/" rel="nofollow">Tween</a></span><span class='metadata' style='display:block;width:100%;clear:both;margin-top:8px;padding-top:12px;height:40px;border-top:1px solid #fff;border-top:1px solid #e6e6e6;'><span class='author' style='line-height:19px;'><a href='http://twitter.com/sawonya'><img src='http://a3.twimg.com/profile_images/1449782004/_____normal.png' style='float:left;margin:0 7px 0 0px;width:38px;height:38px;' /></a><strong><a href='http://twitter.com/sawonya'>やまもとさをん</a></strong><br/>sawonya</span></span></p></div> <!-- end of tweet -->

たしかにEvernoteのクライアントにはショートカットメニューがありませんね。普段よく使うものならともかく、全てを覚えておくというのは不可能でしょう。
※だからEvernoteを使っているわけです。

だったら、自分で作ってしまいましょう。「パンがなければ、ケーキを食べればいいじゃない」ばりに。

<h3>今回の目論見</h3>
実装の方法はいくつか考えられます。MacだったらApplescriptを使うのも一手です。

が、今回はEvernoteだけで完結させてしまいましょう。

使うのは、FavoriteBarです。

<a href="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot41.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot41.png" alt="screenshot4" title="screenshot4" width="468" height="200" class="alignnone size-full wp-image-6977" /></a>

ここにショートカットリストへのリンクを作ります。

つまり、

<ul>
	<li>Evernoteのノートでショートカットリストをつくる</li>

	<li>そのノートをFavoriteBarに入れる</li>

	<li>完成！</li>
</ul>



という手順です。

<h3>リストの作成手順</h3>
まずは、ショートカットのリストをゲットします。

<a href="http://jp.support.evernote.com/ics/support/DLSplash.asp?task=download" target="_blank">ダウンロード</a>（Evernote）

上のから、「Evernote for Mac ユーザーガイド (日本語)」のPDFがダウンロード。そこにショートカットの一覧が載っています。
※Windows版もあります。

これをそのままFavoriteBarに入れても良いのですが、ショートカットはページの最後の方にありアクセシビリティが悪いので、多少加工してショートカット部分だけを切り取ります。

どんな方法でもアリですが、私の場合はEvernoteのキャプチャー（shift + command + c）を使って、必要な部分を切り取り、一つのノートにまとめました。

後は適当な名前（Evernote for Mac ショートカットとか）をノートに付けて、FavoriteBarに放り込むだけ。

<a href="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot21.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot21.png" alt="screenshot2" title="screenshot2" width="500" height="340" class="alignnone size-full wp-image-6975" /></a>

<a href=" http://www.evernote.com/shard/s4/sh/9fc61838-5a4c-4d11-9ed5-0e42c9247dd8/218323867b04b0a02dba3b5635da356f" target="_blank">
http://www.evernote.com/shard/s4/sh/9fc61838-5a4c-4d11-9ed5-0e42c9247dd8/218323867b04b0a02dba3b5635da356f</a>

完成です。

<a href="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot13.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot13.png" alt="screenshot1" title="screenshot1" width="345" height="111" class="alignnone size-full wp-image-6976" /></a>


この方法以外にも、ブログなどからショートカットリストを公開している記事を探して、それをクリップし、不必要な部分を削除する、という方法でもいけるでしょう。

これで「あ、あれ何だっけ」となったときにショートカットリストを参照できます。
※ただし、ノートにアクセスするまでのスピードはPCのスペックに大いに依存すると思いますのであしからず。

<h3>似たような需要がありそう</h3>
もう一つ、Evernoteで忘れがちなのが、「検索演算子」ですね。

まったく先ほどのユーザーズガイドに検索演算子のリストもあるので、同様の手順で作成可能です。

<a href="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot31.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot31.png" alt="screenshot3" title="screenshot3" width="500" height="380" class="alignnone size-full wp-image-6978" /></a>

<a href="http://www.evernote.com/shard/s4/sh/f47c06b6-88f9-4bda-9e5f-41a7883f0b84/d1b8436acd1cd9896e4318191547a427" target="_blank">http://www.evernote.com/shard/s4/sh/f47c06b6-88f9-4bda-9e5f-41a7883f0b84/d1b8436acd1cd9896e4318191547a427</a>

完成。

<h3>さいごに</h3>
このように自分がアクセスしたい情報というのがわかってきたら、それをFavoriteBarに入れておくとなかなか便利です。

では、快適なEvernoteライフを。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 9515<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

