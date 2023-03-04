---
title : [Scrivener＋でんでんコンバーター]で各章の扉ページに画像を配置する
link : 14730
date : Sun, 02 Nov 2014 22:00:52 +0000
categories : ["scrivenerへの散歩道"]
tags : ["epub","scrivener","でんでんコンバーター","作り方","電子書籍"]
draft : false
author : 倉下忠憲
---

絶賛好評発売中の『Fount of Word -α-』には、珍しく画像が多用されています。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/Fount-Word-%CE%B1-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00OW20IWC%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00OW20IWC" target="_blank">Fount of Word -α-</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/Fount-Word-%CE%B1-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00OW20IWC%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00OW20IWC" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51bS5WgPBxL._SL160_.jpg" border="0" alt="Fount of Word -α-" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />倉下忠憲  2014-10-31<br />売り上げランキング : 977<br /><br /><br /><a href="http://www.amazon.co.jp/Fount-Word-%CE%B1-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00OW20IWC%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00OW20IWC" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

各章の扉ページに、こういった画像が配置されているのです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/20141102120616.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/20141102120616.png" alt="20141102120616" width="500" height="" class="alignnone size-full wp-image-14731" /></a>
※本書は、ぜひ画面を縦にしてお読みください。

で、<a href="http://conv.denshochan.com/" target="_blank">でんでんコンバーター</a>において画像の配置は以下のような記入を必要とします。

![代替テキスト](img.jpg)

こういう記入をしておくと、でんでんコンバーターが次のようなタグに変換してくれるわけです。

&lt;img src="img.jpg" alt="代替テキスト" /&gt;

※代替テキストは省略することも可能です。

さて、『Fount of Word -α-』は全部で40の章があります。ということは、章の扉ページも40個あります。そのそれぞれに、上のタグを書いていく……。悪夢ですね。

でも、Scrivenerなら大丈夫！（テレビの通信販売風）

<H3>Formatting Hack</H3>

使うのはCompileのFormatting。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14732" /></a>

この「Section Layout」を使うと、その文章のタイトル部分に細工ができます。先に結論を書いてしまうと、

![](word&lt;$n&gt;.png)

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot1.png" alt="screenshot" width="380" height="348" class="alignnone size-full wp-image-14733" /></a>

という風に書きます。ポイントは&lt;$n&gt;の部分。

これは一種の変数で、一回呼び出されるたびに数が一つ増えます。n++なわけです。

つまり、上のように書いておくと、第一章の扉ページの部分では、

![](word1.png)

となり、第二章・第三章では、

![](word2.png)
![](word3.png)

となるわけです。もちろんこれが40個続いてきます。

これでいちいち画像タグを書いていく必要はなくなりました。あとは、この連番に合わせて画像ファイルを作成すればOKです。

<H3>階層ズラし</H3>

が、このまま普通にやってしまうと、「おわりに」とか「著者プロフィール」のページにもこの画像タグが挿入されることになります。それはちょっと嫌ですね。

というわけで、階層を分けます。本文にあたる文章はフォルダの中に格納し、「おわりに」などは第一階層に置いておきます。もちろん、逆でも構いません。ともかく階層をズラすのがポイントです。

そうすると、

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot2.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14734" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot3.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14735" /></a>

というように、当てられるFormattingが変えられます。こうしてめでたく、本文の中だけに扉ページの画像タグを自動的に挿入することができました。

<H3>さいごに</H3>

もちろん画像ファイルを連番で作成する、という作業が若干面倒なわけですが、それはなんとかなるでしょう（大ざっぱ）。

ともかく、

<ul>
<li>Formattingでタイトルに細工</li>
<li>変数を活用</li>
<li>階層をズラす</li>
</ul>

という３つのテクニックを知っておくと、Scrivenerは界王拳3倍ぐらいすごくなりますのでぜひ覚えておいてください。

<strong>▼こんな一冊も：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">KDPではじめる セルフパブリッシング</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51XYQ5BxD0L._SL160_.jpg" border="0" alt="KDPではじめる セルフパブリッシング" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-12-21<br />売り上げランキング : 260412<br /><br /><br /><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>
