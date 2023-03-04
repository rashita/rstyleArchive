---
title : 物書きが使うVS Code　〜インストールと日本語表示化〜
link : 30307
date : Thu, 27 Aug 2020 05:43:07 +0000
categories : ["物書き生活と道具箱"]
tags : ["vs-code","テキストエディタ","物書きが使うvs-code","物書きエディタ"]
draft : false
author : 倉下忠憲
---

Microsoft が提供している「<a href="https://azure.microsoft.com/ja-jp/products/visual-studio-code/">Visual Studio Code</a>」（以降VS Code）を最近好んでよく使っています。

<a href="https://azure.microsoft.com/ja-jp/products/visual-studio-code/" rel="attachment wp-att-30308"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-9-700x370.png" alt="" width="700" height="370" class="alignnone size-large wp-image-30308" /></a>

基本的にはコードを書くためのエディタであり、その用途としても便利に使えるのですが、案外執筆作業でも活躍してくれることを最近知りました。物書きエディタとコードエディタには共通点が多いのではないかとTak.さんがおっしゃっていましたが、その通りだと思います。

で、このVS Codeの何が良いのかですが、以下の点が挙げられます。

<ul>
	<li>エグイほどのカスタマイズ性</li>
	<li>便利なワークスペース概念</li>
	<li>充実した拡張機能</li>
</ul>

これに加えて、スクリプトを使われる方なら「内蔵されたターミナル」も挙げられます。まあ、その辺はおいおい語っていきましょう。

<h2></h2>

まずは、導入です。といっても、無料なので以下からダウンロードするだけです。

<a href="https://code.visualstudio.com/download">https://code.visualstudio.com/download</a>

Window,Mac,Ubuntuとか、いろいろバージョンがあるみたいです。とりあえず、ここではすべてMac版（Version: 1.48.2）で話を進めます。

<h2>日本語環境</h2>

「べ、別に英語環境だってぜんぜん構わないんだからね！」という方は別にして、メニューなどを日本語にしたい方は、設定を変えましょう。

いろいろやり方はありますが、今後頻繁に使うであろう方法でいきます。

shift + command + p

を押します。これでコマンドパレットが開きます。コマンドとかファイル都下を探すための検索ウィンドウだと思ってください。適当な言葉を入れたら、それでぐいぐい絞り込んでくれます。

今回見つけたいのは、「Config Display Language」なので、頭から素直に入力してもいいのですが、「Language」を入れるのが早いでしょう。見つけたらリターンです。

<a href="https://gyazo.com/1dbc80f68fd2285531996a8e008fbd7d"><video alt="Video from Gyazo" width="500" autoplay muted loop playsinline controls><source src="https://i.gyazo.com/1dbc80f68fd2285531996a8e008fbd7d.mp4" type="video/mp4" /></video></a>


何も設定していなければ、初期では「en」が表示されるだけだと思います。その下に「install additional languages…」が表示されるので、そちらを選択しましょう。

すると、サイドバーに変化が現れると思います。これは「Extensions」でいわゆる拡張機能というやつです。つまり、他の言語表示にするために必要な拡張機能だけを絞り込んで表示してくれているわけですね。

もちろんここでは「japanese」（日本語）を選択します。正確には「Japanese Language Pack for Visual Studio Code」です。これをインストールします。

インストールが終わると（一瞬で終わります）、右下に「おまえさん、言語表示を日本語に変えたいのならば、再起動が必要でありんすが、いかがいたします？」と聞いてくれるので、ポチッと「Yes」を押しましょう。

すると、自動的に再起動されて、あれ不思議、メニューもろもろが日本語に変わっています（ぜんぜん不思議ではない）。

<h2>さいごに</h2>

というわけで、まずは表示周りを日本語にしてみました。別に気にならない人はいいのですが、英語というだけでちょっと難しそうに感じてしまう人は（私は含めて）多いので、変えておくのは良いでしょう。

あと、この「コマンドパレットからコマンドを探す」と「拡張機能をインストール」はたびたび出てくるので、一度慣れておくのも良いかと思います。

では次回は、画面周りの説明に入りましょう。

（つづく）
