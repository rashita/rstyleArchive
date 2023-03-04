---
title : 物書きが使うVS Code　〜カスタマイズと設定項目〜
link : 30332
date : Tue, 01 Sep 2020 08:07:35 +0000
categories : ["物書き生活と道具箱"]
tags : ["vs-code","物書きが使うvs-code"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=30307">物書きが使うVS Code　〜インストールと日本語表示化〜</a>
<a href="https://rashita.net/blog/?p=30312">物書きが使うVS Code　〜画面構成〜</a>
<a href="https://rashita.net/blog/?p=30321">物書きが使うVS Code 〜Workspace〜</a>

VS Codeは、すげーカスタマイズできます。

以上、あとはググってください。

で、終わらせたい気持ちがいっぱいです。なにせ、カスタマイズできることが多すぎて、それを列挙していくだけでMacBook Airのバッテリーがへばってしまうからです。

なので、カスタマイズに関しては、ごくごく触りだけを紹介します。詳しくは、Webの大海を泳いでください。

<h2>設定の仕方</h2>

設定周りは、メニューの「Code」→「Preferences」→「Settings」から行えます。ショートカットキー command + , からでも開けますので覚えておきましょう。

で、「Settings」を選択すると、次のようなタブが開くと思います。ここでさまざまな設定ができるのですが、一度上から下までスクロールしてもらうと、いかに細かいカスタマイズが可能かが理解されるかと思います。

<a href="https://rashita.net/blog/?attachment_id=30334" rel="attachment wp-att-30334"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-700x561.png" alt="" width="700" height="561" class="alignnone size-large wp-image-30334" /></a>

一応左側にカテゴリーもありますので、そちらから探すこともできますが、やっぱりVS Codeは気が利いていて、なんとカスタマイズ項目を検索で探すことができます。

たとえば、gitの周りの項目を探したいなら、そのままgitを上の検索ボックスに打ち込めば、それで絞り込まれます。Wow！

<a href="https://rashita.net/blog/?attachment_id=30335" rel="attachment wp-att-30335"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-1-700x297.png" alt="" width="700" height="297" class="alignnone size-large wp-image-30335" /></a>

カスタマイズの細かさで言うと、Scrivenerもなかなかやるんですが、あいつは「どこに、どの項目があるのか皆目検討もつかないし、探し方も分からない」な状況なのですが、VS Codeはバッチリサポートされています。

というか、こういう探し方ができないと、にっちもさっちもいかないくらい設定項目がある、というのが本当のところでしょう。

<h2>私の設定項目</h2>

もし、設定する項目の名前が分かっているなら、いちいち探し回る必要もありません。自分で直接記述すればOKです。

タブの右側にある、ファイルがターンしようとしているアイコンをポチっと押しましょう。

<a href="https://rashita.net/blog/?attachment_id=30336" rel="attachment wp-att-30336"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-2.png" alt="" width="298" height="204" class="alignnone size-full wp-image-30336" /></a>

settings.json というファイルが開くと思います。名前から察せられる通り、設定項目を扱うファイルです。先ほどのメニューは、このファイルの編集をサポートしてくれる機能なので、じかにこちらを編集するほうが早い場合は、そちらでやっちゃいましょう。他の人の設定をパク……拝借するときも、このやり方の方が手っ取り早いです。

私は、以下のような設定をしています。
[code]
{
    &quot;editor.fontSize&quot;: 16,
    &quot;editor.wordWrap&quot;: &quot;on&quot;,
    &quot;editor.wordWrapColumn&quot;: 64,
    &quot;window.zoomLevel&quot;: -1,
    &quot;editor.minimap.enabled&quot;: false,
    &quot;markdown.preview.scrollPreviewWithEditor&quot;: false,
    &quot;markdown.preview.scrollEditorWithPreview&quot;: false,
    &quot;workbench.colorCustomizations&quot;: {
        // アクティビティバー
        &quot;activityBar.background&quot;: &quot;#000&quot;, // アクティビティバーの背景色
        &quot;activityBar.foreground&quot;: &quot;#ffffff&quot;, // アクティビティバーの前景色
        &quot;activityBar.border&quot;: &quot;#646464&quot;, // アクティビティバーの境界線
        // サイドバー
        &quot;sideBarSectionHeader.background&quot;: &quot;#373746&quot;, // サイドバーセクションヘッダーの背景色
        &quot;sideBarSectionHeader.border&quot;: &quot;#8db3ff46&quot;, // サイドバーセクションヘッダーの境界線の色
        &quot;sideBar.background&quot;: &quot;#292931&quot;, // サイドバーの背景色
        &quot;sideBar.foreground&quot;: &quot;#a0a0a0&quot;, // サイドバーの前景色
        &quot;sideBar.border&quot;: &quot;#646464&quot;, // サイドバーの境界線
        &quot;list.activeSelectionBackground&quot;: &quot;#2c88d377&quot;, // アクティブな状態のセクションの背景色
        &quot;list.focusBackground&quot;: &quot;#2c88d377&quot;, // フォーカス状態のセクションの背景色
        &quot;list.hoverBackground&quot;: &quot;#193c5877&quot;, //ホバー状態のセクションの背景色
        // ヘッダー、タブ
        &quot;editorGroupHeader.tabsBackground&quot;: &quot;#2929316e&quot;, // ヘッダーの背景色
        &quot;tab.activeBackground&quot;: &quot;#0319464f&quot;, // アクティブタブの背景色
        &quot;tab.border&quot;: &quot;#8db3ff46&quot;, // タブの横線
        &quot;tab.inactiveBackground&quot;: &quot;#2929316e&quot;, // 非選択タブの背景色
        // エディター
        &quot;editor.selectionBackground&quot;: &quot;#1d34b765&quot;, // 選択領域の強調色
        &quot;editor.lineHighlightBackground&quot;: &quot;#9e99ee11&quot;, // 選択している行の強調色
        &quot;editorLineNumber.foreground&quot;: &quot;#a2bdddbb&quot;, // 選択行番号の文字色
        &quot;editorBracketMatch.background&quot;: &quot;#2c88d377&quot;, // 対応する括弧の背景色
        // ステータスバー
        &quot;statusBar.background&quot;: &quot;#000&quot;, // ステータスバー背景色
        &quot;statusBar.foreground&quot;: &quot;#ffffff&quot;, // ステータスバー前景色
        &quot;statusBar.border&quot;: &quot;#646464&quot;, // ステータスバー前景色
        // スクロールバー
        &quot;scrollbarSlider.background&quot;: &quot;#0d478a99&quot;, // スクロールバーの色
        // walcomeページ
        &quot;welcomePage.background&quot;: &quot;#2231419c&quot;
    },
    &quot;markdown.preview.fontFamily&quot;: &quot;'Hiragino Kaku Gothic ProN',-apple-system, BlinkMacSystemFont, 'Segoe WPC', 'Segoe UI', system-ui, 'Ubuntu', 'Droid Sans', sans-serif&quot;,
    &quot;markdown.preview.fontSize&quot;: 16,
    &quot;markdown.preview.markEditorSelection&quot;: false,
    &quot;editor.fontFamily&quot;: &quot;'Hiragino Sans','Hiragino Mincho ProN',Menlo, Monaco, 'Courier New', monospace&quot;,
    &quot;terminal.integrated.fontSize&quot;:15,
    &quot;terminal.integrated.fontFamily&quot;:&quot;monospace&quot;,
    &quot;git.postCommitCommand&quot;: &quot;push&quot;,
    &quot;terminal.integrated.letterSpacing&quot;: 0,
}

[/code]

物書きさんが気にしそうなところだけ解説すると、

"editor.fontSize": 16,
"editor.fontFamily": "'Hiragino Sans','Hiragino Mincho ProN',Menlo, Monaco, 'Courier New', monospace",

エディタのフォントサイズと、フォントファミリーです。

"editor.wordWrap": "on",
"editor.wordWrapColumn": 64,

エディタの「折り返し」がありで、64文字で折り返しです。

"editor.minimap.enabled": false,

エディタに表示されるミニマップを消します。

あとは、もう、それぞれの項目名でググってください。これ以外にもいっぱい設定項目があります。

<h2>Workspaceごとのカスタマイズ</h2>

上記は、VS Code全般に関するカスタマイズでした。VS Codeの恐ろしいところは、前回紹介したWorkspaceごとに、上記のカスタマイズを設定・保存できることです。

ごく簡単に言えば、プロジェクトAというWorkspaceでは"editor.fontFamily": 'Hiragino Sans'にして、プロジェクトBというWorkspaceでは"editor.fontFamily":'Hiragino Mincho ProN'にする、みたいなことができます。

で、たとえば、「執筆用プロジェクト」と「コーディング用プロジェクト」で設定をまったく変えてしまうということが可能なわけですね。

先ほどの検索ボックスの直下を見てください。「User」「Workspace」「Folder」の三つが並んでいるかと思います。

<a href="https://rashita.net/blog/?attachment_id=30337" rel="attachment wp-att-30337"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-3.png" alt="" width="492" height="230" class="alignnone size-full wp-image-30337" /></a>

先ほどは「User」のsettings.jsonを開きました。ここに設定を書くと、すべてのWorkspaceにその設定が反映されます。

一方次の「Workspace」のsettings.json（開き方は先ほどと同じです）に設定を書くと、そのWorkspaceを開いたときだけに反映されます。

さらに、です。最後の「Folder」のsettings.jsonに設定を書くと、Workspaceに取り込んだ、特定のFolderのファイルを開くときにだけその設定が反映されます。

ですので、たとえばHugoのように、テキストファイルで文章を書くことと、htmlやcssをいじることが、同一のプロジェクト（Workspace）にあったとしても、それぞれにおいて適切な表示の仕方をカスタマズできるのです。アンビリーバボ！

これはスゲー便利で、たとえば私は文章を書くときはやや大きめのフォントサイズを指定しているのですが、「書籍リスト」とか「単語リスト」みたいなファイルは、小さめの文字で表示された方が一覧性が上がります。それらをいちいちアプリなどで切り替えることなく、ごく自然に適切に表示させられるのです。この機能には、うならされました。

テキストファイルだけしか扱わないときは、それほど威力は感じられないと思いますが、テキストとHTMLとか、そういう操作をするときは、本当にむっ茶便利です。

<h2>Workspaceだけの設定</h2>

もう一つ、Workspaceのsettings.jsonを開くと、こんな感じの項目があらかじめ設定されていると思います。

<a href="https://rashita.net/blog/?attachment_id=30338" rel="attachment wp-att-30338"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-4-700x629.png" alt="" width="700" height="629" class="alignnone size-large wp-image-30338" /></a>

名前からなんとなく推測できるでしょうが、そのWorkspaceに取り込んだフォルダの一覧です。で、この記述の順番にExplorerでは表示されます。逆に言えば、Explorerでの表示順を変えたい場合は、このsettings.jsonを書き換えればOKです。

Evernoteなどはノートブックの順番がいじれませんが、VS Codeはその辺が融通が利くので好きです。

<h2>さいごに</h2>

ということで、今回は沼中の沼であるVS Codeのカスタマイズについて紹介しました。

ほんとうにすいませんが、詳細はググってください。ググったらきっとびっくりするはずです。あと、ショートカットキーなども設定できるのですが、それも今回は割愛しておきます。それをしなくても、十分便利なエディタですので、まずは触ってみるのが大切かなと思います。

ちなみに私は、できるだけWorkspaceごとに「見た目」を変えて、「今自分が開いているプロジェクトはこれだな」ということが視覚的に分かりやすくなるように設定しています。これだけでもずいぶん楽しいものです。