---
title : ScrivenerのCompileで覚えておきたい３テクニック
link : 12788
date : Fri, 28 Feb 2014 05:28:19 +0000
categories : ["scrivenerへの散歩道"]
tags : ["scrivener"]
draft : false
author : 倉下忠憲
---

Scrivenerには「compile」（以下コンパイル）という機能があります。

プレーンなテキストエディタならtxtファイルを、Wordであれば.docあたりを生成するわけですが、Scrivenerでは.scrivという専用のファイルを生成します。これはScrivenerでしか読めません。

しかし、このデータを元にしてさまざまなフォーマットのファイルを作成できるのがScrivenerの強みです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/scrivner.002.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/scrivner.002.jpg" alt="scrivner.002" width="500" height="375" class="alignnone size-full wp-image-12789" /></a>

このコンパイルの際に、覚えておくとよいことがいくつかあります。今回は３つだけ紹介してみましょう。

<ul>
	<li>タイトルへの接頭語、接尾語</li>
	<li>タグでメタデータ入力の省略可</li>
	<li>全てをコンパイルしなくていい</li>
</ul>

<H3>タイトルへの接頭語、接尾語</H3>

形式を持った文章をコンパイルするときに覚えておきたいのがこの方法。章題をつける際に非常に便利です。

以前このブログでも紹介しました。

<a href="https://rashita.net/blog/?p=12662" target="_blank">Scrivener→「EPUB3::かんたん電子書籍作成」のちょっとしたコツ</a>（R-style）

Prefix（接頭辞）、Suffix（接尾辞）を使えば、以下のような原稿を

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot34.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot34.png" alt="screenshot" width="470" height="192" class="alignnone size-full wp-image-12790" /></a>

以下のように出力できます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot35.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot35.png" alt="screenshot" width="500" height="254" class="alignnone size-full wp-image-12791" /></a>

原稿にはなかった、sectionが追記されているのがわかるでしょうか。

このPrefixはこんな感じになっています。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot36.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot36.png" alt="screenshot" width="381" height="339" class="alignnone size-full wp-image-12792" /></a>

コードに慣れた人なら一目瞭然でしょうが、<$n>は変数です。ご覧のように出力ではそれが１になっています。当然二つ目のセクションではこれが２になります。こうして自動的に増えていってくれるのが<$n>です。

もちろん、「第<$n>章」という使い方もできますね。どういう表記にするかは、自分で変更可能です。

変数を使う利点は、仮に章の順番を入れ換えても、いちいち数字を変更していく必要がない点です。50のナンバリングを一つずつずらしていくなんて、悪夢以外の何者でもありません。章題をつける場合は、Prefixを積極的に活用されるとよいでしょう。

また<$n>ではなく、<$t>とすれば、テキストによる表記になります。私の環境では漢数字の「一」になりました。英語設定なら「ONE」になるのでしょう。好みで使い分けてください。

<H3>タグでメタデータ入力の省略可</H3>

上と似たようなものですが、メタデータを保存してくれる変数があります。すでにテンプレートを使っている方ならば、お馴染みでしょう。たとえば、<$projecttitle>なら、そのプロジェクトのタイトルが入っています。なので、原稿データで<$projecttitle>とある部分は、コンパイル時にプロジェクトのタイトルに変換されます。

その他にも、こうしたタグがいくつもあります。

<$projecttitle>
<$abbr_title>
<$fullname>
<$surname>
<$forename>
<$author>
<$status>
<$longdate>
<$year>
<$BLANK_PAGE>
※これ以外にもあるはず

これらを使えば、直接表記することなく、出力時には必要なデータが反映されます。

ちなみにプロジェクトのタイトルや著者に関しては、メニューの「project」 →「Mate-Data settings」から変更可能です。
<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot37.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot37.png" alt="screenshot" width="500" height="444" class="alignnone size-full wp-image-12793" /></a>

<$projecttitle>を使っておけば、後からタイトルを変更しても、原稿中の全ての表記をいちいち変えて回る必要がありません。これは置換でも対応できますが、<$longdate>（※）などは日付の変更忘れをなくしてくれます。
※今日なら「2014年2月28日」が入る

また、これらのタグはテンプレートを作る際にも活躍します。それは実際、いくつかのテンプレートをご覧になればすぐにわかるでしょう。

<H3>全てをコンパイルしなくていい</H3>

コンパイルのフォーマットを見てみると、必ずしも全てのテキストを出力する必要がないことに気がつきます。第三章と第四章だけ出力する、という風に選択できるのです。

もっと言えば、本文を抜いて、章題だけを出力することも可能です。以下の記事で紹介しました。

<a href="https://rashita.net/blog/?p=11505" target="_blank">Scrivenerで見出し部分だけを出力して、目次っぽいファイルを作る</a>(R-style)

これでアウトライン（あるいは目次）を作成することも可能です。

<H3>さいごに</H3>

正直、高機能すぎてScrivnerを使い切れない人は多いのではないでしょうか。私もその一人です。上の方法は、たまたま発見したか、あるは必要に迫られて検索して見つけたものでしかありません。私も、Scirvenerの全てを知っているわけではないのです。

というわけで、解説本の登場が待たれますね。

では、Happy Writingを！

<h2><span style="color: rgb(0, 0, 255);">Scrivener</span></h2><div style="margin: 0;float: left;"><div style="margin-left: 109px;"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" rel="nofollow" style="text-decoration: none;"><img src="http://a375.phobos.apple.com/us/r1000/068/Purple/v4/7f/c7/66/7fc7663d-0b33-0fcb-7924-d384ce39b2a5/Scrivener.100x100-75.png" style="margin-left: -109px; float: left; width: 100px; height: 100px;"><img src="http://r.mzstatic.com/htmlResources/2338/images/mask100.png" style="margin-left: -109px; float: left; width: 100px; height: 100px;" /></a></div></div> カテゴリ: 仕事効率化, 教育<br><br> 販売元: <a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" rel="nofollow">Literature & Latte - Literature & Latte Ltd</a><br> リリース日: 2011/07/06<br style="clear: both;">