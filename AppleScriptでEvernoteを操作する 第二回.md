---
title : AppleScriptでEvernoteを操作する 第二回
link : 22638
date : Sat, 05 Aug 2017 02:58:37 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

では、さっそくAppleScriptを触ってみましょう。

使用するのは「スクリプトエディタ」という標準アプリケーションで、「ユーティリティ」（あるいは「その他」）というフォルダに入っているかと思います。

<a href="https://rashita.net/blog/?attachment_id=22640" rel="attachment wp-att-22640"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-1.png" alt="" width="189" height="139" class="alignnone size-full wp-image-22640" /></a>

これを起動します。

<h2>新規ファイル作成</h2>

ファイル確認のダイアログが表示されるかと思いますので、「新規書類」を選択してください。すると、以下のようなウィンドウが立ち上がるはずです。

<a href="https://rashita.net/blog/?attachment_id=22639" rel="attachment wp-att-22639"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-500x503.png" alt="" width="500" height="503" class="alignnone size-medium wp-image-22639" /></a>

ここにコードを書いていくことになります。

<h2>AppleScriptの選択</h2>

この「スクリプトエディタ」では、AppleScript以外にもJavaScriptが書けます。なので、最初にAppleScriptが選択されているかどうかを確認しておきましょう。

<a href="https://rashita.net/blog/?attachment_id=22641" rel="attachment wp-att-22641"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-2.png" alt="" width="271" height="103" class="alignnone size-full wp-image-22641" /></a>

<a href="https://rashita.net/blog/?attachment_id=22642" rel="attachment wp-att-22642"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-3.png" alt="" width="256" height="123" class="alignnone size-medium wp-image-22642" /></a>

もともとAppleScriptが選択されていればそのままでOKです。もしJavaScriptになっているならクリックしてAppleScriptを選択してください。

<h2>テスト</h2>

では、ごくごく簡単なコードを書いてみましょう。安心してください。本当にごくごく簡単です。

ウィンドウに以下のコードを打ち込みます。コピペでも結構ですが、自分で打ってみてもよいでしょう。

<code>Display dialog "Hallo AppleScript"</code>

普通にコードを打ち込めば、このように紫字で表示されているかと思います。で、入力を終えたら、上にあるトンカチのボタン（コンパイルボタン）をクリック。

<a href="https://rashita.net/blog/?attachment_id=22643" rel="attachment wp-att-22643"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-4.png" alt="" width="279" height="126" class="alignnone size-full wp-image-22643" /></a>

以下のように、文字が変化しますね。

<a href="https://rashita.net/blog/?attachment_id=22644" rel="attachment wp-att-22644"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-5.png" alt="" width="276" height="128" class="alignnone size-full wp-image-22644" /></a>

こうなったら、構文的にはまあまあ問題ないよ、ということなのですがそれはさておき、そのままトンカチの左にある音楽プレイヤーの再生みたいなボタン（実行ボタン）を押してみましょう。以下のようなダイアログが表示されればOKです。

<a href="https://rashita.net/blog/?attachment_id=22646" rel="attachment wp-att-22646"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-7-500x300.png" alt="" width="500" height="300" class="alignnone size-medium wp-image-22646" /></a>

つまり、Display dialogは、「ダイアログを表示（ディスプレイ）したまえ」という命令で、その後に続く"Hallo AppleScript"が、そのディスプレイに表示されるテキストの内容を指定しています。当然"Hallo AppleScript"の中身を変更すれば、ダイアログに表示されるテキストも変わりますので、ちょこちょこ書き換えて試してみてください。

というわけで、今回はスクリプトエディタの基本中の基本を紹介しました。まずは、コードを実行するための、コード書き（変更）→コンパイル→実行、という流れを掴んでください。

次回はさっそくEvernoteの操作へと入っていきましょう。