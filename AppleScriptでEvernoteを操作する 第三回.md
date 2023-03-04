---
title : AppleScriptでEvernoteを操作する 第三回
link : 22680
date : Sat, 12 Aug 2017 03:52:36 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---


では、実際にEvernoteを操作するためのコードを書いていきましょう。

覚えていると思いますが、一応書いておくと、使うのは「スクリプトエディタ」の"AppleScript"モードです。忘れた方は、<a href="https://rashita.net/blog/?p=22638">前回</a>を復習しておいてください。

<a href="https://rashita.net/blog/?attachment_id=22641" rel="attachment wp-att-22641"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-2.png" alt="" width="271" height="103" class="alignnone size-full wp-image-22641" /></a>

<h2>tell Application</h2>

いきなりですが、スクリプトエディタに次のコードを入力してみましょう。

<code>
tell Application "Evernote"
create note title "テスト" with text "テストノートです。"
end tell
</code>

もちろんコピペでも構いませんが、コード書きに不慣れなら、自分で入力してみてもよいでしょう。

<a href="https://rashita.net/blog/?attachment_id=22683" rel="attachment wp-att-22683"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-8.png" alt="" width="416" height="154" class="alignnone size-full wp-image-22683" /></a>

入力が終わったら、トンカチ風のコンパイルボタンをポチっと。入力にミスがなければ、このように整形されるはずです。

<a href="https://rashita.net/blog/?attachment_id=22684" rel="attachment wp-att-22684"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-9.png" alt="" width="426" height="151" class="alignnone size-full wp-image-22684" /></a>

では、再生ボタン風の実行ボタンを押してみましょう。あっと、その前にEvernoteアプリを起動させておいた方がスムーズかもしれませんね。起動していなくてもこのコードの実行で自動的に起動されますが初期の同期などでもたつくこともあるでしょうから、予め起動させておくのも一手です。

で、コードにミスがなければ、実行後に以下のようなノートが作成されていることでしょう。

<a href="https://rashita.net/blog/?attachment_id=22685" rel="attachment wp-att-22685"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-10-500x467.png" alt="" width="500" height="467" class="alignnone size-medium wp-image-22685" /></a>

成功です。おめでとうございます。コードを書くだけで、自動的に新規ノートを作成できました。これがAppleScriptでEvernoteを操作することの基本的なスタイルです。

もちろん、ノート一枚程度なら手動でやった方が早いかもしれませんが、これはまあ、序の口というかお試し編みたいなものなので、工夫次第ではもっと大規模な（あるいはややこしい）ことができるようになります。そうなってからが面白いわけですので、もうしばらくは基礎編にお付き合いください。

<h2>コード解説</h2>

では、コードの解説に入りましょう。ここを押さえておかないと、応用ができませんからね。説明が続きますがご了承を。

<code>
tell Application "Evernote"
　create note title "テスト" with text "テストノートです。"
end tell
</code>

まず全体は3行のコードで構成されています。

１行目：Evernoteにメッセージの送信を開始することを宣言
２行目：実際にEvernoteにさせることの記述
３行目：メッセージの送信の終了を宣言

AppleScriptは自然言語に近い形なので、おそらく込み入った解説は不要かもしれませんが、一応書いておきます。

まず、１行目の <strong>tell Application "Evernote"</strong> がこれから何度も登場する記述です。「"Evernote"というアプリケーションに、以下の命令を伝えてね」くらいの理解で良いでしょう。簡単に推測できることですが、"Evernote"部分を別のアプリケーション名に書き換えることで、Evernote以外のアプリを操作することも可能です。

そして、3行目の <strong>end tell</strong> がその終わりを示します。つまり、１〜３が大きなブロック（塊）であり、２がその中身ということです。コンパイルすると自動的にインデントが発生するので、わかりやすいかと思います。

で、メインとなる <strong>create note title "テスト" with text "テストノートです。"</strong> ですが、これもストレートに読めば、「ノートを作成する。タイトルは"テスト"で、中身は"テストノートです。"というテキストである、となるでしょうが、まったくその通りです。

この「create note」はEvernote専用の命令であり、tell Application "Evernote" ブロックの中でしか効果を発揮してくれません。逆に言えば、create noteで新規ノートを作成しようと思うなら、tell Application "Evernote"宣言が必要だ、ということです。

このようなEvernote専用の命令は複数準備されていて、それを理解することがEvernote操作の第二歩目となります。create noteコマンドについてはまた次回詳しく見ていきますが、その他のコマンドについては、スクリプトエディタのメニュー「ウィンドウ」から「ライブラリ」を選び、そこにある「Evernote」を選択すればコマンドリストが表示されるので、チラチラとでも覗いてもらえばよいでしょう。

<a href="https://rashita.net/blog/?attachment_id=22688" rel="attachment wp-att-22688"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-11.png" alt="" width="213" height="491" class="alignnone size-full wp-image-22688" /></a>

もし"Evernote"が選択肢にない場合は、左上の「＋」ボタンからEvernoteアプリケーションを追加してみてください。ちなみに、ここで追加できるものが「AppleScript対応アプリケーション」であり、ライブラリに追加できないものは対応していないアプリケーションということになります。見分ける際にでもお使いください。

とりあえず、Evernoteで使えるコマンドは以下に列挙されます。

<a href="https://rashita.net/blog/?attachment_id=22689" rel="attachment wp-att-22689"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-12-500x431.png" alt="" width="500" height="431" class="alignnone size-medium wp-image-22689" /></a>

すでに上記が自分で読める方は、たぶん私の解説は不要だと思いますので、そのままガリガリとコードを書いていってください。そうでない方は、しばらくは私と一緒に歩いていきましょう。

というわけで、次回は create note のもう少し詳しい使い方を紹介してみます。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.12</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 110,731<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.12</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 2,295<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
