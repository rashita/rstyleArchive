---
title : WorkFlowyの3種のExport +α
link : 18528
date : Thu, 14 Jul 2016 02:04:26 +0000
categories : ["アウトライナーで遊ぼう","物書き生活と道具箱"]
tags : ["opml","scrivener","workflowy"]
draft : false
author : 倉下忠憲
---

WorkFlowyには、作成したアウトラインを出力するためのパターンが３つ用意されています。

<a href="https://rashita.net/blog/?attachment_id=18529" rel="attachment wp-att-18529"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot1-500x435.png" alt="screenshot" width="500" height="435" class="alignnone size-medium wp-image-18529" /></a>
※メニューから「Export」を選択

Formatted
<a href="https://rashita.net/blog/?attachment_id=18530" rel="attachment wp-att-18530"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot2-500x407.png" alt="screenshot" width="500" height="407" class="alignnone size-medium wp-image-18530" /></a>

Plain Text
<a href="https://rashita.net/blog/?attachment_id=18531" rel="attachment wp-att-18531"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot3-500x404.png" alt="screenshot" width="500" height="404" class="alignnone size-medium wp-image-18531" /></a>

OPML
<a href="https://rashita.net/blog/?attachment_id=18532" rel="attachment wp-att-18532"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot4-500x406.png" alt="screenshot" width="500" height="406" class="alignnone size-medium wp-image-18532" /></a>

昔は、「表示されたテキストを選択→コピー→別の場所に貼り付け」、ができるだけでしたが、最近はファイルのダウンロードも可能になっています。

<h3>Formatted</h3>

ごく簡単に言えば、リッチテキスト。ワープロソフトなどに貼り付ければ、「箇条書き」の形式で貼り付けられます。

たとえば、Evernoteに貼り付けてみるとこうなります。

<a href="https://rashita.net/blog/?attachment_id=18533" rel="attachment wp-att-18533"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot5-500x360.png" alt="screenshot" width="500" height="360" class="alignnone size-medium wp-image-18533" /></a>

同じものをCotEditor（プレーンテキスト）を貼り付けるとこう。

<a href="https://rashita.net/blog/?attachment_id=18534" rel="attachment wp-att-18534"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot6-500x442.png" alt="screenshot" width="500" height="442" class="alignnone size-medium wp-image-18534" /></a>

行頭のバレットが消え、単に空白スペースの数だけで階層が表示されていますね。これはこれで使い勝手があるかもしれません。

ちなみに、このFormattedをファイルでダウンロードすると、html形式となります。箇条書きの形式はリストタグ（ul,li)による表現です。

<a href="https://rashita.net/blog/?attachment_id=18535" rel="attachment wp-att-18535"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot7-500x535.png" alt="screenshot" width="500" height="535" class="alignnone size-medium wp-image-18535" /></a>
※ダウンロードしたファイルをブラウザで閲覧

簡単に解説すると、項目（トピック）のclassは"name"、noteのclassは"note"となっています。正規表現による置換にでもお使いください。

<h3>Plain Text</h3>

その名の通りプレーンなテキスト。でも、普通にコピペすると、「いやいや、欲しいのはそれじゃないから」的に行頭に「-」が付いてきます。noteは行頭と行末に「"」です。これはダウンロードしたテキストファイルでも同じです。

<a href="https://rashita.net/blog/?attachment_id=18536" rel="attachment wp-att-18536"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot8-500x509.png" alt="screenshot" width="500" height="509" class="alignnone size-medium wp-image-18536" /></a>

このままではまるで使いものにならないのですが、正規表現による置換を使えば、マークダウン形式に変換できる可能性があります。ようは、「- 」を「#」に、「  - 」を「##」に置換すればいいわけですね。ただし、本文が入っている階層がバラバラだとややこしいことになります。

あるいは、行頭に「- 」が必ず付いてくることから、Scirvenerの「text and Split」で読み込ませる手もあります。

<a href="https://rashita.net/blog/?p=13922">Scrivenerにテキストファイルを分割してインポートする機能。そしてEvernoteからScrivenerへ。</a>

分割場所を示す記号に「- 」を指定すれば、綺麗に行頭の文字が消えてすべての項目がScrivenerに読み込まれます。ただし、WorkFlowy上の階層構造はいっさい消えてしまう点には注意しましょう。

<h3>OPML</h3>

いわゆるアウトライン形式。正式名称はOutline Processor Markup Language（アウトライン・プロセッサ・マークアップ言語）です。

<a href="https://rashita.net/blog/?attachment_id=18537" rel="attachment wp-att-18537"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot9-500x460.png" alt="screenshot" width="500" height="460" class="alignnone size-medium wp-image-18537" /></a>
※テキストエディタで開いてもさっぱり

この形式でダウンロードしておくと、他のアウトライナーアプリに読み込ませられます。また、たいていのマインドマップアプリもこの形式に対応しています。

もし本文をnoteに格納しているなら、Scrivenerへの移行も簡単です。

<a href="https://rashita.net/blog/?p=16596">WorkFlowyからScrivenerへインポート</a>

「いやいや、noteとか使ってないし」という方は、以下の変換スクリプトが役に立つかもしれません。

<a href="https://note.mu/maro_draft/n/n128a0418c25d">トピック圧縮ハサミスクリプト｜マロ。｜note</a>

noteはnoteでも別のnoteですが、最下位項目をnoteに変換するブックマークレットが提供されています。

<h3>ふつーにコピペ</h3>

ちなみに、Exportを経由せず、普通に項目を選択してコピーし、別のツールに貼り付けたらどうなるでしょうか。

プレーンなテキストエディタなら、こう。

<a href="https://rashita.net/blog/?attachment_id=18538" rel="attachment wp-att-18538"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot10-500x483.png" alt="screenshot" width="500" height="483" class="alignnone size-medium wp-image-18538" /></a>

リッチテキストエディタ（Evernote）ならこうです。

<a href="https://rashita.net/blog/?attachment_id=18540" rel="attachment wp-att-18540"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot12-500x314.png" alt="screenshot" width="500" height="314" class="alignnone size-medium wp-image-18540" /></a>

ようするに、Formattedなわけですね。
※おそらくChromeだとうまくいきません

<h3>さいごに</h3>

WorkFlowyはすばらしいツールですが、不思議とExportの使い勝手があまりよくありません。たぶん、それもまた本ツールの設計思想と関わっているのでしょう。

ちなみに、テキストファイルで扱う一番面倒のない方法は、Formattedからコピペして、半角スペースを置換で一気に削除してしまう方法です。

※これを
<a href="https://rashita.net/blog/?attachment_id=18541" rel="attachment wp-att-18541"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot13-500x483.png" alt="screenshot" width="500" height="483" class="alignnone size-medium wp-image-18541" /></a>

※こうする
<a href="https://rashita.net/blog/?attachment_id=18542" rel="attachment wp-att-18542"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot14-500x482.png" alt="screenshot" width="500" height="482" class="alignnone size-medium wp-image-18542" /></a>

階層は無くなりますが、使い勝手はあがります。

というわけで、皆様も楽しいアウトライン・ライフを。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51ymv5zS94L._SL160_.jpg" alt="クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.07.14</div></div><div class="amazlet-detail">インプレスR&D (2016-01-29)<br />売り上げランキング: 9,177<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.07.14</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 517<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>



