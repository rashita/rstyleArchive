---
title : 対話で進捗を記録し、Evernoteにノートを作る「進捗くん」
link : 18588
date : Wed, 20 Jul 2016 02:49:02 +0000
categories : ["evernoteの使い方"]
tags : ["applescript","evernote"]
draft : false
author : 倉下忠憲
---

お手製のAppleScriptです。Macで、Evernoteがインストールされている環境で使えます。

「スクリプトエディタ」を開き、そこに以下のコードをコピっとペーストしてください。スクリプトが「AppleScript」になっているかもチェック。

<a href="https://rashita.net/blog/?attachment_id=18589" rel="attachment wp-att-18589"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot31-500x314.png" alt="screenshot" width="500" height="314" class="alignnone size-medium wp-image-18589" /></a>

※「進捗くん」のコード
<script src="https://gist.github.com/rashita/eeae7b4a44c156227f4e62bef26e4ace.js"></script>

で、実行ボタン（右向きの矢印）をポチッとすれば、テストできます。

<a href="https://rashita.net/blog/?attachment_id=18590" rel="attachment wp-att-18590"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot32-500x366.png" alt="screenshot" width="500" height="366" class="alignnone size-medium wp-image-18590" /></a>


以下は、スクリプトの流れ。

<h3>進捗くんデモ</h3>

起動すると「日報」か「週報」かを尋ねられます。どちらを選んでも以降の動作は基本的に同じで、ダイアログの中身が少し変わる程度です。ここでは「日報」を選んでおきましょう。

<a href="https://rashita.net/blog/?attachment_id=18591" rel="attachment wp-att-18591"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot33.png" alt="screenshot" width="420" height="119" class="alignnone size-full wp-image-18591" /></a>

まずは、「やったこと」の入力。簡単に言えばプロジェクト名ですが、そんなに小難しく考える必要はありません。思いつく「やったこと」の見出しを書き込みましょう。複数入力する場合は「,」で項目を区切って下さい。

<a href="https://rashita.net/blog/?attachment_id=18592" rel="attachment wp-att-18592"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot34.png" alt="screenshot" width="419" height="174" class="alignnone size-medium wp-image-18592" /></a>


<a href="https://rashita.net/blog/?attachment_id=18593" rel="attachment wp-att-18593"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot35.png" alt="screenshot" width="419" height="175" class="alignnone size-medium wp-image-18593" /></a>


すると、「やったこと」一つひとつにたいしてスクリプトが進捗を尋ねてきます。なぜ関西弁なのかと言えば、その方が気楽そうな気がしたからです。

<a href="https://rashita.net/blog/?attachment_id=18594" rel="attachment wp-att-18594"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot36.png" alt="screenshot" width="418" height="298" class="alignnone size-medium wp-image-18594" /></a>

一つ答えたら、次。それが繰り返されます。

<a href="https://rashita.net/blog/?attachment_id=18595" rel="attachment wp-att-18595"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot37.png" alt="screenshot" width="417" height="321" class="alignnone size-medium wp-image-18595" /></a>

すべて終わったら、他にもう何もないかが尋ねられます。何かあったとしましょう。

※「あったわ」を選択
<a href="https://rashita.net/blog/?attachment_id=18596" rel="attachment wp-att-18596"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot38.png" alt="screenshot" width="420" height="118" class="alignnone size-medium wp-image-18596" /></a>

<a href="https://rashita.net/blog/?attachment_id=18597" rel="attachment wp-att-18597"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot39.png" alt="screenshot" width="423" height="297" class="alignnone size-medium wp-image-18597" /></a>

入力を終えたら、もう一度他にもう何もないかが尋ねられます。「なかった」を選択するまでエンドレスです。

※「あらへん」でループから脱出
<a href="https://rashita.net/blog/?attachment_id=18598" rel="attachment wp-att-18598"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot40.png" alt="screenshot" width="419" height="117" class="alignnone size-medium wp-image-18598" /></a>


以上を入力し終えたら、明日（「週報」なら来週）何をするのかを尋ねられますので、思いを語っておきましょう。これが終われば、スクリプトが以上の内容をEvernoteにノートとして作成してくれます。


<a href="https://rashita.net/blog/?attachment_id=18599" rel="attachment wp-att-18599"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot41.png" alt="screenshot" width="418" height="305" class="alignnone size-medium wp-image-18599" /></a>

<a href="https://rashita.net/blog/?attachment_id=18600" rel="attachment wp-att-18600"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot42.png" alt="screenshot" width="420" height="119" class="alignnone size-medium wp-image-18600" /></a>


※作成されたノート（あくまでサンプルです）
<a href="https://rashita.net/blog/?attachment_id=18601" rel="attachment wp-att-18601"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot43-500x516.png" alt="screenshot" width="500" height="516" class="alignnone size-medium wp-image-18601" /></a>

<h3>さいごに</h3>

テストが無事終了したら、「スクリプトエディタ」で内容を保存し、形式を「アプリケーション」としておけば、いつでも使えるようになります。

一応私専用に作ったものですが、極端な機能は使っていないので、ごく普通に使えるかと思います。

関西弁が気にくわない方は、スクリプト上で修正していただければ、標準語に戻すことも（他の方言に変更することも）可能です。また、スクリプト内の「h3」を「h4」や「h2」に変えれば、Evernoteに作成されるノートの見た目もちょっぴり変わります。そのあたりは、お好みでどうぞ。

では、皆様も楽しいEvernote Lifeを！

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.07.20</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 3,151<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/515rWUhPqbL._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.07.20</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 33,063<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>



