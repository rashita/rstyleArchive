---
title : Evernote for Macのバージョンアップと「タグ」についての基本方針（上）
link : 6934
date : Tue, 22 Nov 2011 03:07:46 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

そういえばEvernote for Macがバージョンアップされていましたね。このバージョンでは、タグの使い勝手が上がっています。
※この辺の記事も参照のこと：<a href="http://lifehacking.jp/2011/11/tag-search-in-toolbar/">ノートブックと多すぎるタグを一発検索できるようになったEvernote for Mac</a>（Lifehacking.jp）

FavoriteBarにある「タグ」を押せば、全部のタグをスライドして表示させることもできますし、文字列を入力して検索することもできます。

<a href="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot3.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot3.jpg" alt="screenshot3" title="screenshot3" width="381" height="134" class="alignnone size-full wp-image-6936" /></a>

これでタグがいくら増えてもへっちゃらですね。

えっ、そんなにタグが増えるものなのか？

もちろん使い方によりますが、ある程度使っているとタグの数は結構増えてきます。

今回はタグ周りの話をちょっと書いてみましょう。
<h3>基本的な方針</h3>
まずノートブックとタグについて。

私自身の方針は、

<ul>
	<li>総ノートブックは「最低限の数」を心がける</li>

	<li>タグは自由気ままに</li>
</ul>



まずこの二つです。

ノートブックの「最低限の数」が一体いくつなのかはいまだに分かりませんが、この基本方針から「必要なさそうなノートブックを見つけたら削除する」という行動方針が生まれてきます。
※スタックを折りたたんだ状態で現状２５個

対してタグは、「とりあえず思いついたものを」という感じです。数に制約はありません。なにせ放り込んでいる情報が多彩なのでタグの数はいくらでも増えていきます。1枚のノートに付けるタグの数は少なくても、存在しているタグの数は結構多いわけです。

基本的にノートブックが情報操作の基盤になっており、数が増えるとごちゃごちゃしてしまうので、できるだけ最小の数を保って一覧性を確保する。タグはノートを検索する際の「補佐」的な位置づけで、一覧性は特に意識しない。こういう使い分けです。

そのため、サイドバーからニッチなタグを探すのが若干面倒になってきていたわけですが、今回の「検索機能」のおかげで随分マシになりました。
<h3>タグの基本的な方針</h3>
タグは、階層を作ることができます。

<strong>親タグ──子タグ──孫タグ──・・・</strong>

こんな感じですね。例えば

<em>仕事術──タスク管理──タスクシュート</em>

こういうタグの関係になるでしょうか。

階層を深く作って、情報の分類をマニアックに細分化することもできますが、私は「孫タグまで」と決めてあります。これ以上深くすると、私の認知力では手に負えないことが目に見えているからです。
※どこにあるか探せない。

が、今回の検索の登場でこれにこだわる必要は少しだけ薄れました。どれだけ階層を深くしてもタグを見つけることは可能です。逆に階層を作らないでのっぺりとタグを並べていっても検索を使えば問題ありません。

が、一応孫タグまでルールは尊重していきたいと思います。別にどっちでもいいんだったら、現状うまくいっているルールを変える必要はありません。

<h3>タグのネーミング</h3>
今回ますます重要になったのがタグの名前付けです。

上に書いた階層構造というのは、あくまで私たちの認知上の問題です。親タグと子タグが、本当の意味で親と子になっているわけではありません。
※親タグのノートを検索したら、それが含まれる子タグのノートも表示される、とかそういう機能はない。

あくまで表示上の見た目問題であって、私たちの所有する脳が情報を見て探すときに「見た目構造化」してあると便利だよね、というところでしかありません。

しかし、タグの名前は「検索」に直接関わってきます。どんな名前を付けるのかは検索において非常に重要です。

さらにFavoriteBar（以下FB）の「タグ」を押したときにリスト形式で表示されるタグの一覧も「名前順」で並びます。サイドバーのタグリストも「名前順」ですが、親タグと子タグを使えば自分なりの分類で仕分けることができます。

対してFBのタグは全てのタグを親子関係一切無視でリスト化します。

この機能の「差」は、ちょっと捻った使い方が可能です。例えばジャンルの大きなカテゴリで親タグを作っていたとしましょう。

A
B
C
D

この４つの親タグの下に、子タグが並びます。

A -Aa,Ab,Ac
B -Ba,Bb,Bc
C -Ca,Cb,Cc
D -Da,Db,Dc

こんな感じですね。もし、この時それぞれの子タグで「よく使うもの」があったとします。参照頻度の高いタグ、ということです。

その場合、その参照頻度の高いタグだけ、共通のルールで少しだけ名前を変えるとピックアップしやすくなります。

そのルールを仮に「頭にドットを付ける」としたとしましょう。するとこうなります。

「Ab」→「.Ab」
「Bc」→「.Bc」
「Ca」→「.Ca」
「Db」→「.Db」

こうしておくと、FBのタグを押したときに、上の四つがリストの最初に並ぶことになります。

サイドバーのタグ表示がどれだけ複雑になっていても、それぞれのタグが別の親タグに所属していても、「よく使うタグは、頭にドットを付ける」というルールを作っておけば、即座にアクセスできるようになる、というわけです。

これはあくまで一例ですが、タグの名前の付け方は少し工夫するだけでかなり使い勝手があがります。
<h3>さいごに</h3>
長くなってきたので、続きは次回に。次回は私が使っている実際のタグのネーミング方法なんかを紹介します。

<a href="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2011/11/screenshot.jpg" alt="screenshot" title="screenshot" width="198" height="283" class="alignnone size-full wp-image-6937" /></a>
<strong>
▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 3930<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>



