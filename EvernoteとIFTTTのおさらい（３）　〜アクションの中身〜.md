---
title : EvernoteとIFTTTのおさらい（３）　〜アクションの中身〜
link : 12242
date : Tue, 17 Dec 2013 03:48:26 +0000
categories : ["evernoteの使い方"]
tags : ["evernoteとiftttのおさらい","evernote","ifttt"]
draft : false
author : 倉下忠憲
---

今回は、Evernoteが持つアクションの具体的な中身を紹介してきます。

※前回まで
第一回：<a href="https://rashita.net/blog/?p=12150" target="_blank">EvernoteとIFTTTのおさらい（１）　〜IFTTTとは何か〜</a>
第二回：<a href="https://rashita.net/blog/?p=12228" target="_blank">EvernoteとIFTTTのおさらい（２）　〜トリガーとアクション〜</a>

話をシンプルにするため、今回のレシピは

<strong>「Evernoteでノートをシェアしたら→Evernoteにノートを作成する」</strong>

というEvernoteだけで完結できるものにしておきましょう。

一見すると何の役にも立たなそうですが、たぶん何の役にも立たないでしょう。あくまで構造を理解するための例ですので、あしからず。

<H3>「Create a note」の中身</H3>レシピ作成のステップ１から５は省略します。

トリガー（Evernote）→「New shared note link」→確定→アクション（Evernote）→「Create a note」

まで進んでください。すると、次のような画面が出てくるでしょう。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot30.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot30.png" alt="screenshot" width="500" height="550" class="alignnone size-full wp-image-12243" /></a>

普段Evernoteを使っている方ならば、お馴染みのものばかり。

<ul>
	<li>Title・・・新規作成されるノートのタイトル</li>

	<li>body・・・新規作成されるノートの中身</li>

	<li>Notebook・・・新規作成されるノートが入るノートブック（省略するとデフォルトのノートブックに）</li>

	<li>Tag・・・新規作成されるノートに付けられるタグ（コンマ（,）で複数入力できます）</li>
</ul>



これらを自由にカスタマイズできます。

そして、そのカスタマイズに一役買ってくれる機能が、IFTTTにはあります。入力エリア内にある青地に白の十字ボタンがそれです。ここには魔法の言葉がいくつか収納されているのです。

<H3>魔法の言葉:Ingredient</H3>まずは、Titleの十字ボタンをぽちっと押してみましょう。

「Select an Ingredient」という選択バーが表示されるはずです。それをクリックして、ひとつ下にある「Note title」を選択します。すると、入力エリアはこんな感じに表示されるでしょう。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot31.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot31.png" alt="screenshot" width="500" height="96" class="alignnone size-full wp-image-12244" /></a>

入力エリアをクリックすると、こうなります。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot32.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot32.png" alt="screenshot" width="500" height="96" class="alignnone size-full wp-image-12245" /></a>

この二つの{}に挟まれた単語が魔法の言葉です。ingredientとは、材料や構成要素といった意味。ノートタイトルや中身の素材になってくれる言葉なのです。言ってしまえば変数なのですが、その説明はスルーしておきましょう。

このIngredientは最初に選択した「トリガー」と緊密な関係を持っています。

たとえば、仮に「Note Title」というIngredientをTitle欄に入れたら、どうなるのでしょうか。今回のレシピをもう一度確認しましょう。

「Evernoteでノートをシェアしたら→Evernoteにノートを作成する」

Title欄に入力されたテキストが、新規作成されるノートのタイトルになります。もし、そこに{{Title}}という魔法の言葉を入れておくと、新規作成されるノートのタイトルが、シェアされたノートのタイトルになるのです。

つまり「私のEvernoteのとっておきの使い方」というノートをシェアしたら、「私のEvernoteのとっておきの使い方」というタイトルのノートが新規作成されます。それに続いて「私のEvernoteのとっておきの使い方ver.2」というノートをシェアしたら、今度は「私のEvernoteのとっておきの使い方ver.2」というタイトルのノートが新規作成されます。

Titleに{{Title}}ではなく、「私のEvernoteのとっておきの使い方」というフレーズを直接入れておいても、最初の動作は上とまったく同じです。しかし、二回目の動作が違ってくることに注意してください。

さて、「Note Title」以外に選べるIngredientには、他にどのようなものがあるでしょうか。

●「Evernoteでノートをシェアしたら→Evernoteにノートを作成する」で選べるIngredient
 
<ul>
	<li> 「Note Title」・・・シェアされたノートのタイトル</li>
	<li> 「Note URL」・・・シェアされたノートのURL</li>
	<li> 「Tags」・・・シェアされたノートのタグ</li>
	<li> 「Created Date」・・・シェアされたノートの作成日時</li>
</ul>

これらは、Title以外の欄にでも使用することができます。
 
たとえば、「Evernoteでノートをシェアしたら、そのノートのタイトルを持ったノートを新規作成し、その中身をシェアされたURLにする」なんてことができます。その動作に、どんな意味があるのかは私にはわかりませんが、そういう動き方ができるという点だけ押さえておいてください。
 
<H3>レシピ・チェンジ</H3>では、一旦ステップを戻って、アクションを「Append to note」に選び直してみましょう。

これは「既存のノートに追記する」という行動でしたね。つまり、

<strong>「Evernoteでノートをシェアしたら→Evernoteのノートに追記する」</strong>

というレシピに変更です。

もしまったく状況が変わっていなければ、「Append to note」を選択した場合、次のような画面が表示されるはずです。すでにいくつかの項目が入力されている状況です。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot33.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot33.png" alt="screenshot" width="500" height="530" class="alignnone size-full wp-image-12246" /></a>

これは他の人が共有したレシピが参考例として表示されていると考えてください（<a href="https://ifttt.com/recipes/125314">参照</a>）。

このレシピをそのまま使ってもよいですし、自分なりにアレンジを加えることもできます。

ちなみに、このレシピを動かすと、次のようなノートが生まれます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot34.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot34.png" alt="screenshot" width="500" height="320" class="alignnone size-full wp-image-12247" /></a>

自分がシェアしたノートのリストができあがるわけです。無論、IFTTTさえ稼働していれば、自分がノートをシェアするたびに、自動的にこのノートに項目が追加されていきます。これは、何かしら使う意味みたいなものはありそうです。

ちなみに、「既存のノート」は、ノートブック、タグ、ノートタイトルによって検索されていると思われます。もし、追記すべきノートが見つからない場合は、自動的にそれを作成してくれます。一見便利ですが、たとえばノートブックのスペルを間違えてしまうと（LifelogをLiferogとしてしまうなど）、その名前でノートブックが新規作成されてしまう点には注意してください。

あと、誠に誠に残念ながら日本語（全角文字ですね）が通りません。ノートブック名に全角文字を使っている場合には注意が必要です。
※私は[業務日誌]というノートブックを、仕方なく[Worklog]という名前に変更しました。

<H3>アレンジのポイント</H3>それぞれの入力欄にアレンジポイントは存在しますが、Evernoteで言えば、やはりBodyが気になるところ。

HTMLをご存じの方ならば、何も問題ありませんが、そうでないならば多少知識が必要です。

が、本当に基本的なことがらで押さえておきたいのは、改行したければ&lt;BR&gt;を入れる、ということぐらいでしょうか。水平線を入れる&lt;HR&gt;、太字にする&lt;B&gt;（あるいはStorng）なんかも便利です。

たとえばレシピをこのように変更すると、

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot35.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot35.png" alt="screenshot" width="500" height="180" class="alignnone size-full wp-image-12248" /></a>

ノート上では、このような変更になります。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot36.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot36.png" alt="screenshot" width="500" height="260" class="alignnone size-large wp-image-12249" /></a>

ちなみにマニアックな話になりますが、&lt;en-todo /&gt;あたりは通りません。
<H3>さいごに</H3>これでチャンネル、トリガー、アクション、についての理解がずいぶんと深まりましたね。

次回は、TwitterとEvernoteとのレシピを掘り下げてみます。

次回→<a href="https://rashita.net/blog/?p=12267" target="_blank">EvernoteとIFTTTのおさらい（４）　〜Twitterとのレシピ〜</a>