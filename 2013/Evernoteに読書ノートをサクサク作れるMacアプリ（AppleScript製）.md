---
title : Evernoteに読書ノートをサクサク作れるMacアプリ（AppleScript製）
link : 10327
date : Mon, 08 Apr 2013 02:08:51 +0000
categories : ["物書き生活と道具箱"]
tags : ["applescript","evernote"]
draft : false
author : 倉下忠憲
---

を自作しました。

読書ノートを作るとき、「レバレッジ・メモ」スタイルであれば簡単です。テキストエディタなり、Evernoteなりを使って、1枚のファイル（ノート）にまとめれば済みます。

が、情報カードを使うように「1トピックス、1ノート」方式でノートを作成する場合、大きな問題が発生します。

それは、「引用元をいちいち転記するのが面倒」という問題です。

”引用元”とは、書籍・論文のタイトルや著者名といったデータのこと。こうしたメタ情報を残していない場合、データとしての活用度はぐぐんっと下がってしまいます。

これまで私は「コピーアンドペースト」という文明の技術を使って、その問題に対処していました。すばらしきパーソナルコンピュータの恩恵です。しかし、長く続けていると、一つ一つのノートにcommand + V を押して回るのも何だか面倒に感じ始めます。人間の怠惰力を侮ってはいけません。

というわけで、AppleScriptの出番です。

<H3>基本動作</H3>
動作はごくシンプルです。アプリを起動すると、まずタイトルの入力を要求されます。ぱたぱたと入力してみましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot.png" alt="screenshot" width="474" height="261" class="alignnone size-full wp-image-10331" /></a>

続いて著者名です。これもシュパシュパとタイピングします。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot1.png" alt="screenshot" width="388" height="177" class="alignnone size-full wp-image-10332" /></a>

次に、引用文の入力画面です。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot2.png" alt="screenshot" width="474" height="325" class="alignnone size-full wp-image-10333" /></a>

本の中から、読書ノートとして残したい部分を転記しましょう。もし、その部分に関して自分なりの考察メモを残したい場合は、「メモの入力」をぽちっと押してください。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot3.png" alt="screenshot" width="474" height="357" class="alignnone size-full wp-image-10334" /></a>

このようなメモの入力画面になります。知力を振り絞って、あるいはあるがままの連想に流されてメモを残してみましょう。創造というのは、そういう作業から始まります。

で、メモの入力を終えたら、「OK」を。すると次のようなノートがEvernoteに作成されます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot4.png" alt="screenshot" width="440" height="290" class="alignnone size-full wp-image-10335" /></a>

本文の一行目がタイトルになったノートですね。引用部分、メモ、著者名、タイトルがばっちり入っています。

が、これは裏側の処理。アプリでは入力を続けるかどうかが問われます。勇ましい気持ちをもって「続ける」をプッシュしましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot5.png" alt="screenshot" width="474" height="225" class="alignnone size-full wp-image-10336" /></a>

すると、再び引用部分の入力ダイアログが表示されます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot6.png" alt="screenshot" width="474" height="325" class="alignnone size-full wp-image-10337" /></a>

入力し「これでOK」を押すと、こちらも次のようなノートが作成されます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/04/screenshot7.png" alt="screenshot" width="440" height="365" class="alignnone size-full wp-image-10338" /></a>

このループが「終了する」を押すまでくるくる回り続けます。

書名と著者名を入力するのは最初の一回だけ。後は、すべての読書ノートに自動的にそのメタ情報が追記されることになります。

<H3>中身開陳</H3>
コードの中身はこちら。

<script src="https://gist.github.com/rashita/5333427.js"></script>

ノートのデザインはHTMLでいじってあります。上部の変数の中身を変えれば、背景色やフォントなどを好みのデザインに変更できます。

<H3>次なる一歩</H3>
今のところ、バージョンアップ案としては、
<ul>
	<li>著者の名前をタグにする</li>
	<li>背景色をユーザーが選べるようにする</li>
	<li>フォントも変更できる</li>
	<li>ノートの見出しを別につける</li>
</ul>


といったものがあります。

もちろん、自分で実装できる方は、必要な機能をばしばし追加してください。

<H3>さいごに</H3>
使ってみたいけど、AppleScriptはよくわからん、という方は以下のリンクからダウンロードし、解凍して使ってください。

<a href="https://dl.dropbox.com/u/554861/bookquote.zip">https://dl.dropbox.com/u/554861/bookquote.zip</a>

もちろん、Mac版のEvernote用ですし、最新版のEvernoteでしか運用していないので、古いバージョンで動かなかったらごめんなさい（たぶん大丈夫だとは思います）。

こうして作成したノートは、以下の本で紹介したように、ハブノートにノートリンクをまとめておくと、さらに使い勝手があがりますね。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E3%82%BD%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E6%99%82%E4%BB%A3%E3%81%AE%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E8%AA%AD%E6%9B%B8%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541244%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541244" target="_blank">ソーシャル時代のハイブリッド読書術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E3%82%BD%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E6%99%82%E4%BB%A3%E3%81%AE%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E8%AA%AD%E6%9B%B8%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541244%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541244" target="_blank"><img src="http://ecx.images-amazon.com/images/I/518XjWRBV5L._SL160_.jpg" border="0" alt="ソーシャル時代のハイブリッド読書術" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-03-26<br />売り上げランキング : 1975<br /><br /><br /><a href="http://www.amazon.co.jp/%E3%82%BD%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E6%99%82%E4%BB%A3%E3%81%AE%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E8%AA%AD%E6%9B%B8%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541244%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541244" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

