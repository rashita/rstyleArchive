---
title : Evernoteのノートをテンプレートとして活用する
link : 14218
date : Mon, 01 Sep 2014 04:29:33 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernoteマニアックワールドへようこそ。

以下の記事を読みました。

<a href="http://worldcafe-emanon.blogspot.jp/2014/08/evernoteapplescript.html" target="_blank">ド素人の僕がAppleScriptを使ってEvernoteのテンプレートを呼び出してみた</a>（World Cafe）

<blockquote>普通にフォーマットを読み込むAppleScriptを誰か書いてくれないかなあ〜</blockquote>

AppleScriptを使ったノート・テンプレートの活用です。

テンプレートは、メールの雛形などで活躍しますが、議事録や日誌、メルマガのフォーマットなんかにも便利です。私もよく利用しています。

が、上の記事で紹介されているスクリプトでは、いちいちノートブックが作成されてしまいます。それはちょっと嫌ですね。あと、enexファイル（ノートをインポートしたときに作成されるファイル）の準備も必要。これは面倒です。

もうちょっと、なんとかしてみましょう。

<H3>ベーシックな解決</H3>

もしかしたら、あまり知られていないのかもしれませんが、Macクライアントではノートをテンプレート的に活用する機能が標準装備されています。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot.png" alt="screenshot" width="372" height="396" class="alignnone size-full wp-image-14219" /></a>

ノートをcontrolクリックし、出てきたメニューから「ノートブックにコピー」を選択すれば、同じ内容のノートが選んだノートブックに新規作成されます。まさにテンプレート向けの機能です。

一度選んだノートブックは、「再度○○○にコピー」としてメニューに表示されるようになるので、さらに利便性はアップ。基本的に、この機能を使えば問題ないでしょう。

さらに活用するには、こうしたテンプレート的ノートをサイドバーのショートカットに置いておくのがベターです。あるいは、テンプレートノートを探す検索結果を保存して設置しておくのも良いですね。

<H3>テンプレート・スクリプト</H3>

が、そうは言っても、その手順すら面倒、という場合に備えて、スクリプトを書いてみました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot2.png" alt="screenshot" width="499" height="524" class="alignnone size-large wp-image-14221" /></a>

以上のようなノートがあるとしましょう。「テンプレート」というタグがついています。

スクリプトを起動。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot1.png" alt="screenshot" width="366" height="324" class="alignnone size-full wp-image-14220" /></a>

ノートを選択。すると、

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot3.png" alt="screenshot" width="500" height="323" class="alignnone size-full wp-image-14223" /></a>

このようにノートが作成されます。

ただし、元のノートのタグは引き継ぎません。また、ノートの作成場所はデフォルトノートブックです。この辺はコードを書き換えれば対応できます。

スクリプトは以下。

<script src="https://gist.github.com/rashita/501d0918f4c0075c1d00.js"></script>

非常に残念ながら、この方法だとチェックボックスがコピーされません。回避するアイデアはあるのですが、実装する時間がないので今回はパス。

<H3>テンプレート・スクリプト・アレンジ</H3>

しかし、考えてみると、私に関してはEvernoteをエディタとしては使っていません。テンプレートの保存場所ではあるものの、執筆場所ではないのです。

だから今までは「よし、メルマガ作ろうか」と思った際は、Evernoteでテンプレートノートを探す→全文コピペ→CotEditorで新規ファイル作成→そこにまるっと貼り付け、という手順を踏んでいました。

で、上のスクリプトを書いたとき思ったんです。これを転用できるのではないか、と。

<script src="https://gist.github.com/rashita/76ca2500c47b479006c7.js"></script>

ほとんど動作は同じです。一番最後が、Evernoteにノートを新規作成するのではなく、CotEditorで新規ファイルが作られるだけです。まさに私専用スクリプト。一回当たり30秒ぐらいの手間が省けそうです（体感）。

<H3>さいごに</H3>

細かいカスタマイズに関しましては、ググるなりなんなりして、ご自分で実施してください。

あと、チェックボックスも対応可能なスクリプトを作成された偉大な方は、ご一報いただければ幸いです。

<strong>▼こんな一冊も：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 231108<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

