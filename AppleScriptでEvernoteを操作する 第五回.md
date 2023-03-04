---
title : AppleScriptでEvernoteを操作する 第五回
link : 22775
date : Sat, 26 Aug 2017 02:33:17 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

さて、<a href="https://rashita.net/blog/?p=22718">前回</a>一通り紹介したcreate noteを使って、より実用的なスクリプトを書いてみましょう。今回で、ぐぐっとプログラムっぽくなるはずです。

<h2>メモ作成</h2>

create noteを使えば、自動的にノートが作成できるのはよいとして、その中身が常に一定ではさほど意味はありません。ノートの内容を、あらかじめスクリプト内に記述しておくのではなく、何らかのデータ処理を行って動的に作成したいところです。

で、まず思い浮かぶのが、「メモ作成ツール」です。たとえば、ダイアログが表示されてそこにテキストを入力する。入力されたテキストを利用してノートを作る。こういう感じの動作なら、いかにもプログラムっぽいですね。

<a href="https://rashita.net/blog/?attachment_id=22776" rel="attachment wp-att-22776"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-22-500x503.png" alt="" width="500" height="503" class="alignnone size-medium wp-image-22776" /></a>

というわけで、実際に一番シンプルな形で書いてみましょう。

<a href="https://rashita.net/blog/?attachment_id=22778" rel="attachment wp-att-22778"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-24-500x223.png" alt="" width="500" height="223" class="alignnone size-medium wp-image-22778" /></a>

[code]
set myAnswer to display dialog &quot;メモを入力してね！&quot; default answer &quot;&quot;
set memoTxt to text returned of myAnswer

tell application &quot;Evernote&quot;
	create note with text memoTxt
end tell
[/code]

上記のコードをスクリプトエディタに書き込み、コンパイル後実行してみてください。

問題がなければ、以下のようなダイアログが表示され、

<a href="https://rashita.net/blog/?attachment_id=22777" rel="attachment wp-att-22777"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-23.png" alt="" width="410" height="142" class="alignnone size-full wp-image-22777" /></a>

適当に入力してOKを押せば、

<a href="https://rashita.net/blog/?attachment_id=22779" rel="attachment wp-att-22779"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-25.png" alt="" width="404" height="145" class="alignnone size-full wp-image-22779" /></a>

Evernoteにノートが作成されているはずです。

<a href="https://rashita.net/blog/?attachment_id=22780" rel="attachment wp-att-22780"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-26-500x369.png" alt="" width="500" height="369" class="alignnone size-medium wp-image-22780" /></a>

おお〜〜〜。ちょっとアプリっぽい感じがしませんか。ただ、あまりにも機能は貧弱で、ノートタイトルなんかも「無題」のままなので、これから改良していきたいところですが、その前に、今回初登場したコードを少しだけ解説しておきましょう。

<h2>default answer</h2>

コードの一行目には、見慣れない二つの記述が出てきます。一つ目はset、もう一つはdefault answerです。まずは後者からいきましょう。

一行目の途中に出てくる display dialogについては<a href="https://rashita.net/blog/?p=22638">第二回</a>で紹介しました。言葉通り、ダイアログを表示するコマンドです。で、このダイアログはなかなかイケてるやつで、今回のようにテキストフィールドを表示させることもできます。その際に使うのが、このdefault answerコマンド。普通に解釈すれば、「既定の答え」という意味で、それを何も指定しない（空白を指定する）ことで、空っぽのテキストフィールドを表示させている、というわけです。

逆に言えば、default answer "お前はもうメモしている" などと書けば、ダイアログのテキストフィールドにはあらかじめその文字列が表示されることになります（気になる方はコードを書き換えて試してみましょう）。

<h2>set</h2>

上記のダイアログによって、ユーザーからの入力を受け取ることはできました。しかし、そのままだと、それを後々利用することができません。そこで活躍するのがsetです。setは、簡単に言えば、

set a to b

で、「bの内容をaに入れておけ！」となるコマンドです。内容をセーブするわけですね。

まとめると、一行目のコードは、ダイアログを空っぽのテキストフィールドと共に表示して、返ってきた答えをmyAnswerにセーブしておいてね、くらいの意味になります。そして、この行以降は、myAnswerを扱えば、ユーザーからの答えを利用できます。

ちなみに、このmyAnswerが「変数」と呼ばれているもので、その名前はスクリプトを書く人が任意に決定できます。今回はmyAnswerにしましたが、aTextとか、QuantumWordとか、なんだって構いません。ただし、AppleScriptとして使われているtellやsetなどの言葉（予約語）はエラーが出ますので注意してください。
※細かい話が気になる方は「変数」でググってみましょう。

<h2>テキスト要素の取り出し</h2>

あとはユーザーからの答えを使ってノートを作成したいところなのですが、そのデータを保存したmyAnswerには、テキスト以外の要素もいろいろ含まれています（たとえばどのボタンが押されたか、など）。そこで、myAnswerの中に含まれている、テキスト要素だけをまた別の領域にセーブしておく、というのが二行目のコードです。

set memoTxt to text returned of myAnswer

ほとんど英語をそのまま読めば、理解できるでしょう。memoTxtに、myAnswerに含まれている返ってきたテキストの要素をセットせよ。よって、以降はmemoTxtを扱えば、ユーザーから返ってきた（ユーザーが入力した）テキストが利用できます。

<h2>さいごに</h2>

ここまでくればあとは簡単ですね。前回までのcreate noteの使い方を合わせれば、memoTxtを内容に指定して、with textでノートを作成すればOKです。create noteを使うために、tell application "Evernote"を宣言するのを忘れないようにしましょう。

さて、非常にシンプルではありますが、これで動的なノート内容の作成が可能となりました。ここからさまざまなアレンジが可能ですが、やることのベースはこのスクリプトにまとまっています。何からの形で処理を行ったデータを用いて、ノートを作成する。あとは、データ処理の方法をいろいろ学んでいくだけです。

次回は、このスクリプトをもう少し改良してみましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.26</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 45,661<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.26</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 2,774<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

