---
title : 二冊目の電子書籍の製作手順（１）　〜EPUBファイル作りの大きな流れ〜
link : 13496
date : Mon, 02 Jun 2014 02:04:21 +0000
categories : ["物書き生活と道具箱"]
tags : ["epub","pixelmator","scrivener","でんでんコンバーター","電子書籍"]
draft : false
author : 倉下忠憲
---

先日発売した以下の電子書籍。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E9%81%A0%E3%81%8F%E3%81%A6%E8%BF%91%E3%81%84%E5%A0%B4%E6%89%80%E3%80%81%E8%BF%91%E3%81%8F%E3%81%A6%E9%81%A0%E3%81%84%E5%A0%B4%E6%89%80-WRM-%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4%E9%9B%86-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00KNMMATO%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00KNMMATO" target="_blank">遠くて近い場所、近くて遠い場所 (WRM エッセイ集)</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E9%81%A0%E3%81%8F%E3%81%A6%E8%BF%91%E3%81%84%E5%A0%B4%E6%89%80%E3%80%81%E8%BF%91%E3%81%8F%E3%81%A6%E9%81%A0%E3%81%84%E5%A0%B4%E6%89%80-WRM-%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4%E9%9B%86-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00KNMMATO%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00KNMMATO" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41mp0tlw%2B6L._SL160_.jpg" border="0" alt="遠くて近い場所、近くて遠い場所 (WRM エッセイ集)" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />倉下忠憲  2014-05-29<br />売り上げランキング : 2039<br /><br /><br /><a href="http://www.amazon.co.jp/%E9%81%A0%E3%81%8F%E3%81%A6%E8%BF%91%E3%81%84%E5%A0%B4%E6%89%80%E3%80%81%E8%BF%91%E3%81%8F%E3%81%A6%E9%81%A0%E3%81%84%E5%A0%B4%E6%89%80-WRM-%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4%E9%9B%86-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00KNMMATO%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00KNMMATO" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

AmazonのKDPによるセルフパブリッシングです。

KDPはさまざまなファイルのアップロードに対応しているのですが、今回はEPUBファイルを選択しました。なんだかんだで定番ですし、多ストアへの展開（予定は未定）を考えるとやはりEPUBの選択が一番でしょう。

「でも、EPUBファイルの作成って難しいんじゃないですか？」

という方のために、上記の本を作った手順を記しておきます。一通りお読みいただいて「これならできるかも」と思われるか「やっぱ無理」と思われるかはわかりませんが、何かしらの参考にはなるでしょう。

話が長くなりそうなので、何回かの連載にわけます。最初に概要を説明し、その後細かい話へと移っていきます。とりあえず本稿だけでも読んでいただければ、EPUB作りの雰囲気は掴めるでしょう。

では、はじめます。

<H3>全体像</H3>

次の画像をご覧ください。全体の大まかな流れを示しています。

<a href="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2014/06/epubnised.003.jpg" alt="epubnised.003" width="500" height="378" class="alignnone size-full wp-image-13497" /></a>

<H4>原稿ファイル</H4>

まず、原稿ファイルはScrivenerで管理しました。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a4.mzstatic.com/us/r30/Purple4/v4/59/f5/79/59f57985-7c59-0b0c-48ba-cf8fc7bfd9e5/Scrivener.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store">Scrivener</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, 教育</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

今回の本は、過去のエッセイをまとめたものでしたので、Evernoteから過去原稿を探索し、必要なものをScrivenerに移しました。誤字脱字の修正などは、このScrivener上で行っています。

そうしてまとめあげた原稿を、Scrivenerのコンパイル機能からtxtファイルとして出力。これで、原稿データに関する部分はOKです。

<H4>表紙画像</H4>

表紙画像はPixelmator で作成。cover.jpgで出力しました。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a2.mzstatic.com/us/r30/Purple2/v4/3b/7f/10/3b7f10bd-509d-c34f-af91-f889be1814bd/AppIcon.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/pixelmator/id407963104?mt=12&uo=4&at=11l4y8" target="itunes_store">Pixelmator</a></strong></span><br><span class="appCategory">カテゴリ: グラフィック&デザイン, 写真</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/pixelmator/id407963104?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

<H4>EPUB化</H4>

そうして完成した二つのデータを、「<a href="http://conv.denshochan.com/">でんでんコンバーター</a>」にアップロードして、EPUBファイルに変換してもらいます。

一応この段階でEPUBファイルはゲットできるのですが、細かい部分に手を入れるために、もう少し手順を加えます。

でんでんコンバーターからダウンロードしたEPUBファイルをzip形式に変更し、一度解凍。そこで中に含まれているxhtmlファイルや、cssファイルをちょこちょこいじります。この辺りはHTMLやらなんやらの知識がないと若干お手上げです。そうして修正が完成したら、ふたたび圧縮をかけます。

EPUBファイルとして機能させるためには、少々特殊な圧縮が必要なのですが、それほど難しい作業ではありません。EPUB用の圧縮のツールも存在しています。が、私はMacのターミナルから2行ほどのコマンドを走らせて作業を終わらせました。

こうして完成したEPUBファイルを、KDPのサイトにアップロードすれば完成です。

細かい部分はかなり省略しましたが、おおよそこのような流れで電子書籍（EPUBファイル）を作成しました。

<H3>前作は？</H3>

ちなみに、エッセイ集シリーズ第一弾にあたる『赤魔導師の白魔法レベルぐらいまでは』もKDPであり、EPUBファイルを提出しました。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E8%B5%A4%E9%AD%94%E5%B0%8E%E5%B8%AB%E3%81%AE%E7%99%BD%E9%AD%94%E6%B3%95%E3%83%AC%E3%83%99%E3%83%AB%E3%81%90%E3%82%89%E3%81%84%E3%81%BE%E3%81%A7%E3%81%AF-WRM-%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4%E9%9B%86-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00ESDIAHU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00ESDIAHU" target="_blank">赤魔導師の白魔法レベルぐらいまでは (WRM エッセイ集)</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E8%B5%A4%E9%AD%94%E5%B0%8E%E5%B8%AB%E3%81%AE%E7%99%BD%E9%AD%94%E6%B3%95%E3%83%AC%E3%83%99%E3%83%AB%E3%81%90%E3%82%89%E3%81%84%E3%81%BE%E3%81%A7%E3%81%AF-WRM-%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4%E9%9B%86-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00ESDIAHU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00ESDIAHU" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41Zm5UR6rCL._SL160_.jpg" border="0" alt="赤魔導師の白魔法レベルぐらいまでは (WRM エッセイ集)" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />倉下忠憲  2013-08-25<br />売り上げランキング : 43451<br /><br /><br /><a href="http://www.amazon.co.jp/%E8%B5%A4%E9%AD%94%E5%B0%8E%E5%B8%AB%E3%81%AE%E7%99%BD%E9%AD%94%E6%B3%95%E3%83%AC%E3%83%99%E3%83%AB%E3%81%90%E3%82%89%E3%81%84%E3%81%BE%E3%81%A7%E3%81%AF-WRM-%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4%E9%9B%86-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00ESDIAHU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00ESDIAHU" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

その際は、Scrivenerから（txtではなく）EPUB出力し、sigilというツールを使ってそのファイルを編集しました。上で紹介した手順に比べると、かなり工程が減っています。が、この方法はあまりオススメできません。

Scrivenerやsigilで扱えるのが少し古いタイプの形式であるから、というのがその理由なのですが、テクニカルな話なのでそこは割愛します。とりあえず、作ったエッセイ集が横書きであり、ルビなどもまったく使わなかったので、「一応は問題なかった方法」と認知しておいてください。

もし、作りたい電子書籍が同じような形式であるならば、上記のツール（Scrivenerやsigil）を使ってEPUBファイルを作ることも「一応」できますし、まだ今のところはそのEPUBファイルでも「とりあえず」KDPにアップロードして電子書籍として販売できます。

<H3>さいごに</H3>

今回は、制作の大きな流れを紹介しました。

次回はScrivenerからでんでんコンバーターへの流れについて書いてみます。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">KDPではじめる セルフパブリッシング</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51XYQ5BxD0L._SL160_.jpg" border="0" alt="KDPではじめる セルフパブリッシング" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-12-21<br />売り上げランキング : 37105<br /><br /><br /><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>


