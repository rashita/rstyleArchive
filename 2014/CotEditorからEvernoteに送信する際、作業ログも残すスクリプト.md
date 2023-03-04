---
title : CotEditorからEvernoteに送信する際、作業ログも残すスクリプト
link : 13866
date : Sat, 19 Jul 2014 01:24:05 +0000
categories : ["evernoteの使い方"]
tags : ["applescript","coteditor","evernote"]
draft : false
author : 倉下忠憲
---

ほとんど全ての原稿を<a href="http://coteditor.github.io/" target="_blank">CotEditor</a>で書いています。

で、それをEvernoteで保存しています。

ブログなどにアップする文章は実体ファイル（.txt）を作らずに、Evernoteのノートにしちゃうわけですね。

で、そのとき使っているのが、以下のスクリプト。

<a href="https://rashita.net/blog/?p=5519" target="_blank">CotEditorからEvernoteに送れるようになった</a>

この頂戴したスクリプトは、さらにカスタマイズされ、あらかじめ指定してあるタグをつけられるようになっています。

<a href="http://rashita.hatenablog.com/entry/2013/01/22/170734" target="_blank">CotEditor to Evernote(ApplleScript）をタグを付けられるように改造</a>

で、これをさらに改造しました。

<H3>文字数表示</H3>

まず最初に手をつけたのが、文字数の表示です。

書き終えた原稿をEvernoteに送った際、「文字数：○○○」という感じで、原稿の文字数をダイアログで表示させるようにしました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot.png" alt="screenshot" width="448" height="150" class="alignnone size-full wp-image-13867" /></a>

「うん。俺はこれだけ仕事したぞ！」という充実感をアップさせるための施策ですね。

しばらく使ってみた感触として、これはなかなか良いです。やっぱりフィードバックというのは重要ですね。

<H3>作業記録へ</H3>

で、気がつきました。これって作業記録になるんじゃね？　と。

テキストファイルの一行目は原稿のタイトルですし、タグとして選んだ文字列はプロジェクト名です。そして文字数カウントもある。ということは、自分で何一つ記録を取らなくても、CotEditorからEvernoteに送信した際に、作業ログを残せるのではないか、と。

私は、毎日デイリータスクリストをEvernoteで作成していますので、そこにデータを追記していけばOKです。つまり、こういう感じになります。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot1.png" alt="screenshot" width="500" class="alignnone size-full wp-image-13868" /></a>

残念ながら、ログにおける最重要な要素である「作業時間」についてはログできませんが、今のところそれを望むのは高望みというところでしょう。でも、何かしら工夫すれば、そこもクリアできるかもしれません。

<H3>コード</H3>

コードは以下のような感じ。

<script src="https://gist.github.com/rashita/2e5f668051dd627dace9.js"></script>

残念ながらハイパー個人カスタマイズしてあるので、このままでは確実に使い勝手が悪いです。

というわけで、ご利用になりたい方は、AppleScriptをググりながら、自分用にカスタマイズしてください。まあ、このツールの需要がどこまであるのかはまったくわかりませんが。

<H3>さいごに</H3>

なんにせよ、「半自動で残るログ」というのは大切です。モチベーション的なものにも関わってくるかもしれません。

今後も、こうしたものを拡張していきたいですね。

では、すてきなEvernoteライフを！

<strong>▼こんな一冊も：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 158000<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

