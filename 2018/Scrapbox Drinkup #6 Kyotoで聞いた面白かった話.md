---
title : Scrapbox Drinkup #6 Kyotoで聞いた面白かった話
link : 25978
date : Sat, 27 Oct 2018 02:37:14 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox","scrapbox-drinkup"]
draft : false
author : 倉下忠憲
---

10月26日に行われた<a href="https://nota.connpass.com/event/103825/"> Scrapbox Drinkup #6 Kyoto Edition </a>に参加してきました。

<a href="https://scrapbox.io/scrapbox-drinkup/Scrapbox_Drinkup_%236_Kyoto">Scrapbox Drinkup #6 Kyoto - scrapbox-drinkup</a>

京都での実施ははじめて、ということで、開催場所はNotaさんのオフィスです。

※オフィスの本棚に『Scprapbox情報整理術』オブジェクトが！
<a href="https://rashita.net/blog/?attachment_id=25979" rel="attachment wp-att-25979"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/AA3CE3AB-317A-414A-BD7E-E21EE115E156-12971-0000033BD8A5C307.jpg" alt="" width="1024" height="1365" class="alignnone size-full wp-image-25979" /></a>

<h2>登壇内容</h2>

今回は三人の方の発表がありました。

<ul>
<li>Scrapboxの最新情報 @shokai</li>
<li>Scrapboxのインターンの話 @rakusai</li>
<li>ページの繋がりを視覚化 @daizplus</li>
</ul>

それぞれ少しだけご紹介します。

<h3>Scrapboxの最新情報</h3>

shokaiさんからは、ここ最近実装されたScrapboxの新機能を紹介してもらえました。

詳しくは以下のページを見てください、というところで済ませたいのですが、

<a href="https://scrapbox.io/scrapbox-drinkup/Scrapbox%E6%9C%80%E6%96%B0%E6%83%85%E5%A0%B12018%2F10_(shokai)">Scrapbox最新情報2018/10 (shokai)</a>

とりあえず、いくつかの新機能をご紹介。どれもすでに実装されているやつです。

○モバイルのドロアーメニュー

<a href="https://gyazo.com/9678e625865bc92843aa6eea85b951d7"><video alt="Video from Gyazo" width="408" autoplay muted loop playsinline><source src="https://i.gyazo.com/9678e625865bc92843aa6eea85b951d7.mp4" type="video/mp4" /></video></a>

これまでのモバイルのメニューは、プロジェクトがたくさんあると、下の方が選択できなくてキーッってなってたんですが、それが解消されています。というか、紹介されるまで、このバグが直っていたことに気がついていませんでした。便利さって、人を盲目にしますね。

○Service Workerでの高速化

「Service Worker」が何なのかはまったくわかりませんが、リンクをホバーした段階で、ページを先読みしているという話を聞いて、めちゃくちゃ感心しました。おかげで、ページを飛んだときの表示がかなり速くなったとのこと。

<a href="https://scrapbox.io/shokai/ServiceWorker%E3%82%92production%E3%81%A7%E4%BD%BF%E3%81%A3%E3%81%A6%E3%82%8B%E8%A9%B1">ServiceWorkerをproductionで使ってる話 - 橋本商会</a>

○ランダムジャンプボタン

気がついている人は多いでしょうが、ページの左側にランダム表示させるためのボタンが付いています。

<a href="https://scrapbox.io/scrapboxlab/%E3%83%A9%E3%83%B3%E3%83%80%E3%83%A0%E3%82%B8%E3%83%A3%E3%83%B3%E3%83%97%E3%83%9C%E3%82%BF%E3%83%B3">ランダムジャンプボタン - Scrapbox研究会</a>

これをドンドン押していって、面白いページと遭遇できる確率をpとするとき、そのpが一定以上であれば、Scrapox健全性が高い、という言い方ができるかもしれませんね。まあ、どうでもいい話ですが。

ちなみに、これもService Workerのおかげで、高速にページを「めくって」いけます。

○merge機能

先にリンクを作ってから、ページを作成する場合はほとんど遭遇しないのですが、ページ新規作成→本文、という形をとると、たまに発生するのが同名のタイトルを持つページの存在です。名前の衝突、という奴ですね。

で、これまでは、「おいおいあんちゃん、もうそのページはあるぜ」と教えてくれるだけだったのですが、現状は「いっそ、マージしちゃう？」と聞いてくれます。で、「するする」と答えると（ボタンを押すと）、すでにあるページにappendする形で統合されます。

この機能を悪用すれば、たとえば３つあるページを統合したいときに、それぞれのページタイトルを同一にすることで実現が可能となるわけですが、まあ基本的に分割方向がScrapbox的なので、こういう話は聞き流してください。

○アカウント削除機能

『Scrapbox情報整理術』を書いたときにはなかった結構大きな機能です。

複数アカウントとか作っちゃったけど、別にいらなくなった、みたいな場合に活躍しますね。

やり方は、以下。

<a href="https://scrapbox.io/help-jp/%E3%82%A2%E3%82%AB%E3%82%A6%E3%83%B3%E3%83%88%E3%82%92%E5%89%8A%E9%99%A4%E3%81%99%E3%82%8B">アカウントを削除する - Scrapbox ヘルプ</a>


というわけで、簡単に機能をご紹介しました。全体が気になる方は、以下のページをどうぞ。

<a href="https://scrapbox.io/scrapbox-drinkup/Scrapbox%E6%9C%80%E6%96%B0%E6%83%85%E5%A0%B12018%2F10_(shokai)">Scrapbox最新情報2018/10 (shokai)</a>

<h3>Scrapboxのインターンの話</h3>

rakusaiさんからは、今年の夏にインターン生が来て、そこでもScrapboxが活躍した、というお話を。

これまた、以下の記事をご覧ください、でお茶を濁したいところです。

<a href="https://scrapbox.io/shokai/%E3%82%A4%E3%83%B3%E3%82%BF%E3%83%BC%E3%83%B3%E3%81%8C%E6%9D%A5%E3%81%A6%E3%81%9F_2018%E5%A4%8F">インターンが来てた 2018夏 - 橋本商会</a>

そうなのです。こうして書いておけば、読む気になった人はその知見が得られます。Notaさんでは、技術的なことや、アイデアに対する議論などもすべてScrapboxに残されていて、ピカピカの新人でも、それらを追いかけることができます。半年もROMる必要はありません。

特に、結論だけでなく、議論の過程そのものが残されているので、思考の筋や理路を追いかけることができる点は大きいでしょう。ポイントは、わざわざそうしたドキュメントを作ろうとはしていなくて、単にそれまでWorkingだった（≒実際に仕事で使っていた）ものが、Archiveとしても機能してる（しかも、いつでもactiveにできる）のが重要です。

この辺の話は、企業というか組織体のナレッジマネジメントにおいてコアになってくる話だと思います。

あと、会議のアジェンダを作ったら、会議しなくても良くなった、という話はとてもいいですね。「そもそも、会議なんていらんかったんや」的な。

<h3>ページの繋がりを視覚化</h3>

daizplusさんは、本体の機能とはまったく関係ない、ご自身の「実験」を紹介してくださりました。

<a href="https://scrapbox.io/scrapbox-drinkup/%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%AE%E7%B9%8B%E3%81%8C%E3%82%8A%E3%81%AE%E8%A6%96%E8%A6%9A%E5%8C%96_(daiiz)">ページの繋がりの視覚化 (daiiz) - scrapbox-drinkup</a>

で、ここで提示されている話が、たいへん面白いです。

Scrapboxでは、[ページタイトル]という記法と、#ページタイトルという記法で、ページリンクを作成できます。で、これは一般的に、「文中リンク」と「ハッシュタグ」という使い方がされます。

[ページタイトル]→文中リンク
#ページタイトル→ハッシュタグ

別にそう使わなければならないルールはないのですが、ついついこういう風に使うのは、私たちが他の情報ツールに慣れているからでしょう。たぶんですが、バリバリのインスタグラマーなら、「#Scrapbox は #最高の情報ツール で、#是非とも広まってほしい」みたいな書き方も全然OKでしょうが、Twitterユーザーにとっては違和感しかないでしょう。

で、文中リンクとハッシュタグの違いというのは、基本的には実体ページのあるなし、です。

具体例を挙げれば、以下が「ハッシュタグ的な」ページです。

<a href="https://rashita.net/blog/?attachment_id=25980" rel="attachment wp-att-25980"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-72.png" alt="" width="1027" height="725" class="alignnone size-full wp-image-25980" /></a>

複数のページを、ゆるやかに関連づけるだけの存在。それ自身の内側に情報を持たないページ。これが「ハッシュタグ的な」ページです。

で、Scrapboxでは、できるだけこういうタイプのリンクではなく、ちゃんと実体化させて、本文を書いたページを作った方が、より面白く・使いやすくなる、という話を『Scrapbox情報整理術』でも書きました。

daizplusさんの実験は、それをデータ的に裏付けるものです。具体的には、ページのつながりを視覚化して表現し、文中リンク的なものとハッシュタグ的なもので、つながり方がどう違うのかを私たちに見せてくれます。

で、紹介されたツールで、私の「<a href="https://scrapbox.io/rashitamemo/">倉下忠憲の発想工房</a>」のページのつながりを視覚化してみました。ページ総数が700にも満たないので、若干心許ないですが、それでもはっきりわかる結果が得られます。

<a href="https://rashita.net/blog/?attachment_id=25981" rel="attachment wp-att-25981"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-73.png" alt="" width="1426" height="754" class="alignnone size-full wp-image-25981" /></a>

こちらは、「文中リンク」で見た場合の、ページのつながりです。閾値は７（7個以上のつながりを持つページのみを表示）を選択しました。いろいろなページがつながっているのがわかるかと思います。その中でも、「Scrapbox」「断片」「カード」がハブ的に機能しているのもわかります。

では、「ハッシュタグ」バージョンはどうなるでしょうか。

<a href="https://rashita.net/blog/?attachment_id=25982" rel="attachment wp-att-25982"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-74.png" alt="" width="1432" height="748" class="alignnone size-full wp-image-25982" /></a>

表示されている数自体も少ないですが、つながりはもっと少なくなります。

考えてみれば、これも当然です。たとえば、表示されている「断片からの創造」と「幸福論」は交じり合うことがありません。言い換えれば、一つのページにこのハッシュタグが同居することはありません。なぜなら、これは「カテゴリ」だからです。カテゴリ（範疇）というのは、それぞれ別の要素に対して排他的なのです。「化学」は「国語」ではなく、「社会」でも「保健」でもありません。それがカテゴリ、ということの意味であり役割です。

つまりです。

こういう「ハッシュタグ的」な使い方は、その内側で複数のページ（情報）をグルーピングする機能はあっても、「ハッシュタグ的」そのものの連合は発生しません。別の言い方をすれば、ハッシュタグ的にグルーピングされている個々のページは、そのグルーピングを越境しないのです。

それって何かと言えば、ツリー構造です。ようするに、頭の中にある恣意的なツリー構造をネットワーク構造に持ってこようとするのが、こうした「ハッシュタグ的」な使い方、ということになります。

だからこそ、Scrapboxでは、ハッシュタグ的ではなく文中リンク的に記述するのが推奨されます。だって、ツリー構造ならば別のツールでも簡単に作れるのですから。特性を活かすならば、よりネットワーク的であった方がよいでしょう。

つまり、別に#でリンクを作ってはいけないわけではないし、また、中身が空っぽのページを作ってはいけないわけでもありません。単に、カテゴリ（排他的なグルーピング）をして、情報を分類しただけで、「整理した気持ち」になっていたのでは、情報の広がり（特に意外な広がり）は増えていかないので気をつけよう、ということです。

とは言え、ハッシュタグ的なものが、完全に無意味・無価値というのでもありません。先ほどの視覚化を両方を混ぜたバージョンで表示してみましょう。

<a href="https://rashita.net/blog/?attachment_id=25983" rel="attachment wp-att-25983"><img src="https://rashita.net/blog/wp-content/uploads/2018/10/screenshot-75.png" alt="" width="1435" height="751" class="alignnone size-full wp-image-25983" /></a>

「断片からの創造」が非常に大きなハブとなり、しかも密接なつながりが生まれています（ひっぱったらメッチャ面白かったです）。たぶん、この二つは補完的に機能してくれるのでしょう。密なネットワークを作るものと、ゆるやかで排他的なグループを作るもの。むしろ、それが混在できる稀有なツールがScrapboxなのかもしれません。

<h2>さいごに</h2>

というわけで、非常に面白いお話が聞けたScrapbox Drinkup #6でした。

一応私も急遽作成したスライドでLTに参加しました。中身は以下をご覧ください。

<a href="https://scrapbox.io/scrapbox-drinkup/%E7%89%A9%E6%9B%B8%E3%81%8D%E3%81%AEScrapbox%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9(rashita)">物書きのScrapboxの使い方(rashita) - scrapbox-drinkup</a>

ちなみに、生ビールとして提供されていた西陣麦酒さんのIPA柚子無碍（YUZUMUGE）は無茶苦茶うまかったです。はい。

<a href="http://nishijin-beer.com/news/%E3%83%93%E3%83%BC%E3%83%AB%E3%81%AE%E3%81%94%E7%B4%B9%E4%BB%8B%EF%BC%88%EF%BC%91%EF%BC%89%E3%80%80%E3%80%8C%E6%9F%9A%E5%AD%90%E7%84%A1%E7%A2%8D%EF%BC%88%E3%82%86%E3%81%86%E3%81%9A%E3%81%86%E3%82%80/">ビールのご紹介（１）　「柚子無碍（ゆうずうむげ）」 | 西陣麦酒計画(Nishijin Ale Project)</a>

というわけで、こちらからは以上です。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.10.27</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 14,906<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
