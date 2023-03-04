---
title : テキストエディタ風ToDo管理のMacアプリ「TaskPaper」を買ってみた
link : 5555
date : Wed, 06 Apr 2011 05:03:38 +0000
categories : ["「タスク」の研究"]
tags : ["applescript","evernote","mac","taskpaper"]
draft : false
author : 倉下忠憲
---

いつ本家ブログを開始されるのかワクテカの<a href="http://twitter.com/synkuro">@synkuro</a>さんが紹介されていたので、ちょっと興味を持って購入。

<a href="http://b2log.posterous.com/mac-taskpapermac-app-store">[Mac] テキストエディタのようなタスク管理アプリ『TaskPaper』がMac App Store登場記念でセール中</a>(b2log/p)

<blockquote>
見た目ほとんどテキストエディタのような超絶シンプルさと軽快な動作で一部から絶大な人気を誇る（？）タスク管理アプリ『TaskPaper』がMac App Storeに登場しました。現在リリース記念で金曜日までセールやってます。

何と$29.99が$4.99で、日本のMac App Storeでは600円！これは安い。
すでにiPhone・iPad対応のユニバーサルアプリがApp Storeでリリースされていますが、こちらは1,200円ですからね。このMacアプリが600円というのがいかに破格か分かって頂けると思う。
</blockquote>

最近はEvernoteでだいたい何でも管理していますが、それでも「タスクマネジメント」系のアプリには興味がつきるところがありません。あんまり高価なものをホイホイ試すわけにはいきませんが、600円ぐらいであればまあ「遊び」の範囲に留められます。とりあえずセールということで、買ってみました。

使ってみた感じは、シンプルで直感的。小難しさは必要なく、テキストエディタでタスク管理をする感覚で扱えます。

実際にどのような動作なのかは、紹介動画を見てもらうのが一番です。

<iframe title="YouTube video player" width="640" height="390" src="http://www.youtube.com/embed/MVH6dP94R-k" frameborder="0" allowfullscreen></iframe>
<h3>簡単な説明</h3>
一応簡単に説明しておきます。

<img src="https://rashita.net/blog/wp-content/uploads/2011/04/window-grab-300x216.png" alt="こんな画面です" title="こんな画面です" width="450" height="324" class="alignnone size-medium wp-image-5556" />

TaskPaparの単位になるのはプロジェクトです。このプロジェクトの中に、ノート（単なるテキスト）とタスク（頭に"ー"がついたもの）を含めることができます。また、テキストエディタと同じようにTabボタン一つで階層化することができますが、タスクを階層化はあくまで表示上だけです。つまり、上位タスクを消したからといって下位タスクがdoneになるわけではありません。
※同様のシンプル系タスク管理のGoogleTaskの場合はきちんと階層化されます。

またプロジェクトの中にプロジェクトを作ることもできます。この場合はサブプロジェクト的な扱いになりますが、使い勝手的にあえてやる必要があるのかは謎です。サンプルウィンドウをご覧になるとわかりますが、ノート＋タスク、ノート＋タスクの組み合わせが「サブプロジェクト」の切り方になっているので、わざわざ新規でサブプロジェクトを立ち上げる必要性はあまりありません。

タスク（頭に"ー"がついたもの）は、"ー"をクリックすればタスク名に取り消し線が入り、完了扱いとして、@doneが付きます。
※@については下記参照

ちなみに、この"ー"マークをDrag&Dropすればタスクを移動できます。シンプルながら表示順番の変更やタスク間の移動を直感的に行えるというのがこのアプリの魅力でもあります。

完了したタスクはそのまま表示させておくこともできますが、メニューの「Archive Done Tasks」を選択すれば「Archive」というプロジェクトに移動されます。その際@project(所属していたプロジェクト名)も自動的に添付されます。

これが基本的な動作です。ここに先ほど出てきた@が加わります。

<h4>@でタグ管理</h4>
タスク管理系のアプリになれている方に説明は不要だと思いますが、@文字列はTagです。優先順位などを含めたコンテキストの管理に使うことができます。先ほどの@doneは完了、つまりタスクの状態を示すものですし、標準で用意されている @priority(1)は優先順位を表すものです。何に使うのかというと、「検索」です。標準では「プロジェクト名」「タグ名」がリストから検索できるようになっています。

加えて、複数条件の検索も可能です。つまり「プロジェクトA」の「@priority」が付いたタスクを探すというような使い方ですね。右上の検索バーを使えばそれが可能です。

<h4>ようするにあれ</h4>
と、ここまで書いてきたんですが、要するにEvernoteと似たような感じだ、ということです。「プロジェクト」がノートブック、「タグ」がタグ、だと書いておけばこのBlogの読者さんにはAll OKでしょう。違いは「保存された検索」のあるなしと、D&Dの違いです。

Evernoteの場合、プロジェクトをノートブックに見立てて、1タスク1ノートにすればD&Dで簡単にプロジェクト間でタスクを移動させることができます。しかし、この場合「閲覧性」が若干下がります。しかし閲覧性を優先させてプロジェクトの区切り（サブプロジェクト）ごとにノートを作成すると、中に含まれているタスク（チェックボックス）はD＆Dでは移動できません。
※コピペが必要。

同時に管理出来る情報では当然Evernoteに勝るものではありませんが、複雑なことはできるだけ考えたくない、他人とワークをシェアすることもない、画像とかアイコンとかは不要という場合、軽い動作でシンプルな使い方がよい、というアプリをお望みの場合は一つの選択になるかもしれません。

<h3>UIショー</h3>
ちなみに標準的なエディタ風UI以外にもいくつか選択ができます。

標準のスタイルにプロジェクトごとの区切り線が付いたもの。
<img src="https://rashita.net/blog/wp-content/uploads/2011/04/window-grab1-300x216.png" alt="区切り線付き" title="区切り線付き" width="300" height="216" class="alignnone size-medium wp-image-5557" />

ターミナル風。いかにもって感じがします。
<img src="https://rashita.net/blog/wp-content/uploads/2011/04/window-grab2-300x216.png" alt="ターミナル風" title="ターミナル風" width="300" height="216" class="alignnone size-medium wp-image-5558" />

これだとタスク管理アプリっぽく見えますね。某アプリからインスパイアされたもののようです。
<img src="https://rashita.net/blog/wp-content/uploads/2011/04/window-grab3-300x216.png" alt="Thingsインスパイアー" title="Thingsインスパイアー" width="300" height="216" class="alignnone size-medium wp-image-5559" />
<h3>もうちょっと気になったところ</h3>
TaskPaperのメニューには、AppleScriptのアイコンが鎮座しています。これは最近使い始めたCotEditorにもあって、このアイコンがあるとつい気になってしまいます。スクリプトエディタで見てみると、このTaskPaperさんもAppleScriptでちょいちょい操作できる感じみたいです。

ちなみに全然中身読んでいないんで妄想にすぎませんが、例えばEvernoteから特定のノートを取得してチェックボックス付いているものをTaskPaperのタスクにするとか、あるいはその逆とかができたら面白そうです。

<strong>▼こんなリンクも：</strong>
<a href="http://www.hogbaysoftware.com/products/taskpaper">本家サイト</a>
<a href="http://hiroshimo.wordpress.com/2010/03/11/taskpaper-ubiquitous-capture/">そのひらめきを逃さない！ TaskPaperで素早くアイデアをキャプチャーする</a>(When you were young)

<strong>▼アプリへGo！：</strong>
<a href="http://click.linksynergy.com/fs-bin/stat?id=Q0goZPzeHEw&offerid=94348&type=3&subid=0&tmpid=2192&RD_PARM1=http%253A%252F%252Fitunes.apple.com%252Fjp%252Fapp%252Ftaskpaper%252Fid424281111%253Fmt%253D12%2526uo%253D4%2526partnerId%253D30" target="itunes_store"><img src="http://ax.phobos.apple.com.edgesuite.net/ja_jp/images/web/linkmaker/badge_macappstore-lrg.gif" alt="TaskPaper - Hog Bay Software" style="border: 0;"/></a>

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_top">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_top"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 1202<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

