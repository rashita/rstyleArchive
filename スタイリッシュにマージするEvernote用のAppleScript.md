---
title : スタイリッシュにマージするEvernote用のAppleScript
link : 15322
date : Mon, 19 Jan 2015 02:50:38 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

さてMergeです。

MacのEvernoteでノートをマージすると、こうなります。

※マージ前
<a href="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot10-1024x370.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-15323" /></a>

※マージ後
<a href="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot11-1024x422.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-15324" /></a>

さほどビューティフルではありません。いささかのダサさが漂っています。せめて、ねずみ色のヘッダー部分はもう少しCoolに行きたいところ。

そこで、AppleScriptを書いてみました。

<H3> enmerge</H3>

<script src="https://gist.github.com/rashita/db220766dc6ae84d1188.js"></script>

β版ですが、とりあえずは動きます。
※できるだけ最新のMac及びEvernoteでご使用ください。

ノートを二つ以上選択して、スクリプトを起動。すると、

<a href="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot12.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot12-1024x429.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-15325" /></a>

こんな感じのノートが新規作成されます。It's Cool!.

ただし、通常のマージとの違いが二点。一つは、マージを適用したノートが削除されないこと。もう一つは、新規作成されるノートのタイトルが「マージしたノート」に固定されることです。

今後のバージョンアップで変更される可能性はありますが、まずは土台として一番シンプルな形で公開してみました。

<H3>さいごに</H3>

ちなみに、私はこれを「Evernoteコマンドランチャー」という別のスクリプトに登録し、そこから起動させています。

<a href="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot13.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/01/screenshot13.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15326" /></a>

このコマンドランチャー自体に、QuickSilverでHOTキーを割り当てているので、即座に各種スクリプトが起動できます。便利です。

では皆様もHappy Evernote Lifeを！

<strong>▼拙著：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 146709<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

