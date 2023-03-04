---
title : miに「青空文庫モード」を追加して、タグの入力を簡易化する
link : 12677
date : Thu, 13 Feb 2014 02:28:48 +0000
categories : ["2-社会情報論"]
tags : ["mi","「本」の未来","電子書籍"]
draft : false
author : 倉下忠憲
---

拙著新刊でも触れましたが、EPUBファイルを作成する方法はいろいろあります。特に正解みたいなものはありません。

さて、以下のツールでは、青空文庫の注記入りテキストファイルをEPUB3ファイルに変換してくれます。

<a href="http://www18.atwiki.jp/hmdev/pages/21.html" target="_blank">AozoraEpub3 - 青空文庫ePub3変換</a>

で、「青空文庫の注記入りテキストファイル」ですが、平のプレーンテキストに独自のタグを入れることでマークアップしたものがそれです。詳しい話は「<a href="http://kumihan.aozora.gr.jp/slabid-19.htm" target="_blank">青空文庫 組版案内</a>」で、ざっくりした話は「<a href="http://takenokoshobo.com/kdp/manual_ao_epub/2.html" target="_blank">原稿から青空文庫形式への編集</a>」をご覧になるとよいでしょう。

これらのタグをいちいち入力してくのは面倒。というときに、ちょこっと便利なテクニックを。

<H3>青空文庫モードを追加</H3>使うのは以下の二つ。

<a href="http://www.mimikaki.net/" target="_blank">mi</a>
<a href="http://fairfield.minibird.jp/other_resources/mi-%E7%94%A8-%E9%9D%92%E7%A9%BA%E6%96%87%E5%BA%AB%E3%83%A2%E3%83%BC%E3%83%89" target="_blank">mi 用 青空文庫モード</a>

miは、Mac用のテキストエディタです。愛用されている方も多いでしょう。

そのmiでは入力時の「モード」を選択することができます。C,CSS,JavaScriptなどのモードが標準装備されているのですが、そこに「青空文庫モード」を追加すると、タグの入力が簡易になります。

モードの導入方法は「<a href="http://fairfield.minibird.jp/other_resources/mi-%E7%94%A8-%E9%9D%92%E7%A9%BA%E6%96%87%E5%BA%AB%E3%83%A2%E3%83%BC%E3%83%89" target="_blank">mi 用 青空文庫モード</a>」をご覧いただければ問題ないでしょう。ちなみに、この「モード」は開発者さんが自分で使っていたものの公開ver.だそうです。

「青空文庫モード」を追加すると、「ツール」にタグ（※）を入力する項目が増えます。

たとえば、この「見出しテスト」を見出しに指定したい場合、

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot12.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot12.png" alt="screenshot" width="394" height="140" class="alignnone size-full wp-image-12678" /></a>

テキストを選択し、「ツール」から「見出し類」→「見出し」→「指定：中見出し」をクリック。すると、

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot13.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot13.png" alt="screenshot" width="458" height="112" class="alignnone size-large wp-image-12679" /></a>

こんな感じでタグが追加されます。いちいちテキスト入力する手間を考えれば大幅に楽チンですね。ちなみに、以下の二つの表記は

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot14.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot14.png" alt="screenshot" width="483" height="143" class="alignnone size-large wp-image-12680" /></a>

同義です。囲んでもOKなのです。

<H3>タグの入力</H3>早速サンプルファイルを作ってみました。

流れは、

<strong>mi（青空文庫モードで入力）→txtファイルで保存→AozoraEpub3で変換→iBooksで閲覧</strong>

です。

作成したテキストファイルはこんな感じ。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot15.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot15-1024x866.png" alt="screenshot" width="500" height="425" class="alignnone size-large wp-image-12681" /></a>

できあがったEPUBファイルはこんな感じ。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot16.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot16-1024x753.png" alt="screenshot" width="500" height="360" class="alignnone size-large wp-image-12682" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot17.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot17-1024x753.png" alt="screenshot" width="500" height="360" class="alignnone size-large wp-image-12683" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot18.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot18-1024x753.png" alt="screenshot" width="500" height="360" class="alignnone size-large wp-image-12684" /></a>

ちゃんとルビも振れていますね。ばっちりです。

この「青空文庫モード」は、省入力できるだけでなく、タグの表記を覚えていなくてもそれなりに青空文庫方式が使えるのが一つのポイントです。もちろん、ある程度学んでおく必要はあるでしょうが。

<strong>▼告知:</strong>
2月17日に、八重洲ブックセンターさんで以下の新刊に関するブックセミナーを行います。

電子書籍の最初の一歩を踏み出せていない方はぜひご来場ください。参加料は無料ですが、事前に登録が必要ですのでご注意ください。

<a href="http://www.yaesu-book.co.jp/events/talk/2919/" target="_blank">倉下忠憲さん講演会　「セルフ・パブリッシングの最初の一歩」</a>

<a href="https://rashita.net/blog/?p=12536" target="_blank">[告知] 2月17日に八重洲ブックセンター本店さんで新刊イベントを行います</a>

