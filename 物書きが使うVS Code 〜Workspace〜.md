---
title : 物書きが使うVS Code 〜Workspace〜
link : 30321
date : Mon, 31 Aug 2020 06:19:13 +0000
categories : ["物書き生活と道具箱"]
tags : ["vs-code","テキストエディタ","物書きが使うvs-code","物書きエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=30307">第一回</a>
<a href="https://rashita.net/blog/?p=30312">第二回</a>

今回は、VS Codeにおける重要概念「Workspace」について紹介します。

<h2>概要</h2>

「Workspace」は、フォルダで構成される作業空間のことです。

まずは、サイドバーのExploerを開きましょう。

<a href="https://rashita.net/blog/?attachment_id=30322" rel="attachment wp-att-30322"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-14.png" alt="" width="612" height="1444" class="alignnone size-full wp-image-30322" /></a>

この「Open Folder」で指定するフォルダが作業空間となります。ためしに「R-style」というフォルダを指定してみます。

<a href="https://rashita.net/blog/?attachment_id=30323" rel="attachment wp-att-30323"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-15-700x633.png" alt="" width="700" height="633" class="alignnone size-large wp-image-30323" /></a>

Finderのようにフォルダの中身が表示されました。どれかをクリックしたら、当然のように、その中身がエディタで表示されます。

<a href="https://rashita.net/blog/?attachment_id=30324" rel="attachment wp-att-30324"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-16-700x540.png" alt="" width="700" height="540" class="alignnone size-large wp-image-30324" /></a>

これがまず基本です。

<h2>Workspaceの保存</h2>

続いて、このWorkspaceを保存してみましょう。「Flie」メニューにある「Save Workspace As」がそれです。

保存すると、「hoge.code-Workspace」というやたら拡張子が長いファイルができます。

<a href="https://rashita.net/blog/?attachment_id=30325" rel="attachment wp-att-30325"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-17.png" alt="" width="416" height="400" class="alignnone size-full wp-image-30325" /></a>

このファイルを開くと、先ほど作ったWorkspaceが開かれます。

これが基本その２です。

<h2>複数フォルダの設定</h2>

Workspaceの本領が発揮されるのは、ここからです。

Workspaceには、複数のフォルダを設定できます。「File」メニューにある「Add Folder to Workspace」を選択して、別のフォルダを入れ込んでみます。

<a href="https://rashita.net/blog/?attachment_id=30326" rel="attachment wp-att-30326"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-18.png" alt="" width="482" height="420" class="alignnone size-full wp-image-30326" /></a>

このように読み込めました。こうして読み込むフォルダは、同じ階層にある必要はまったくありません。ぜんぜん違う階層に飛んでいてもOKです。これが極めて使い勝手が良いのです。

<h2>Workspaceの利用</h2>

軽くまとめましょう。

Workspaceは複数フォルダをまとめる環境であり、それぞれのフォルダは別の階層にあっても問題ありません。

また.code-workspaceファイルは、読み込んだフォルダ内に保存しなくても大丈夫です。たとえば、R-styleフォルダを読み込んだからといって、code-workspaceファイルもR-style内に保存しなけれいけない、というルールはありません。

私はテキストファイルはDropbox下のそれぞれのプロジェクト用フォルダに、.code-workspaceファイルはデスクトップに配置しています。複数のフォルダをまとめられるので、デスクトップをすっきりさせたまま、しかし、必要なフォルダ群に即座にアクセスできる環境が整うわけです。

また、同一のフォルダを別のWorkspaceに読み込ませることもできます。私は、「Writing」というフォルダを作り、そこに執筆全般に必要な情報をまとめて、それぞれのWorkspaceに読み込ませるようにしています。

<a href="https://rashita.net/blog/?attachment_id=30327" rel="attachment wp-att-30327"><img src="https://rashita.net/blog/wp-content/uploads/2020/08/screenshot-19.png" alt="" width="450" height="344" class="alignnone size-full wp-image-30327" /></a>

どのWorkspaceにいるときでも、ここの情報を更新すれば、他のWorkspace利用時にも更新されるので、たいへん便利です。他にも「総合Todo」みたいなもの、このやり方で管理できるかもしれません。使い方は、他にも考えられるでしょう。

<h2>Workspaceの切り替え</h2>

で、これがもっとも重要な機能ですが、control + r (Mac版)で、最近開いた別のWorkspaceに切り替え可能です。

そうなのです。先ほどcode-workspaceをデスクトップに保存する、みたいなことを書きましたが、実はそういう気配りすら要りません。control + r で移動したいWorkspaceを見つけてリターンで移動は完了します。

これが極めて便利です。快適です。まるで冒険の初めの方で、やっとこさルーラを覚えたかのような感覚があります。Dynalistの command + o のジャンプも快適ですが、それに匹敵するか上回る快適さがあります。

このショートカットがなければ、プロジェクトごとにファイルを分けて管理することはずいぶん面倒な作業になったでしょう。しかし、このショートカットがあるおかげで、複数ファイル管理の手間はまったく感じなくなります。ほとんどUlyssesを使っているような使い心地です（もちろん、完全に同じではありませんのであしからず）。

<h2>さいごに</h2>

というわけで、今回は超絶便利なWorkspaceについてでした。

<ul>
	<li>作業のフォルダをまとめ</li>
	<li>code-workspaceファイルとして保存し</li>
	<li>そのファイルを control + r  で行き来する</li>
</ul>



こんな感じで使えます。

で、さらにこのWorkspaceごとにカスタマイズを設定できるのですが、それはカスタマイズの回で紹介しましょう。

（つづく）