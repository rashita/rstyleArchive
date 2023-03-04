---
title : Hagoromoの文章をEvernoteに保存するスクリプト
link : 13393
date : Thu, 22 May 2014 02:00:49 +0000
categories : ["物書き生活と道具箱"]
tags : ["applescript","evernote","hagoromo"]
draft : false
author : 倉下忠憲
---

引き続きMacのエディタ「Hagoromo」の話題を。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a3.mzstatic.com/us/r30/Purple6/v4/16/69/7d/16697da8-bb23-8206-01df-99dbb9dc5b83/hagoromoApp.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/hagoromo/id865949654?mt=12&uo=4&at=11l4y8" target="itunes_store">Hagoromo</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, ビジネス</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/hagoromo/id865949654?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

Hagoromoは、AppleScriptに対応しております。

公式さんでも、いくつかスクリプトが公開されていて、なかなか便利そうなものもチラホラと。

<a href="http://www.artman21.com/jp/hagoromo/scripts.html" target="_blank">スクリプトライブラリ</a>

ここでダウンロードしたスクリプトを、メニューのスクリプトっぽいアイコン→「スクリプトフォルダを表示」で表示されるフォルダに入れておけば簡単に召喚できます。

たとえば、公式さんの「日付（元号）スタンプ」を、

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot23.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot23.png" alt="screenshot" width="380" height="265" class="alignnone size-full wp-image-13394" /></a>

こうやってフォルダに入れておくと、

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/scrchot.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/scrchot.png" alt="scrchot" width="230" height="170" class="alignnone size-large wp-image-13396" /></a>

メニューに「日付（元号）スタンプ」が表示されるようになり、それを選択すると、

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot24.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot24.png" alt="screenshot" width="325" height="98" class="alignnone size-large wp-image-13395" /></a>

このように日付と時間が自動的に挿入されます。

スクリプトを改造する僅かばかりの知識があれば、この日付・時間フォーマットを変更することも可能です。時間だけとか、日付だけとか。自分の用途に合わせることができるわけですね。

あるいは改造するだけでなく、自分好みの機能を持たせることも（ある程度は）可能になります。

<H3>自作スクリプト</H3>

というわけで、Hagoromoに書いた文章をEvernoteに保存するスクリプトを書いてみました。スクリプト本体はもう少し下にあります。

文章を書き終えた後、このスクリプトを起動させると、タグの選択画面が表示されます。で、タグを選ぶとそのタグ付きでEvernoteにノートが作成されます。当然、ノートの中身は書いた文章です。Hagoromoは文章以外に画像ファイルも追加できますが、そうしたものは反映されません。ピュアにテキストだけです。

またノートタイトルは、ファイル名ではなく文章の一行目が使用されますのでご注意ください。

ちなみに、タグを選ばずにキャンセルすると、タグなしでEvernoteに送信されます。そうです、一度スクリプトを起動させると、Evernoteに送信しない、という選択肢は無いのです。まあ、いいですよね。いらなかったら、あとでノートを削除すればいいわけですから。

しかしながらシンプルに考えると、スクリプトを使わずとも、文章全体をコピーして、control + command + v をぽちっと押せば済む話です。わざわざスクリプトを書く意味みたいなものは感じられません。

ただ、このスクリプトを使うと、自動でタグを（ただし、あらかじめしておいたタグを）割り当てることができます。これが地味にinboxを整理するときに効いてきます。特に、毎日毎日文章を書いているような人間ならなおさらです。

<script src="https://gist.github.com/rashita/fc09cb6fa78dc2422b45.js"></script>

「ちょっと使ってみたい」という方は、AppleScriptエディタ開き、上のコードをコピペした上で、冒頭のタグ指定をお好みのものに変えてからご使用ください。

そのまま使えば、デフォルトノートブックにノートが新規作成されます。ノートブックを指定したい場合は、二行目のコメント指定を外した（※）上で、保存したいノートブック名を変数に入れてください。
※コメント指定を外すとは、冒頭にある二つの「-」を削除することを意味しています。

ついでに、19行目をコメントアウト（※）し、その代わりに21行目のコメントを外してください。
※コメントアウトするためには、行の冒頭に二つの「-」を入力します。

個人的には、ノートは一度inboxを経由した方がよいと考えているのでこの形にしていますが、人によってはinboxがデフォルトノートブックではない可能性もあるので、一応ノートブック指定も配慮しておきました。

<H3>さいごに</H3>

おそらく上のスクリプトは、人によっては使い勝手が悪い部分もあろうかと思います。

その辺は各自自由に改造してください。

<strong>▼関連エントリー：</strong>
<a href="https://rashita.net/blog/?p=13330" target="_blank">Macのエディタ「Hagoromo」に注目しています</a>
<a href="https://rashita.net/blog/?p=13372" target="_blank">HagoromoでEPUBファイルを作ってみる</a>