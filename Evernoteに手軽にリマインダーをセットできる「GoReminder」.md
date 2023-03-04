---
title : Evernoteに手軽にリマインダーをセットできる「GoReminder」
link : 14910
date : Mon, 24 Nov 2014 00:08:05 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

自作スクリプトです。Mac用。

「とにもかくにもリマインダーがセットしたいんだ」という強い要望（主に私の願望）に応えて作りました。

Evernote（for Mac）は、control + command + n でクイックノートの作成が可能なのですが、いかんせんリマインダーの設定ができません。でも、ちょっとしたタスクを即座に追加したいときもありますよね。

そこで、このアプリの出番です。

<H3>主な流れ</H3>

アプリを起動。

ダイアログが立ち上がるので、メモを入力して、リマインダーボタンをボチっと（リターンキーでもOK）。


<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot25.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot25.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14912" /></a>

Evernoteにリマインダーノートが登録される。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot26.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot26.png" alt="screenshot" width="463" height="386" class="alignnone size-full wp-image-14913" /></a>

以上です。

<ul>
<li>登録されるリマインダーは、リマインド日時がありません。</li>
<li>メモボタンを押せば、リマインダーなしのただのメモが登録されます。</li>
</ul>

QuickSilver経由でHOTキーに登録しておくと、抜群に便利になります。

<H3>コード</H3>

コードは以下。

<script src="https://gist.github.com/rashita/4b12415b48b70b1db6df.js"></script>

ver6.0以降で動くのは確認していますが、それ以前のversionはわかりませんのであしからず。

スクリプトエディタ・アプリ＿＿ユーティリティフォルダに入ってます＿＿を立ち上げ、上記をまるっとコピペして、実行ボタンを押して頂ければ、動作が確認できるでしょう。それをアプリケーションとして保存して、アプリケーションフォルダにでも置いてみてください。

<H3>さいごに</H3>

ver6.0になって、保存されているノートファイルの形式が結構変わっている印象があります。content.htmlがなくなり、note.xhtmlに変更されていたりとか。AppleScriptもちょこちょこ書き換えが必要っぽいですね。

他にもスクリプトは二、三ありますので、また紹介してみます。

では、皆様も楽しいEvernoteライフを！

<strong>▼拙著：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 190522<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>
