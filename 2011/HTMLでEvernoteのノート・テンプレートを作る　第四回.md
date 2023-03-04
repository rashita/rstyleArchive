---
title : HTMLでEvernoteのノート・テンプレートを作る　第四回
link : 6348
date : Sat, 13 Aug 2011 04:33:12 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

連載ものです。過去のエントリーはこちら。

<a href="https://rashita.net/blog/?p=6327">HTMLでEvernoteのノート・テンプレートを作る　第一回</a>
<a href="https://rashita.net/blog/?p=6335">HTMLでEvernoteのノート・テンプレートを作る　第二回</a>
<a href="https://rashita.net/blog/?p=6338">HTMLでEvernoteのノート・テンプレートを作る　第三回</a>

連載は、一応今回で終了。本来はもっと詳しくHTMLとかCSSについて解説しようかと考えていましたが、一体何のブログなのか分からなくなってきそうなので、今回で一区切りにしておきます。

<h3>タスクリスト</h3>
<a href="https://rashita.net/tool/evernote/task1.html">タスクリストサンプル</a>

上記のページを、クリップしてEvernoteに取り込んでください。左から、締め切り、タスク名、着手したかどうか、終わったかどうか、です。使用時にはSTとCKの欄に一つ一つチェックボックスを挿入していくとGoodです。
※二回目以降はこれをコピーして使うので、そういう手間は必要無し。

これはHTMLの＜TABLE＞を使ったタスクリストです。＜TABLE＞は表組みを追加するタグです。

シンプルな例を挙げれば、次のような感じになります。

[css]
&amp;lt;html&amp;gt;
&amp;lt;head&amp;gt;
&amp;lt;title&amp;gt;Pink&amp;lt;/title&amp;gt;
&amp;lt;/head&amp;gt;
&amp;lt;body&amp;gt;
&amp;lt;Table&amp;gt;
&amp;lt;TR&amp;gt;
&amp;lt;TD&amp;gt;ここがマス１&amp;lt;/TD&amp;gt;
&amp;lt;TD&amp;gt;ここがマス２&amp;lt;/TD&amp;gt;
&amp;lt;/TR&amp;gt;
&amp;lt;/Table&amp;gt;
&amp;lt;/body&amp;gt;
&amp;lt;/html&amp;gt;
[/css]

これにTRとTDを追加していけば、いくらでも大きいサイズの表組みを作れます。また前回紹介した背景色の指定を＜TD＞に行うことで、好みのセル色にすることができます。

上のサンプルのコードはあまりにも長いので、ブラウザでページを表示させて「ページのソースを表示」あたりで確認してください。

テーブルについて詳しく知りたい方は、とほほさんの、「<a href="http://www.tohoho-web.com/html/table.htm">&lt;table&gt; - テーブル（表）</a>」を参考にしてください。というかHTMLやCSSはここで調べれば大抵問題は片づきます。

<h3>プロジェクトノート</h3>
<a href="https://rashita.net/tool/evernote/project2.html">プロジェクトノートサンプル</a>

ページの背景色指定、＜DIV＞や＜TABLE＞の要素を組み合わせて作ったのが、上記のページ。これも実際にEvernoteにクリップしてみてください。

その後、「進捗日誌」の部分に何か書いてみてください。改行を入れると罫線が細かいドットになっていると思います。ソースの部分で言うと、

style="border-bottom:1px dotted gray;"

が、これにあたります。以前書いた「改行を入れると同じ要素を繰り返す」という現象を利用して、罫線を作っています。

上のスタイルシートは、下の線を、１ｐｘの太さで、ドットで、灰色にしなさいという指示です。ｐｘの前の数字を大きくすれば、線が太くなります。dottedの部分は、他にもdashed（粗い点線）、solid（実線）、double（二重線）などがあります。
※この辺も、とほほさんの「<a href="http://www.tohoho-web.com/css/reference.htm#border">border</a>」あたりを参考に。

その他の要素については、ソースを確認してみてください。

<h3>さいごに</h3>
というわけで、後半ものすごく駆け足になりましたが、Evernoteのテンプレ作りの基本を紹介してみました。実際詳しく紹介していくと、HTML講座になってしまうので、こまかい部分は「とほほ」さんを参考にしてください。

基本的に使う要素は、＜DIV＞＜TABLE＞あたりで事足りるはずです。スタイルシートは背景色(background-color)、テキストの色（color)、フォントサイズ(font-size)、あたりが使えると思います。

デジタルの「ノート」は、自分の好みのテンプレを作るというのが、なかなか難しいものですが、Evernoteであれば、HTMLとCSSの簡単な知識があれば、割合好きな感じに作れます。その自由さも、個人的にはEvernoteの魅力の一つです。
<strong>
▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540728/goodpic-22/" target="_top">EVERNOTE「超」仕事術</a></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540728/goodpic-22/" target="_top"><img src="http://ecx.images-amazon.com/images/I/51D2v1-KakL._SL160_.jpg" border="0" alt="EVERNOTE「超」仕事術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2010-08-18<br />売り上げランキング : 35570<br /><br /><br /><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540728/goodpic-22/" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540817/goodpic-22/" target="_top">EVERNOTE「超」知的生産術</a></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540817/goodpic-22/" target="_top"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 26158<br /><br /><br /><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863540817/goodpic-22/" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>


