---
title : Scrapbox企画：第五回：Scrapboxのカスタマイズ
link : 23902
date : Sat, 10 Feb 2018 02:01:12 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox企画","scrapbox"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?attachment_id=23839" rel="attachment wp-att-23839"><img src="https://rashita.net/blog/wp-content/uploads/2018/02/scrapbox-1.png" alt="" width="250" height="100" class="alignnone size-full wp-image-23839" /></a>

<a href="https://rashita.net/blog/?p=23866" title="Scrapbox企画：第四回：Scrapboxの操作・入力法 – R-style">前回</a>は、入力方法について見てきました。これで、とりあえずは使えるようになると思います。

最後は、Scrapboxのカスタマイズについて紹介しておきましょう。

<h2>ブックマークレット</h2>

Scrapboxは、Webブラウザで作動するので、ブックマークレットが使えます。

まずは公式のものを。メニューから「Setting」に飛び「Page Date」タブを表示させると、一番上に「Bookmarklet」が出てきます。

で、この「Scrap to 〜〜」というのをブラウザのブックマークツールバーにドラッグすればOKです。後は取り込みたいWebページを表示させた状態でこのブックマークレットを発動させたら（クリックしたら、という意味です）、該当のプロジェクトにページが取り込まれます。

以下のようなアレンジバージョンもあります。

<a href="http://d.hatena.ne.jp/wineroses/20170320/p1" title="2017-03-20 - W&amp;R : Jazzと読書の日々">2017-03-20 - W&amp;R : Jazzと読書の日々</a>

画像付きで取り込まれるブックマークレットです。

他にもいろいろあるのですが、とりあえずは上記のような簡単なブックマークレットを押さえておけばOKでしょう。

ちなみにAPIについては以下を。

<a href="https://scrapbox.io/help-jp/API" title="API - Scrapbox ヘルプ - Scrapbox">API - Scrapbox ヘルプ - Scrapbox</a>

<h2>CSS</h2>

続いて見た目まわりのカスタマイズ。

ブラウザ拡張であれば「Stylish」などで見た目を変えることが可能ですが、Scrapboxでは直接改変が可能です。それを支えるのが「UserCSS」という仕組みなのですが、大きく二種類の書き方があります。

一つは、自分が閲覧するときだけに適用される書き方。もう一つは、管理者・編集者以外の閲覧者にも適用される書き方です。詳しくは以下をどうぞ。

<a href="https://scrapbox.io/shokai/UserCSS" title="UserCSS - 橋本商会 - Scrapbox">UserCSS</a>

自分ひとりのプライベートプロジェクトを使っている場合はどちらも差はありません。公開あるいは共有しているプロジェクトについて差が出てきます。

とは言え、違いはどこにCSSのコードを書くかだけです。

自分だけの場合は、「自分のページ」を作り、そこにcode:style.cssを記入すればOKです。他の人にも適用させたい場合は、「settings」という新規ページを作り、そこにcode:style.cssを書けばOKです。

復習すると、「自分のページ」とは、Scraoboxのアカウント名（Username）のページです。「rashita」というアカウントなら、以下が「自分のページ」となります。

<a href="https://rashita.net/blog/?attachment_id=23897" rel="attachment wp-att-23897"><img src="https://rashita.net/blog/wp-content/uploads/2018/02/screenshot-34.png" alt="" width="557" height="613" class="alignnone size-full wp-image-23897" /></a>

これはメニューの「Edit profile」からも確認できます。

<a href="https://rashita.net/blog/?attachment_id=23906" rel="attachment wp-att-23906"><img src="https://rashita.net/blog/wp-content/uploads/2018/02/screenshot-36.png" alt="" width="625" height="504" class="alignnone size-full wp-image-23906" /></a>

とりあえず、CSSページを書き込む場所以外は同じなので、ここではSettingsの方で実際例を見てみましょう。

<a href="https://scrapbox.io/rashitaactivity/settings">https://scrapbox.io/rashitaactivity/settings</a>

<a href="https://rashita.net/blog/?attachment_id=23907" rel="attachment wp-att-23907"><img src="https://rashita.net/blog/wp-content/uploads/2018/02/screenshot-37.png" alt="" width="802" height="458" class="alignnone size-full wp-image-23907" /></a>

<a href="https://rashita.net/blog/?attachment_id=23905" rel="attachment wp-att-23905"><img src="https://rashita.net/blog/wp-content/uploads/2018/02/screenshot-35.png" alt="" width="1209" height="546" class="alignnone size-full wp-image-23905" /></a>
※どちらも同じです。こちらは行頭からフォーカスを移動させた見え方。

こんな風に書いて、ブラウザをリロードすれば、CSSが適用されます。最初は他の人が使っているCSSをパクったり、アレンジしたりするのが良いでしょう。本格的にカスタマイズしたいなら、ブラウザの開発ツールなどでクラス名やIDを探る必要があります。

<h2>JavaScript</h2>

かなり似た仕組みで、JavaScriptを書くこともできます。こちらは「UserScript」と呼ばれています。

違いは、先ほども出てきた「Edit Profile」にある「Extensions」の設定項目をオン（Enabled）にしておくこと。

<a href="https://rashita.net/blog/?attachment_id=23908" rel="attachment wp-att-23908"><img src="https://rashita.net/blog/wp-content/uploads/2018/02/screenshot-38.png" alt="" width="647" height="666" class="alignnone size-full wp-image-23908" /></a>

そして、UserScriptに関しては、「settings」ページに書いて全体適用ができません。あくまで「自分のページ」に書いて、自分だけに効かせることオンリーです。

で、UserScrptも、JavaScriptがわからなければさっぱりなわけですが、他の人のScrapboxを覗いているといろいろ見つかります。

<a href="https://scrapbox.io/customize/" title="Scrapboxカスタマイズコレクション - Scrapbox">Scrapboxカスタマイズコレクション - Scrapbox</a>

<a href="https://scrapbox.io/scrasobox/" title="Scrapboxとあそぶ - Scrapbox">Scrapboxとあそぶ - Scrapbox</a>

<a href="https://scrapbox.io/shokai" title="橋本商会 - Scrapbox">橋本商会 - Scrapbox</a>

その他、誰かのScrapboxを訪れ、その人の「自分のページ」を見て回る、というのが実に「いい趣味」です。コピペ文化万歳ですね。

<h2>アプリ</h2>

純粋な意味でのカスタマイズではありませんが、公式以外のツールがあります。「Porter for Scrapbox」と「91958」です。

<div class="sticky-itslink"><a href="https://itunes.apple.com/jp/app/porter-for-scrapbox/id1305805708?mt=8&uo=4&at=Q0goZPzeHEw" rel="nofollow noopener noreferrer" target="_blank"><img src="http://is2.mzstatic.com/image/thumb/Purple118/v4/63/45/67/634567ab-a29a-19ed-500c-616b2867dfbd/source/60x60bb.jpg" style="border-style:none;float:left;margin:5px;" alt="Porter for Scrapbox" title="Porter for Scrapbox" ></a><div class="sticky-itslinktext"><a href="https://itunes.apple.com/jp/app/porter-for-scrapbox/id1305805708?mt=8&uo=4&at=Q0goZPzeHEw" rel="nofollow noopener noreferrer" target="_blank">Porter for Scrapbox</a><br>shunsuke senoo<br>価格： 0円<br><span style="font-size:xx-small;">posted with <a href="http://sticky.linclip.com/linkmaker/" target="_blank" rel="noopener noreferrer">sticky</a> on 2018.2.10</span></div><br style="clear:left;" ></div> 

<div class="sticky-itslink"><a href="https://itunes.apple.com/jp/app/91958/id1257585182?mt=8&uo=4&at=Q0goZPzeHEw" rel="nofollow noopener noreferrer" target="_blank"><img src="http://is2.mzstatic.com/image/thumb/Purple118/v4/2e/98/43/2e98434d-7289-4146-20da-5dea4f5ea3c2/source/60x60bb.jpg" style="border-style:none;float:left;margin:5px;" alt="91958" title="91958" ></a><div class="sticky-itslinktext"><a href="https://itunes.apple.com/jp/app/91958/id1257585182?mt=8&uo=4&at=Q0goZPzeHEw" rel="nofollow noopener noreferrer" target="_blank">91958</a><br>minimalab<br>価格： 0円<br><span style="font-size:xx-small;">posted with <a href="http://sticky.linclip.com/linkmaker/" target="_blank" rel="noopener noreferrer">sticky</a> on 2018.2.10</span></div><br style="clear:left;" ></div> 

前者はScraobox用クライアント、後者はメモ投稿用アプリという感じでしょうか。

もちろん、当たり前のようにScrapboxに情報があります。

<a href="https://scrapbox.io/porterapp/" title="Porter for Scrapbox オンラインヘルプ - Scrapbox">Porter for Scrapbox オンラインヘルプ - Scrapbox</a>

<a href="https://scrapbox.io/minimalab/91958%E3%81%AE%E3%83%98%E3%83%AB%E3%83%97" title="91958のヘルプ - minimalab - Scrapbox">91958のヘルプ - minimalab - Scrapbox</a>

iPhoneでScrapboxを激活用したい場合などは、使ってみてもよさそうです。
（注意：アンドロイドについては僕に聞かないでください。端末持ってないので）

<h2>さいごに</h2>

というわけで、拡張機能について簡単に触れてみました。

この辺については、話題が沼の様相を呈してくるので、深入りしてしまうとズブズブと書き続けてしまうので簡単に触れるに留めました。幸い、Scrapboxは他の人のUserCSSやUserScriptが閲覧できるので、ここでやいやい書くよりも、自分で探し回る方が「インターネット」的ですね。

さて、これでScrapboxについては一通り書けました。とりあえず書いてみて思ったのは、まだまだ書くことがある、ということです。特に、いろいろ細かい話、マニアックな話についてはすっ飛ばしてきたので、その辺は「Scrapbox企画」第二回か何かで書いてみたいと思います。

とりあえず、すごく楽しいツールなので、ぜひ皆さん触ってみてください。

では、では。