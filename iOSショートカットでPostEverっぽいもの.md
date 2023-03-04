---
title : iOSショートカットでPostEverっぽいもの
link : 29352
date : Tue, 20 Aug 2019 02:03:58 +0000
categories : ["プログラミング"]
tags : ["evernote","iosショートカット"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=28639">iOSのショートカットを学ぶ９</a>で、同一のノートにガシガシ追記していけるショートカットを作った。が、できるのはあくまでテキストの追加だけである。せっかくなら、写真も追加できるようにしたい。そこで改造だ。

流れのイメージは以下の通り。

・「テキスト」か「写真」を最初に選ぶ
・「テキスト」を選択したら入力ダイアログが立ち上がりメモが入力できる
・「写真」を選択したらカメラが立ち上がり写真が撮れる
・それぞれの内容をEvernoteの日付ノートに追記する

「テキスト」の処理と、「日付」の処理は、上の記事で解説したので、今回は分岐と写真の処理となる。といっても、これもこれまで書いてきた記事の知識でカバー可能だ。

<a href="https://rashita.net/blog/?attachment_id=29354" rel="attachment wp-att-29354"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/B25CBD28-69CF-4B25-8A31-D2C10B1D4127.jpg" alt="" width="640" height="1136" class="alignnone size-full wp-image-29354" /></a>

「メニューからの選択」で分岐を設定する。必要なのはテキストと写真だけなので、二つの選択肢を設定する。

<a href="https://rashita.net/blog/?attachment_id=29355" rel="attachment wp-att-29355"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/1E121D41-449D-474C-AF3F-544388030435.jpg" alt="" width="640" height="1136" class="alignnone size-large wp-image-29355" /></a>

「テキスト」時の処理はこんな感じ。入力した内容を、bodyという名前の変数に入れておく。

<a href="https://rashita.net/blog/?attachment_id=29356" rel="attachment wp-att-29356"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/0C6342AF-6416-4175-BEF7-54BC9CDFC734.jpg" alt="" width="640" height="1136" class="alignnone size-large wp-image-29356" /></a>

「写真」が選択されたときは、「写真を撮る」が選ばれ、撮られた写真のサイズを小さくする。単に日記的なものの写真だし、あまりサイズが大きいと送信に時間がかかってしまうが故の処置である。

<a href="https://rashita.net/blog/?attachment_id=29357" rel="attachment wp-att-29357"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/A0547BCF-48E0-4AD7-9E98-4A7602FAA8CF.jpg" alt="" width="640" height="1136" class="alignnone size-large wp-image-29357" /></a>

でもって、その処理した写真のデータを、やっぱり変数bodyに入れておく。一応解説しておくと、この「テキスト」と「写真」は分岐処理なので、一回の実行においてはどちらかしか発動しない。つまり、bodyにはテキストか写真かのどちらかが入ることになる。

でもって、一応の保険として、その写真データは、フォトアルバムにも保存しておく。送信できなかったときなどはフォトアルバムから写真にアクセスできるはずだ。

<a href="https://rashita.net/blog/?attachment_id=29358" rel="attachment wp-att-29358"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/0EA936F1-74A7-40FB-BD07-4ABF3E9C253F.jpg" alt="" width="640" height="1136" class="alignnone size-large wp-image-29358" /></a>

で、その日の日付を取得して、私のEvernoteのノートのフォーマットに合わせておく。

<a href="https://rashita.net/blog/?attachment_id=29359" rel="attachment wp-att-29359"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/099C81DF-50DB-46A5-977A-3821028B2DB7.jpg" alt="" width="640" height="1136" class="alignnone size-large wp-image-29359" /></a>

その上で、変数bodyの中身を取得し（テキストか写真が入っている）、それをEvernoteの「メモに追記」に渡す。ノートのタイトルを、先ほどフォーマットした日付に設定する。これで完了だ。

<h2>さいごに</h2>

これで写真を撮っても、以下のようにきちんとデイリーノートに追加されることになった。

<a href="https://rashita.net/blog/?attachment_id=29360" rel="attachment wp-att-29360"><img src="https://rashita.net/blog/wp-content/uploads/2019/08/screenshot-21-700x648.png" alt="" width="700" height="648" class="alignnone size-large wp-image-29360" /></a>

無事完成である。が、写真を送信する場合はかなり待たされる。覚悟が必要だ。

だったらPostEverとかDayEntryとかを使えばいいじゃないかと思われるかもしれないが、私は私で事情がある。それらのアプリは、自動的にデイリーノートを作ってくれるのだが、私はそれが邪魔なのである。なにせもう365日分のデイリーノートが作成されている。しかも、それらのノートが、前後の日付ページへのリンクを含んでいる。逆に言うと、Evernoteで前後の日付ページへのリンクを設定するためには、あらかじめそれらのノートを作っておく必要がある。アプリが自動的にノートを作ってくれる方式とはすこぶる相性が悪いのだ。

というわけで、私は少し待たされることを選択しよう。幸い、一日辺りに写真を取る枚数は平均1枚を切っているので大した損失ではない。うまく付き合っていけるだろう。

ちなみに、最初の選択肢をもう一つ増やして、音声入力でのメモに対応させることも可能だ。そういうアレンジはいくらでもできるのでお好みでどうぞ。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank" rel="noopener noreferrer">amazlet</a> at 19.08.20</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 104,710<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank" rel="noopener noreferrer">amazlet</a> at 19.08.20</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 1,169<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
