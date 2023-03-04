---
title : Scrivener→でんでんコンバーターで気をつけたいこと（アルテさんと僕）
link : 15905
date : Thu, 23 Apr 2015 02:48:14 +0000
categories : ["5-創作文","物書き生活と道具箱"]
tags : ["アルテさんと僕","scrivener","電子書籍"]
draft : false
author : 倉下忠憲
---

「アルテさん、助けてください！」
「何？」
「<a href="http://conv.denshochan.com/" target="_blank">でんでんコンバーター</a>でEPUBファイル作ったんですけど、エラーが出ちゃってうまく表示されないんです」
「エラー文でググってみて」
相談はそれで打ち切り、と言わんばかりに本のページをめくるアルテさん。
「いや、一応僕もウェブ時代に生きていますから、それぐらいはやってみましたよ。でも、英語のページばっかりでさっぱりなんです」
「ウェブ時代に生きてるんだったら、英語ぐらい読めないとね」
ページをめくる手は止まらない。厚みのある文庫本は、まだはじめの方だ。きっと買ってきたばかりの新刊なのだろう。
「ア・ル・テ・さん！」
目一杯のアピールをすると、やれやれと大げさに首を振ってから、アルテさんは机に本を置いた。
「どんなエラー？」
「Char value 12なんちゃらっていうのが出てくるんです」
眉をぴくりと上げたアルテさんは、「みせて」と僕のノートパソコンを引き寄せる。

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot7.png" alt="screenshot" width="482" height="448" class="alignnone size-full wp-image-15907" /></a>

「どうやってこのEPUBを作ったの」
ほとんど詰問口調でアルテさんが尋ねてくる。
「ええっと、この前教えてもらったScrivenerというアプリで、テキストファイルを作って、それをでんでんコンバーターにアップしたんですが……」
「そのファイルは？　テキストじゃなくて、おおもとの方」
「これです」
えらく画面に近いアルテさんの顔に遠慮しながら僕はキーボードを叩く。
「ちょっといい？」と僕の返事を待たずに、アルテさんはトラックパッドに指を置く。繊細な長い指。ピアノの鍵盤が似合いそうだ。
「これね」

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot9.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15909" /></a>

ディスプレイにはCompileの設定ウィンドウが表示されていた。「このPBが悪さをしてるの」。アルテさんは、画面右の小さい文字を指さす。そこには「Pg Break Before」とあった。
「Pg Break？　プログラマーをぶっ壊すってことですか。なかなか物騒ですね」
「その発言の方が物騒だと思うけど」
コホンと咳払いを一つしてから、アルテさんは続ける。
「PgはPage。Page Breakで改ページの区切りってところね」
「それをBefore？」
「そう、ようするにこのテキストの後に改ページを入れます、というのがこのチェックマークの意味」
「それを入れるとどうなるんですか」
「もちろん改ページされるわよ。テキストファイルでは意味がないけれども、たとえばPDFでコンパイルしてみればわかるわ」
「これが何か悪さをしてるんですか」
「まあ、そうね。さっきのEPUBのもとになったテキストファイルを開いてみて」
アルテさんが立てた指をクルクルと回す。
僕は、tab + commandでアプリを切り替える。ちょうどさっき開いていたところだ。

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot8.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15908" /></a>

「ほら、ここ」とアルテさんが指さす。
「何かありますか？」
「よく見なさいよ」
「この横棒ですか？」
「そう、それがChar value 12ね。その行を削除してみて」
言われた通りに、僕は行頭でdeleteキーを押す。

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot10.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15910" /></a>

「ほら、消えたでしょ。これならエラーは出ないわ」
「ということは、さっきのコンパイルの設定でチェックマークを外せばOKなんですね」
「まあ、そうね。ただし、注意する箇所がもう一つ」
「もう一つ？」
「Scrivenerだと、コンパイル時にSeparatorsの設定ができるの。テキストとテキストの間とかテキストとフォルダの間に、任意の文字列なんかも潜り込ませられる。そこにも、Page breakがあるから、そこもチェックしておいた方がいいわね」

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot11.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15911" /></a>

「なるほど」
パタパタとチェックマークを外し、Separatorsの設定も確認する。アルテさんはじっとその作業を見つめている。テキストファイルでコンパイルし、一応その中身も確認する。変な横棒はついていない。
でんでんコンバーターにそのファイルをアップロードして、iBooksで確認。

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot12.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot12-1024x772.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-15912" /></a>

エラーはどこにもなかった。
「ありがとうございます」
僕がそう言うと、コクリとアルテさんが頷く。
「ところでその本、面白そうね」
「でしょ。といっても、まだ取りかかったばかりなんですが。完成したらまっさきにアルテさんにお見せしますよ」
ありがと、とだけ言ってアルテさんは自分の席に戻っていった。再び文庫本に手が伸びる。僕も原稿の手直しに戻る。
ぱらりぱらり、カタカタ、カタカタ、という音だけが部屋に満ちていた。

<hr />
＜アルテさんと僕シリーズ＞

<a href="https://rashita.net/blog/?p=15126" target="_blank">でんでんコンバーターでスタイルを変更する方法（アルテさんと僕）</a>
<a href="https://rashita.net/blog/?p=15170" target="_blank">でんでんコンバーターでスタイルを変更する方法２（アルテさんと僕）</a>
<a href="https://rashita.net/blog/?p=15339" target="_blank">でんでんコンバーターでスタイルを変更する方法３（アルテさんと僕）</a>

<a href="https://rashita.net/blog/?p=15432" target="_blank">でんでんコンバーターで改ページする方法（アルテさんと僕）</a>

<a href="https://rashita.net/blog/?p=15823" target="_blank">でんでんコンバーターにアップできるファイル（アルテさんと僕）</a>


