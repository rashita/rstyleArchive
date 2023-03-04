---
title : Evernoteのメールによるノート作成が無くなって困っているなら
link : 15954
date : Fri, 01 May 2015 06:13:41 +0000
categories : ["evernoteの使い方"]
tags : []
draft : false
author : 倉下忠憲
---

先日紹介したとおり、Evernoteに新しいプランが登場しました。

それに伴っていくつか変更があり、スタンダードプランから「メールによるノート作成」の機能がなくなりました。使う人はわりと便利に使っていたので、残念なところです（プラスとプレミアムにはあります）。

そんなときにはライフハッカーの心得第五条「迂回路を探せ」ですね。

ようはメールを送信して、Evernoteのノートが作成できれば良いわけですから、あのツールの登場です。そう、IFTTTですね。

IFTTTについては、以下をどうぞ。

<ul>
<li><a href="https://rashita.net/blog/?p=12150" target="_blank">EvernoteとIFTTTのおさらい（１）　〜IFTTTとは何か〜</a></li>
<li><a href="https://rashita.net/blog/?p=12228" target="_blank">EvernoteとIFTTTのおさらい（２）　〜トリガーとアクション〜</a></li>
<li><a href="https://rashita.net/blog/?p=12242" target="_blank">EvernoteとIFTTTのおさらい（３）　〜アクションの中身〜</a></li>
<li><a href="https://rashita.net/blog/?p=12267" target="_blank">EvernoteとIFTTTのおさらい（４）　〜Twitterとのレシピ〜</a></li>
<li><a href="https://rashita.net/blog/?p=12315" target="_blank">EvernoteとIFTTTのおさらい（５）　〜他のWebツールのレシピ〜</a></li>
</ul>

<H3>シンプルなやり方</H3>

一番シンプルな方法は、「Gmailの受信箱にメールが入ってきたら、メールの本文を使ってEvernoteにノートを新規作成する」でしょう。これで、ほぼ理想の機能が手に入ります。

トリガーは、Gmailの「Any new email in inbox」で、アクションはEvenroteの「Create a note」。レシピを作ると、初期設定ではこのようになっています。

<a href="https://rashita.net/blog/wp-content/uploads/2015/05/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/05/screenshot.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15955" /></a>

仮に、次のようなメールを受信すると、

<a href="https://rashita.net/blog/wp-content/uploads/2015/05/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/05/screenshot1.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15956" /></a>

Evernoteにこんなノートが作られます。

<a href="https://rashita.net/blog/wp-content/uploads/2015/05/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/05/screenshot2.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15957" /></a>

日時や送信元が必要なければ、レシピの設定を変えましょう。本文(bodyplain)だけにもできます。

<H3>アレンジバージョン</H3>

普段Gmailを使っておらず、Evernoteに送信するためだけのアカウントとして運用するならば、このままのレシピでも問題ありません。

しかし、Gmailが普段使いなら、受信箱に入ったメールがすべてEvernoteにノート化されてしまいます。正気の沙汰ではありません。Evernote転送用に別のアカウントを作る手もありますが、その場合は通常のレシピが使えなくなります。残りの手としては、トリガーを変えることです。

「Any new email in inbox」ではなく、「New email in inbox from」を使い、普段自分が送るであろうメールアドレスを登録しておけば、メール→Evernote転送として十分機能します。複数のアドレスが想定されるなら、複数のチャンネルを作ればOkです。

<H3>さいごに</H3>

拙著『Evernote豆技50選』でもちらっと紹介しましたがEvernoteとIFTTTの相性は最高ですので、ぜひともIFTTTの使い方は覚えておきましょう。

他にもいろいろなことができますので。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/Evernote%E8%B1%86%E6%8A%8050%E9%81%B8-Espresso-Books-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00VEEJ9XU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00VEEJ9XU" target="_blank">Evernote豆技50選 (Espresso Books)</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/Evernote%E8%B1%86%E6%8A%8050%E9%81%B8-Espresso-Books-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00VEEJ9XU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00VEEJ9XU" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" border="0" alt="Evernote豆技50選 (Espresso Books)" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />倉下忠憲  2015-03-29<br />売り上げランキング : 65<br /><br /><br /><a href="http://www.amazon.co.jp/Evernote%E8%B1%86%E6%8A%8050%E9%81%B8-Espresso-Books-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00VEEJ9XU%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00VEEJ9XU" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>
