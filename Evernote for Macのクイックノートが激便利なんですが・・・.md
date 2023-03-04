---
title : Evernote for Macのクイックノートが激便利なんですが・・・
link : 10038
date : Thu, 21 Mar 2013 02:04:58 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

新バージョンで遂に正式導入された「クイックノート」。β版だと日本語が通らなかったのでムズムズしてたんですが、正式版では問題なく使えるようになっています。

詳しい機能は以下の記事で。

<a href="http://blog.evernote.com/jp/2013/03/14/12553" target="_blank">Evernote for Mac アップデート: クイックノートで時間を節約</a>（Evernote日本語ブログ）

とりあえず激しく便利なんですが・・・

あの、何というのか、サードパーティーがちまちま作っていたら本家が登場して一気に潰された、みたいな感覚がちょっとだけわかりました。

明らかに自作スクリプトの「goEver」が用無しです。

<h3>過去形になりつつある愛用品</h3>
<a href="https://rashita.net/blog/?p=5376" target="_blank">Mac中にEvernoteにメモを送るためだけのアプリ『goEvernote』（仮）</a>
<a href="https://rashita.net/blog/?p=6970" target="_blank">goEvernote（仮）をQuickSilverでもう一段早く&amp;改名しました</a>

これですね。AppleScriptで作成したアプリをQuickSilver系のランチャーに登録し、さらにHOTキーを設定しておくと、まるでiPhoneアプリ「FastEver」みたいな感覚でEvernoteにメモを遅れちゃうわけです。個人的超愛用アプリでした。

そう、もはや過去形になりつつあります。

まず、本家のクイックノートは上のような設定は一切必要ありません。Appstoreダウンロード版ならばインストールしてすぐさま使い始められます。初心者にどちらを勧めるべきかと言えば、明らかに本家でしょう。

で、本家のクイックノートはテキスト以外のノート作成も可能です。画面キャプチャー、音声メモ、ファイル添付。個人的には画面キャプチャーのノートにすぐさまテキストメモを付け加えられる点が高評価です。もちろん、一行目がタイトルになってくれます。

純粋にテキストメモだけしか残さないというのであれば、「goEver」はクイックノートとタメを張れるような気がしますが、実はクイックノートだと位置情報が残るんですよね。「goEver」は単にメモを作成するだけです。

これを上位互換と言わず何を上位互換というのでしょうか。

まあ、私はアプリを有料で販売していたわけではないので、ノンダメージですが（ちょっと残念な感じはある）、そうじゃなかったら致命傷でしょうね。

<h3>チェックボックス付きノート</h3>
このまま「さよならgoEver」と別れを告げるのも、すがすがしいわけなんですが、ちょこっとだけあがいてみましょう。

テキスト用途に限定して、クイックノートにできないことはなんでしょうか。

まずは、チェックボックスです。

<a href="https://rashita.net/blog/?p=9642" target="_blank">Macでチェックボックス付きのメモもEvernoteに簡単送信「goEver3」</a>

このアプリを使えば、チェックボックス付きのノートが簡単に作成できます。ただし、一行限り。もちろん、チェックボックスなしのノートも作成可能です。

多少手を加えれば、各行の先頭にチェックボックスを付けることも可能でしょう。こういう方向に進化させていくこともできそうです。

<h3>ノートブックとタグを指定</h3>
もう一つは、ノートを保存するノートブックの指定とタグの設定。クイックノートはデフォルトのノートに突っ込まれますし、もちろんタグは付きません。

<script src="https://gist.github.com/rashita/5209957.js"></script>

上のスクリプトを使えばノートの保存先を指定し、タグを付けることもできます。

現状付けられるタグはひとつだけですが、多少改変すればひとつのノートに複数のタグを付けることも可能です。あるいはボタンをいくつか作り、複数のタグからひとつを選べるようにすることもできるでしょう。
※「アイデアノート」「ToDo」「タグ無し」といった感じ。

こういう方向に高機能化していくこともできます。

※上のスクリプトを使用される場合は、AppleScriptエディタを開き、上のコードをコピペし、10行目の"inbox"をお好みのノートブック名に、11行目の"アイデアノート"を好みのタグに書き換えて、アプリケーションとして保存してください。

<h3>さいごに</h3>
Evernoteが高機能化し、自作スクリプトを使わなくても望む機能が使えるというのは、なかなか素晴らしいものです。が、「こんなことなら、ちまちまとスクリプトの勉強しないでちょっと待っていればよかったな」という風には感じません。

「goEver」の作成で学んだ知識は、その他のアプリ作成にも大いに役立っています。そういうのって、個人的に結構大切です。

というわけで、近日goEverとは別の切り口のノート作成アプリを公開します。

とりあえずこのエントリーで一番言いたいのは、「クイックノートは便利だよ」ということです。goEverを愛用してくださっている方には説明不要でしょうが。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 98141<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<strong>▼Coming Soon…</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E3%82%BD%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E6%99%82%E4%BB%A3%E3%81%AE%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E8%AA%AD%E6%9B%B8%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541244%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541244" target="_blank">ソーシャル時代のハイブリッド読書術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E3%82%BD%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E6%99%82%E4%BB%A3%E3%81%AE%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E8%AA%AD%E6%9B%B8%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541244%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541244" target="_blank"><img src="http://ecx.images-amazon.com/images/I/518XjWRBV5L._SL160_.jpg" border="0" alt="ソーシャル時代のハイブリッド読書術" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-03-26<br />売り上げランキング : 20184<br /><br /><br /><a href="http://www.amazon.co.jp/%E3%82%BD%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E6%99%82%E4%BB%A3%E3%81%AE%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E8%AA%AD%E6%9B%B8%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541244%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541244" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

