---
title : 物書きが使うVS Code　〜画面構成〜
link : 30312
date : Fri, 28 Aug 2020 06:25:52 +0000
categories : ["物書き生活と道具箱"]
tags : ["vs-code","テキストエディタ","物書きが使うvs-code","物書きエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=30307">第一回</a>→

今回は、基本的な画面構成を紹介します。

<h2>エディタ</h2>

中央がテキストエディタ領域です。特に難しい説明は要りませんね。

<a href="https://rashita.net/blog/?attachment_id=30314" rel="attachment wp-att-30314"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-10-700x532.png" alt="" width="700" height="532" class="alignnone size-large wp-image-30314" /></a>

タブ型になっているので、そこにいくらでも開いていけます。

また、ウィンドウの分割もできます。右上の方にある「田」という漢字を書くのを途中で諦めたようなアイコンを押せば横に分割されます。メニューの「View」→「Editor Layout」を使えば、上下左右に分割することもできますし、規定のウィンドウ構成にセットすることもできます。

<a href="https://rashita.net/blog/?attachment_id=30315" rel="attachment wp-att-30315"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-11-700x550.png" alt="" width="700" height="550" class="alignnone size-large wp-image-30315" /></a>

でもって、分割されたウィンドウもまた、それぞれにタブを持てます。ページ開きたい放題です。

ちなみに、変更があり、保存されていないタブは右側に「●」がつきますので、お見逃しなきよう。

あと、下の方に状態を表示するバー（ステータスバー）もついています。ここも地味に使いますので注意しておきましょう。

<h2>サイドバー</h2>

左にあるアイコンのどれかを押せば、サイドバーが展開されます。VS Codeではアクティビティーバーと呼ばれています。

標準では以下の５つの領域があります。

<ul>
	<li>Explorer</li>

	<li>Search</li>

	<li>Source Control</li>

	<li>Run</li>

	<li>Extensions</li>
</ul>



Explorerは、ファイル周りです。Searchは検索で、Source ControlはGit用、Runは物書き仕事ではほぼ使わずで、Extensionsは拡張機能をインストールするための領域です。

（Explorer）
<a href="https://rashita.net/blog/?attachment_id=30316" rel="attachment wp-att-30316"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-12.png" alt="" width="426" height="1172" class="alignnone size-full wp-image-30316" /></a>

（Search）
<a href="https://rashita.net/blog/?attachment_id=30317" rel="attachment wp-att-30317"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-13.png" alt="" width="434" height="874" class="alignnone size-large wp-image-30317" /></a>

通常の作業でよく使うのは、ExplorerとSearchで、Gitを使うならSource Controlを、カスタマイズして機能拡張するときはExtensionsが活躍します。

アクティビティーバーは、Command + b で開閉がトグルします。

<h2>ターミナル</h2>

「View」→「Terminal」とするか、shift + control + @ とすればエディタの下にターミナルが開きます。

Gitまわりは、Source Controlでだいたい事足りますが、それ以外の用途でターミナルを使うときはたいへん便利です。

VImなどは、「ターミナルから立ち上げられるテキストエディタ」ですが、VS Codeは「ターミナルを立ち上げられるテキストエディタ」というわけで、どちらも単一のツールで完結するすがすがしさがあります。

「物書きにターミナルが必要なのか？」

という疑問はあろうかと思いますが、使えて不便なことはないし、いろいろ処理の可能性が広まるので、余裕があれば使えるようになった方が良い、ということは書いておきます。実践経験からの感想です。

<h2>さいごに</h2>

というわけで、画面構成は以上です。難しいものは特にありませんね。

次回は、VS Codeの便利な概念「WorkSpace」について紹介します。

（つづく）