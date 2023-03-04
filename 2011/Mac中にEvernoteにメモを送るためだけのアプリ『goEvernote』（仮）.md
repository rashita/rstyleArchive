---
title : Mac中にEvernoteにメモを送るためだけのアプリ『goEvernote』（仮）
link : 5376
date : Mon, 28 Feb 2011 00:47:30 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernoteをお使いの方は、PC触っているときに「おっ、そうだ、あれメモしとかなきゃ」と考えたときどんな風にEvernoteに送信されているでしょうか。考えられる手段はものすごく多彩です。

<ul>
	<li>クライアントを立ち上げて新規ノートを作成</li>
	<li>ロディアなどに書いておき、あとで処理</li>
	<li>iPhoneを取り出しFastEver起動</li>
	<li>適当なテキストエディタにでも書いてホットキーでとりこみ</li>
	<li>「ATOK Pad」などのアプリを使う</li>
</ul>


実際まだまだありますが、だいたいはこんな感じでしょうか。どのような手段でも良いのですが、できるだけ手軽に送りたいというのは常なる願いです。

<h3>一長一短</h3>
Windowsメインの時は、ホットキーを多様していたのですが、Macメインになってからは「Quickslver」をいじって、そこからメモを送信していました。QS自体は便利なヤツなのですが、テキスト入力モードの切り替えたりうんぬんが面倒だったので「ATOK Pad」に移行。optionキーx2で起動して、即メモ入力できるこいつはかなり重宝していました。

しかしながら、まったく問題がないかというとそうでもありません。まず勝手に「ATOK Pad」というタグを付けます。まあ、この辺は気にしなければどうということもありません。もう一つの問題がEvernoteへの送信です。ネットに接続していないと送信できないという罠があります。まあPC立ち上げているときは常時ネットにいるわけだから問題ないと言えば問題ないわけですが。

あと、細かいところですが「メモ入力→Evernoteに送信→アプリ終了」という手順の後、再びメモ入力しようと思ってアプリ起動すると前のメモが残っているんですよね。まあ新規ノート立ち上げればよいわけですが、コンマ0.5秒ぐらい「！？」となるのが微妙にストレスでした。

まあ、そういう微妙なすれ違いはあるにしても便利なメモです。ただ、もっと「FastEver」なみにシンプルにメモが送りたいという欲求が潜んでいたことも確かです。

<h3>『EgretType』</h3>
そういう状況で、登場したのが『EgretType』。ネーミングセンスも良ければアイコンのテカリ具合も抜群のこいつ。詳しいことは、@synkuroさんの

<a href="http://b2log.posterous.com/mac-evernoteegretlistegrettype">[Mac] Evernoteに簡単にチェックボックス付きメモ（しかもEgretlist形式）を作成できるアプリ『EgretType』</a>（b2log/p）

を参照していただくとして、簡単に言うとMacからEvernoteにタスク系のメモを即座に送れるアプリで、かつ「Egretlist」というアプリで参照できるフォーマットを実現しているというかなりニッチなユーザーを対象としたアプリです。

使ってみるとわかりますが、なかなか快適で、「アプリ起動→タスク名記入→詳細記入（あってもなくてもOK）→OKで送信」という流れがとてもスムーズです。Evernote上ではタスク名の頭にチェックボックスが付いて表示されます。Egretlistを使っていなくてもチェックボックス付きのノートを即座に作りたい場合はなかなか使えるアプリではないかと思います。

<h3>一念発起</h3>
前々からAppleScriptを使えばこういう事ができるのは知っていたのですが、やっぱり「めんどくさい」という思いが先に立ちます。が、今回の『EgretType』はコードを公開されており、その中身をのぞいてみると「なんとかなりそう」という気がふつふつと湧いてきました。このコードの改変して、自分好みのメモアプリが作れるんじゃないか、と。

自分でいくつかサイトを検索・探索してみると、簡単な動作なら予想以上に「らくちん」にできることがわかり、ゼロから（といっても6行ぐらいの）メモアプリ作りました。特に現状どうこうするつもりはないのでアプリのアイコンも手抜きでEvernoteのヤツをそのまま拝借しております。他に使う人がいるならなんとかしますが、結構ニッチなのでその心配も必要ないでしょう。アプリの名前も激しく適当です。

動作に関しても「うちのMacでは動く」というだけで、他のMacで動くのかどうかも試しておりませんので、使ってみたい方はその辺ご了承ください。

※以下ドロップボックスのダウンロードリンク(zipで圧縮してあります)
<a href="http://db.tt/MUEpkZy">http://db.tt/MUEpkZy</a>

<h3>簡単な説明</h3>
動作は、極めてシンプルです。

[caption id="attachment_5377" align="alignnone" width="400" caption="アプリ画面"]<img src="https://rashita.net/blog/wp-content/uploads/2011/02/window-grab.png" alt="アプリ画面" title="アプリ画面" width="400" height="317" class="size-full wp-image-5377" />[/caption]

アプリを起動→メモを入力→OKで送信。
※OKボタンはcommand + returnで。

[caption id="attachment_5378" align="alignnone" width="300" caption="こんなノートができます"]<img src="https://rashita.net/blog/wp-content/uploads/2011/02/screenshot5-300x118.png" alt="こんなノートができます" title="こんなノートができます" width="300" height="118" class="size-medium wp-image-5378" />[/caption]

これだけ。ポイントらしいポイントは、「一行目がノートタイトルになる」というだけです。WindowsのEvernoteは基本的に「ノートの一行目がノートタイトルになる」という仕様なんですが、現状Macバージョンではタイトル無しになってしまいます。これがどうしても引っかかっていたので、そこだけをフォローしたメモアプリを作りました。

「ATOK Pad」もノートタイトルは自動で付けてくれるのですが、改行を認識しないのかなかなか違和感あるノートタイトルになります。この辺も気にしなければどうということはないのですが、個人的には「一行目は見出しで入力」という形をシンプルに守りたいので、このアプリのスタイルにしてあります。

<h3>さいごに</h3>
タグを付けたりノートブックを付けたりすることもできますが、今回はものすごくシンプルなバージョンをたたき台としてアップしておきます。ソースいじれるようにしてありますので、その辺は改竄してみてください。

新しいバージョンを作ったらまたアップします。
<strong>
▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_top">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_top"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 648<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>


