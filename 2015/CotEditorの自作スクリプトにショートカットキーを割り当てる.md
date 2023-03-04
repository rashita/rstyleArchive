---
title : CotEditorの自作スクリプトにショートカットキーを割り当てる
link : 17135
date : Mon, 23 Nov 2015 01:30:03 +0000
categories : ["物書き生活と道具箱"]
tags : ["coteditor","iphoneipad"]
draft : false
author : 倉下忠憲
---

Macのテキストエディタは「CotEditor」を使っています。

<span class="appIcon"><img class="appIconImg" height="60" src="http://is4.mzstatic.com/image/thumb/Purple69/v4/de/63/96/de6396f7-5b0f-b334-6e41-522aee3705ce/source.icns/60x60bb.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/coteditor/id1024640650?mt=12&uo=4&at=11l4y8" target="itunes_store">CotEditor</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, 開発ツール</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/coteditor/id1024640650?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

基本的に便利に使えますし、また自作のAppleSciptを配置できるのもありがたいです。

たとえば、リスト項目を作り、自作の「ul」というスクリプトを実行すると、

<a href="https://rashita.net/blog/?attachment_id=17136" rel="attachment wp-att-17136"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot2.png" alt="screenshot" width="384" height="237" class="alignnone size-full wp-image-17136" /></a>

<a href="https://rashita.net/blog/?attachment_id=17137" rel="attachment wp-att-17137"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot3.png" alt="screenshot" width="364" height="254" class="alignnone size-full wp-image-17137" /></a>

自動的にリストのタグを付けられます。

あるいは、すべての行にPタグを付けてまわるのも、

<a href="https://rashita.net/blog/?attachment_id=17138" rel="attachment wp-att-17138"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot4.png" alt="screenshot" width="377" height="209" class="alignnone size-full wp-image-17138" /></a>

<a href="https://rashita.net/blog/?attachment_id=17139" rel="attachment wp-att-17139"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot5-500x194.png" alt="screenshot" width="500" height="194" class="alignnone size-medium wp-image-17139" /></a>

簡単にできます。

さらにこれを応用して、スタイルシート付きの縦書き表記を、

<a href="https://rashita.net/blog/?attachment_id=17140" rel="attachment wp-att-17140"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot6.png" alt="screenshot" width="427" height="252" class="alignnone size-full wp-image-17140" /></a>

<a href="https://rashita.net/blog/?attachment_id=17141" rel="attachment wp-att-17141"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot7.png" alt="screenshot" width="323" height="418" class="alignnone size-medium wp-image-17141" /></a>

ブラウザで確認する、なんてこともやってます。

で、これらは上部のスクリプトメニューから実行できるわけですが、この項目にショートカットを割り当てることができます。詳しくはCotEditorのヘルプを参照いただければよいのですが、簡単に言うとファイル名の拡張子にちょこちょこ小細工をすれば良いだけです。

<a href="https://rashita.net/blog/?attachment_id=17142" rel="attachment wp-att-17142"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot8.png" alt="screenshot" width="469" height="514" class="alignnone size-full wp-image-17142" /></a>

私の場合は、「全文をEvernoteにタグを付けて送信する」というスクリプトを一日に何回も起動するので、それにcontrol + command + Uのショートカット割り当ててあります。このUは、「Upload」の頭文字＿＿とかではなく、単にキー配置的に押しやすかっただけです。

<a href="https://rashita.net/blog/?attachment_id=17143" rel="attachment wp-att-17143"><img src="https://rashita.net/blog/wp-content/uploads/2015/11/screenshot9.png" alt="screenshot" width="199" height="35" class="alignnone size-full wp-image-17143" /></a>

こういうのは、本当にちょっとしたことなのですが、頻繁に行う動作であればあるほど、ショートカットキーでショートカットする効果というのは出てきます。それは数秒の時間が時短できるということではなく、むしろ脳の認知資源の節約の方に重点があるのでしょう。

というわけで、スクリプトを自作して使っている人はショートカットキーもご活用ください。それにしても、ヘルプはちゃんと読むべきですね。つい最近まで、この機能知りませんでした。
