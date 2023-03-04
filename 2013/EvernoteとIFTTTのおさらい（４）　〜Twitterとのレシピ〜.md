---
title : EvernoteとIFTTTのおさらい（４）　〜Twitterとのレシピ〜
link : 12267
date : Fri, 20 Dec 2013 02:50:25 +0000
categories : ["evernoteの使い方"]
tags : ["evernoteとiftttのおさらい","evernote","ifttt"]
draft : false
author : 倉下忠憲
---

ここまででIFTTTの概要はつかめたと思います。

で、今回は実践編。

※前回まで
第一回：<a href="https://rashita.net/blog/?p=12150" target="_blank">EvernoteとIFTTTのおさらい（１）　〜IFTTTとは何か〜</a>
第二回：<a href="https://rashita.net/blog/?p=12228" target="_blank">EvernoteとIFTTTのおさらい（２）　〜トリガーとアクション〜</a>
第三回：<a href="https://rashita.net/blog/?p=12242" target="_blank">EvernoteとIFTTTのおさらい（３）　〜アクションの中身〜</a>

何か役に立ちそうなEvernoteとTwitterとの連携を考えてみます。

基本的には、

<strong>「(トリガー)Twitter→(アクション)Evernote」</strong>

のレシピです。

というのも、以前書いたとおりEvernoteのトリガーはひとつしかないので、考える余地がほとんどないからです。バリエーションを広げられるのはTwitter→Evernoteの形ですね。

では、さっそく。
<H3>シンプル連携</H3>Twitterチャンネルで使えるトリガーは以下の５つ。

「New tweet by you」（あなたがツイートしたら）
「New tweet by you with hashtag」（あなたがハッシュタグツイートをしたら）
「New tweet by you in area」（あなたが位置情報付きツイートをしたら）
「New link by you」（あなたがリンク付きツイートをしたら）
「New favorite tweet by you」（あなたがツイートをお気に入りにしたら）

まず、トップにある「New tweet by you」を使ってみましょう。

すると、次のような画面が出てきます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot37.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot37.png" alt="screenshot" width="500" height="394" class="alignnone size-full wp-image-12268" /></a>

リツイート、あるいはリプライを含めるかどうかの選択です。とりあえずは、スルーしておきましょう。

続いてアクションのチャンネルにEvernoteを選択します。Evernoteアクションは次の５つ。

「Create note」（ノートを新規作成する）
「Append to note」（ノートに追記する）
「Create a link note」（URLソースを含んだノートを新規作成する）
「Create image note from URL」（URLにある画像を含んだノートを新規作成する）
「Create an audio note from URL」（URLにある音声ファイルを含んだノートを新規作成する）

これまた一番最初の「Create note」を選択します。

すでに誰かが作成したレシピがあるのか、いくつかの項目が入力されていますね。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot38.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot38.png" alt="screenshot" width="500" height="520" class="alignnone size-full wp-image-12269" /></a>

<H3>使えるIngredient</H3>Twitter「New tweet by you」→Evernote「Create note」で使用できるIngredientは、

「Tweet Text」・・・ツイートの内容
「User Name」・・・ツイートのユーザー
「Link To Tweet」・・・ツイートへのリンク
「Create Date」・・・ツイート時間
「Tweet Embed Code」・・・ツイート埋め込みコード

の５つ。

上の4つは説明不要でしょう。「Tweet Embed Code」は、ツイート情報をひとまとめにして表示してくれる機能だとざっくり理解していただければよいかと思います。

標準で表示されるレシピにもこのIngredientが使われていますね。そのレシピでEvernoteにノートを作成すると次のようになります。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot39.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot39.png" alt="screenshot" width="500" height="363" class="alignnone size-full wp-image-12270" /></a>

レシピのBodyと見比べてもらうとわかりますが、viaよりも上の部分が「Tweet Embed Code」で作成された部分です。ツイート名、ユーザー名、ツイート時間がまとめて表示されています。基本的にはこれを使っておけば問題無いでしょう。

ただ、自分のツイートだけを保存するのであれば、ユーザー名は必要ありません。その場合は「Tweet Text」「Link To Tweet」「Create Date」あたりを使うとよいでしょう。

たとえば、こんな感じにすると、シンプルなノートが作れます（<a href="https://ifttt.com/recipes/135088">参照</a>）。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot40.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot40.png" alt="screenshot" width="500" height="495" class="alignnone size-full wp-image-12271" /></a>

Evernoteにできあがるノートはこんな感じ。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot41.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot41.png" alt="screenshot" width="500" height="327" class="alignnone size-full wp-image-12272" /></a>

ツイートと日時だけが表示されていて、日時はTwitter Webへのリンクになっています。これぐらいの情報があれば十分ですね。

逆に特にリツイートを含める場合は、ユーザー名が欲しいので、素直に「Tweet Embed Code」を使った方がよいでしょう。

<H3>チャレンジ・アレンジ</H3>以上がベーシックなTwitterとEvernoteの連携です。

このまま運用すると、自分の全ツイート（RT、リプライ除く）が、1ツイート1ノートで保存されていきます。が、さすがにノート数上限の問題もありますし、普通に運用するのは微妙かもしれません。

ここからがアレンジです。

<H4>アレンジ１：ノートに追記する</H4>ベーシックなレシピは、

「New tweet by you」→「Create note」

でしたが、これを

「New tweet by you」→<strong>「Append to note」</strong>

こう変えることで、1ノートに全ツイートが追記されていきます。

もちろんノートの容量にも限界がありますが、かなりのツイートを溜め込むことができるでしょう。一杯になれば、別のノートを作り、そこに追記していくことで対応できます。

<H4>アレンジ２：ハッシュタグを使う</H4>当連載の一番最初に紹介させていただいた、

<a href="http://lifehacking.jp/2013/12/sending-notes-to-evernote-from-twitter/" target="_blank">Evernoteとツイッターをつなぐ@myen機能が終了へ。利用している方は移行作業を</a>（Lifehacking.jp）

で紹介されているのがこの方法。

<strong>「New tweet by you with hashtag」</strong>→「Create note」

というレシピです。

このレシピでは、自分で決めたハッシュタグ（#myenなど、#付きの言葉）が付いているツイートだけをEvernoteに保存します。
※もちろん自分のツイートです。

この方法であれば、TwitterをEvernoteの送信アプリ的に使うことができます。また、私がやっている「今日の一言」など、Twitterで展開しているマイクロコンテンツを抜粋してロギングしていくこともできますね。使い方はいろいろあります。

もちろん、

「New tweet by you with hashtag」→<strong>「Append to note」</strong>

にして1ノートにまとめることもできます。

<H4>アレンジ３：お気に入りを使う</H4>もう一つの方向がfav.を使うもの。

<strong>「New favorite tweet by you」</strong>→「Create note」

というレシピです。

これで、ファボした（お気に入りにした）つぶやきがEvernoteに保存されます。

どちらかといえば、これは（自分が気に入った）他の人のつぶやきをEvernoteに保存する使い方になるでしょう。もちろん、自分のツイートをファボしていく手もあります。

言うまでもありませんが、

「New favorite tweet by you」→<strong>「Append to note」</strong>

というレシピもありです。こちらは、お気に入りのツイート一覧ノート、みたいな感じになるでしょう。これはこれで楽しそうです。

<H3>さいごに</H3>ざっと上げただけでも、多様なバリエーションが考えられます。

ここからどんなものを組み上げていくのか。それは、あなた次第です。こういうのは、なんだかレゴっぽくて、私は実に楽しいです。

ちなみに、TwitterとEvernoteの連携で言えば、「<a href="http://twieve.net/ja" target="_blank">ツイエバ</a>」という優れたサービスがあるのですが、お気に入りだけをEvernoteに入れたい、なんて場合はIFTTTを使ってみるのもよいでしょう。

次回は、Twitter以外のトリガーにも目を向けてみます。

次回→<a href="https://rashita.net/blog/?p=12315" target="_blank">EvernoteとIFTTTのおさらい（５）　〜他のWebツールのレシピ〜</a>
【告知】
12/21に新刊が発売になります。

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_top">KDPではじめる セルフパブリッシング</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_top"><img src="http://ecx.images-amazon.com/images/I/51hhsyNMkKL._SL160_.jpg" border="0" alt="KDPではじめる セルフパブリッシング" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-12-21<br />売り上げランキング : 115785<br /><br /><br /><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

自分で本を作りたい人、ブログのコンテンツをまとめてみたい人。そういう方向けに、KDPを使ったセルフパブリッシングの方法を紹介しています。
【告知終わり】
