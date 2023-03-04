---
title : HTML5やらjQueryやらで「Rashita's DashBoard」を作りました
link : 14614
date : Tue, 21 Oct 2014 01:38:23 +0000
categories : ["0-知的生産の技術"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

作業の効率化のため、というお題目でダッシュボードを作りました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot31.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot31-1024x566.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-14615" /></a>

環境はHTML5 + JavaScript。つまり、単なるWebページです。でも、案外いろいろできちゃうものです。

あと、後方支援として、

<a href="http://jquery.com/" target="_blank">jQuery</a>
<a href="http://getbootstrap.com/" target="_blank">Bootstrap</a>
<a href="http://fortawesome.github.io/Font-Awesome/" target="_blank">Font Awesome</a>
<a href="http://startbootstrap.com/template-overviews/sb-admin-2/" target="_blank">SB Admin 2</a>

を使わせていただきました。大いに助かりました。

<H3>ダッシュボードの機能</H3>

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/ee090a7662c73a88fa4c46fd3938ac4c.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/ee090a7662c73a88fa4c46fd3938ac4c-1024x566.png" alt="ee090a7662c73a88fa4c46fd3938ac4c" width="500" height="" class="alignnone size-large wp-image-14616" /></a>

<strong>Headar</strong>には各種クラウドツールへのリンクがあります。まあ、頻繁にクリックするのはTwitterですけれども。ちなみにGoogle+のアイコンが二つあるのは、自分のページと、「<a href="https://plus.google.com/u/0/communities/110281958623092778174" target="_blank">21世紀の知的生産の技術</a>」の両方へのアクセスを確保しているからです。

<strong>Sidebar</strong>はツール系へのリンク。別の自作のツールへのリンクや、WorkFowlyなどへのリンクがまとまっています。

<strong>Maincolumn</strong>は、「作業」するときに必要なリンク集。各種ブログのダッシュボードや、メルマガ管理画面へのリンクがまとまっています。KDPページとかも頻繁に確認するので必須ですね。

<strong>Footnote</strong>は、進行中プロジェクトの概況がまとめられています。

基本的にはブラウザにこのページを常時表示させておき、ここ経由で作業を開始する形になっています。あっちこっち探し回る必要がなく、タスクのワンストップステーションとして機能してくれれば理想です。

<H3>connection with Evernote</H3>

基本的にはただのリンク集なのですが、多少手の込んだことも実装されています。

一つは、テンプレート。sidebarに「テンプレート」という項目があり、それをクリックすると記事の雛形が表示されるようになっているのですが、このデータをEvernoteから持ってきています。詳しく書くと、Evernoteの「テンプレ」というタグが付いたノートの内容を表示しているのです。

※クリックすると
<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot32.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot32.png" alt="screenshot" width="264" height="591" class="alignnone size-full wp-image-14617" /></a>

※テンプレートが表示される
<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot33.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot33-1024x641.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-14618" /></a>

つまり、Evernote上でそのテンプレタグが付いたノートを修正すれば、このページで表示されるテンプレの内容も修正される、ということですね。これは手作業ではなく、スクリプトによる自動作業なので、テンプレタグが付いたノートが新しく作成されれば、その内容も取り込まれます。

同様に、Footnoteの内容もEvernoteのノートから持ってきています。具体的には、プロジェクトノートブックにある、▼MITタグが付いたノートの、頭の部分だけを抜粋してノート表示している、という形です、こちらもEvernoteのノートを修正すれば、ダッシュボードのFootnoteも表示変更されます（タイムラグはありますが）。

※この部分は
<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot34.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot34.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14619" /></a>

※このノートからやってきている
<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot35.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot35.png" alt="screenshot" width="328" height="296" class="alignnone size-large wp-image-14620" /></a>

今のところはFootnoteの形に留まっていますが、将来的にはEvernoteのプロジェクトノートブックにあるノートの内容を良い感じに表示して、一覧できるようにできればベストソリューションかな、というイメージがあります。なかなか実装は大変そうですが。

<H3>どうやって作っているのか？</H3>

このページの作成は、AppleScriptで行っています。

雛形になるhtmlファイルをあらかじめ作成しておき、そこでスクリプトを起動すると、Evernoteから情報を読み取って、その情報をおおもとのhtmlに追加した形で、新規にhtmlファイルを作成する、という流れになっています。で、そのスクリプトが自動的かつ定期的に実行される形です。

さすがにそれを解説し始めると、エントリーが膨大な量になるので今回は割愛。

MacのEvernoteはAppleScriptに対応しているので、結構いろいろなことができちゃいます。

<H3>さいごに</H3>

まあ、うたがいなくマニアックですし、そもそも私が使いやすいようにカスタマイズしてあるので汎用性は著しく低いページです。

が、それはそれとしてEvernoteのノートの内容をこうやって利用するというのも、面白いかなと感じる今日この頃です。