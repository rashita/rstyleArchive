---
title : AppleScriptでEvernoteを操作する 第二十回
link : 23574
date : Sat, 23 Dec 2017 02:42:54 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

いよいよ最終回です。今回は振り返り＆まとめとなります。

これまでの回は以下から確認できますので、どうぞ。

<a href="https://rashita.net/blog/?tag=%e2%89%aaapplescrpt%e3%81%a7evernote%e3%82%92%e6%93%8d%e4%bd%9c%e3%81%99%e3%82%8b%e2%89%ab" title="≪AppleScrptでEvernoteを操作する≫ – R-style">≪AppleScrptでEvernoteを操作する≫</a>

<h2>二つの方向性</h2>

Macでは、AppleScriptという簡易言語を用いることによって、Evernoteをより高度に（あるいはマニアックに）操作することができます。

基本的な方向性は以下の二つ。

<ul>
<li>処理の自動化</li>
<li>データを他のアプリケーションに受け渡し</li>
</ul>

「処理の自動化」では、人間の手で行うと非常に面倒な処理を、ほとんど一瞬で実行できます。たとえば、似た内容のノートを365枚作成する、すべてのノートのタイトルの冒頭に『R-style:』をつける、すべてのノートに日付を書き加える、といったことです。つまり、

・ノートの自動作成
・ノートのメタ情報操作
・ノートの内容の操作

といったことが手軽に行えます。まだ、条件分岐や入力ダイアログを使うことで、より柔軟かつ繊細な処理も可能となります。

ここで使用されるAppleScriptのコマンドは、

・create note
・append 

の二つで、前者が新規作成、後者が追記を担当してくれます。

さらに、検索や選択されているノートの情報を取得することで、そのメタ情報を操作することもできました。

■

「データを他のアプリケーションに受け渡し」では、Evernoteのノート内容を取得し、それを利用できます。

使えるのは、ノートのメタ情報である、HTML content。これを使いノートの情報を取り出せば、たとえば、別のエディタアプリに書き出したり、ノートの内容をWebブラウザで閲覧したりも可能です。

また、HTML contentを使うことで、二つのノートの内容を取得し、そこから一つの新しいノート、つまりマージされたノートを作り出すこともできます。標準のマージのデザインが気にくわない場合は、こうした方法でマージを実行してみてもよいでしょう。スクリプトの書き方によっては、Aのノートに、Bのノート内容をappendする、みたいなこともできます。この辺は工夫次第です。

<h2>さいごに</h2>

この連載では、AppleScriptの非常に基本的な話と、その中で使えるEvernote用のコマンドをいくつか解説してきました。AppleScriptの構文もEvernoteのコマンドも完全には紹介しきれていませんが、それでも必要最低限のスクリプトはこれで書けるはずです。

ぜひとも、自分で困っているEvernoteの煩雑な操作をAppleScriptで簡略化してみてください。きっと、もっと、Evernoteのことが好きになると思います。

Enjoy Evernote!

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.23</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 68,656<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.23</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 60<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


