---
title : Evernote企画6th:第三回：HTMLファイルで「リフィル」を作る
link : 6005
date : Wed, 15 Jun 2011 03:32:11 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernote企画6thエントリー:
<a href="https://rashita.net/blog/?p=5989">Evernote企画6th:第一回：アップデートで追加された機能の確認</a>
<a href="https://rashita.net/blog/?p=5999">Evernote企画6th:第二回：ノートの見た目にこだわる</a>

<hr>
前回、簡単に紹介した「テンプレ」ノート。作成に少々手間がかかるものの、一度作ってしまえば後はコピーで使い回せます。少なくとも単にテキストや味気ないテーブルを並べただけのノートよりは見返しやすいノートになるでしょう。

今回はいくつかサンプルを紹介してみます。

<h3>タスクリスト</h3>
Evernoteで表組みを作ると、だいたいこんな感じになるでしょう。
<a href="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot6.png" alt="screenshot" title="screenshot" width="500" height="180" class="alignnone size-full wp-image-6006" /></a>

あまり「見た目」が良いとはいえませんね。

これも、HTMLで表組みを作って、それをクリップすることで見栄えの良いテーブルが作れます。
<a href="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot14.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot14.png" alt="screenshot1" title="screenshot1" width="500" height="420" class="alignnone size-full wp-image-6007" /></a>
※マージン・パディングが甘いのはご愛敬。

日付、タスク名、着手日、チェックボックスと必要最低源の確認はできますね。

<h3>プロジェクトノート</h3>
一つのプロジェクトに関するデータをまとめるためのテンプレです。
<a href="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot22.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot22.png" alt="screenshot2" title="screenshot2" width="500" height="380" class="alignnone size-full wp-image-6008" /></a>

例えば、こんな感じで記入できます。

<a href="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot3.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot3.jpg" alt="screenshot3" title="screenshot3" width="500" height="400" class="alignnone size-full wp-image-6010" /></a>
※上記は実際に使っているものにプライバシー保護処理を加えたものです。

タスクはチェックボックス、関連情報はノートリンク、関係者は画像、など好き勝手に情報を追記できるのがEvernoteの強力なポイントです。

例えば、関係者の部分にその人の名刺ノートのノートリンクを貼るといった使い方もできます。

<h3>自著データ</h3>
こちらも上と似たような感じですが、「出版」に関するデータをまとめておくもの。

<a href="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot41.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot41.png" alt="screenshot4" title="screenshot4" width="500" height="380" class="alignnone size-full wp-image-6011" /></a>

基本データから、書籍のタイトル画像、あるいは書評のウェブクリップへのリンクをまとめる、という使い方ができます。

<h3>さて、どう作る？</h3>
今回紹介したテンプレは基本的にHTML＋CSSでウェブページをつくり、それをクリップするという形でEvernoteに取り込んでいます。

Dropboxのパブリックにサンプルを上げておきましたので、気になる方は実際にブラウザで表示→クリップしてみてください。
※Firefox用に調整してありますので、その他のブラウザでは違った表示になるかもしれません。

<a href="http://dl.dropbox.com/u/554861/task1.html">http://dl.dropbox.com/u/554861/task1.html</a>
<a href="http://dl.dropbox.com/u/554861/project2.html">http://dl.dropbox.com/u/554861/project2.html</a>

問題は、この「作り方」です。普通にウェブページをクリップするとわかりますが、大方のCSSは無視されます。CSSファイルと、ページの＜Script＞内で指定されているCSSは効かないようです。

と、いうことは一つ一つのタグに対してスタイルを指定していくという作業が必要なわけですね。Webデザイン的に「ちょっと考えられ無い」作業です。

この辺の話題が分からない方は「デジカメで撮影した写真一つ一つに自分で連番を振っていく」ぐらいの面倒な作業だ、という認識でOKです。

というわけで、「面倒ならスクリプトを作ればいいじゃん」というありがちな発想で、applescriptで色とマスの数指定して、自動的にその面倒なHTMLを自動生成するアプリを作ってみました、＿＿＿と発表したいところですが、今のところそこまでは行ってません。

現状は、望むマス数の分の「タスクリスト」を作るスクリプトが手許にあるだけです。
※テーブル部分を任意の回数リピートするだけの簡単なもの。

とりあえず、手でHTML書いて→コード化に何が必要なのか理解して→アプリを作ろう、の二段階目にようやく来たところです。まあ、いろいろ技量が足りていないので、歩みが遅いのは仕方ないですね。

<h3>さいごに</h3>
ようは、テーブルのデザイン（色・マス数）を指定すれば、タグに直接スタイル指定したものが出力されるアプリがあれば、お手軽に「リフィル」が作れるということですが、現状はサンプルで作った「リフィル」にそこそこ満足してしまっているので、アプリ作成の優先順位は低くなっている現状です。

あと、画像ではないので、ノートの「サマリービュー」の表示はあんまりCoolではありません。「サムネールビュー」だとイイカンジです。
<a href="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot51.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/06/screenshot51.png" alt="screenshot5" title="screenshot5" width="340" height="334" class="alignnone size-full wp-image-6012" /></a>

こういう「自作」の可能性があるのもEvernoteの面白いところですね。上に紹介したようなアプリをすでに作っているよ、という奇抜な発想をお持ちの方がおられましたら、是非シェアしていただきたいところです。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540728/goodpic-22/" target="_top">EVERNOTE「超」仕事術</a></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540728/goodpic-22/" target="_top"><img src="http://ecx.images-amazon.com/images/I/51D2v1-KakL._SL160_.jpg" border="0" alt="EVERNOTE「超」仕事術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2010-08-18<br />売り上げランキング : 15071<br /><br /><br /><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540728/goodpic-22/" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540817/goodpic-22/" target="_top">EVERNOTE「超」知的生産術</a></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540817/goodpic-22/" target="_top"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 6031<br /><br /><br /><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540817/goodpic-22/" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

