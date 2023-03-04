---
title : Evernoteのショートカットに業務日誌を重ねる
link : 9777
date : Wed, 13 Feb 2013 03:58:35 +0000
categories : ["「タスク」の研究","物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

小ネタです。

最近、実験的に「デイリータスクリスト」をEvernoteで管理するようにしています。

正確に言うと、デイリータスクリスト+業務日誌、という体裁です。


<a href="https://rashita.net/blog/wp-content/uploads/2013/02/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/02/screenshot1.png" alt="screenshot" width="210" height="406" class="alignnone size-full wp-image-9778" /></a>


ここにタイマー（時間ログ）が加われば天下無敵なのですが、そちらはXcode+AppleScriptでちょこちょこ作成中。

ちなみに、このデイリータスクリストの作成もAppleScriptで行っています。

ここまでが前振り。

<h3>ショートカットに置く</h3>
毎日一枚のノートを作成しているわけですが、そのノートはその日頻繁にアクセスすることになります。

当然、そういうノートはMacクライアントの新機能「ショートカット」に入れておくのが便利ですね。
※『SmartEver』で確認できるように「SmartEver」タグも付けておくとさらに便利。

初めは、
<em>
その日のノートを作成→ショートカットに登録→前日分をショートカットから排除</em>

というサイクルを回していました。つまり、その日のノートだけが常にショートカットに表示されている状態を保つわけです。

が、すこし考えを改めました。

<h3>ログを仮蓄積</h3>
現状はこういう風に、一週間分のノートを蓄積しています。

<a href="https://rashita.net/blog/wp-content/uploads/2013/02/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/02/screenshot2.png" alt="screenshot" width="187" height="479" class="alignnone size-full wp-image-9779" /></a>


こうしておくと、前日以前の業務日誌がすぐに確認できます。で、そういう場面が結構あるのです。その時、いちいち検索するのも面倒なので、ショートカットに常駐させることにしました。

で、一週間経って、週次レビューの際にこのノート群を再読し、確認し終えたものはショートカットから外します。すると訪れるスッキリ感！、という具合です。

<h3>さいごに</h3>
このシステムはまだまだ不十分ですが、なかなか面白い要素の可能性も眠っています。

AppleScriptにもうもう少し精通しているとシステム構築の速度も上がるんですけども・・・。まあ、ぼちぼちいきます。

<strong>▼こんなアプリ＆一冊も：</strong>

<a href="http://click.linksynergy.com/fs-bin/stat?id=Q0goZPzeHEw&offerid=94348&type=3&subid=0&tmpid=2192&RD_PARM1=https%253A%252F%252Fitunes.apple.com%252Fjp%252Fapp%252Fsmartever-sakusaku-shieru%252Fid493990103%253Fmt%253D8%2526uo%253D4%2526partnerId%253D30" target="_blank" rel="nofollow"><img width="75" class="alignleft" align="left" src="http://a1946.phobos.apple.com/us/r1000/062/Purple/v4/03/e5/86/03e5863b-78e4-fab1-d7c6-9adb6d9ca301/mza_5251020485347599819.75x75-65.png" style="border-radius: 11px 11px 11px 11px;-moz-border-radius: 11px 11px 11px 11px;-webkit-border-radius: 11px 11px 11px 11px;box-shadow: 1px 4px 6px 1px #999999;-moz-box-shadow: 1px 4px 6px 1px #999999;-webkit-box-shadow: 1px 4px 6px 1px #999999;margin: -5px 15px 1px 5px;"></a><strong> SmartEver - サクサク使える軽量Evernoteクライアント 1.4（￥170）</strong><a href="http://click.linksynergy.com/fs-bin/stat?id=Q0goZPzeHEw&offerid=94348&type=3&subid=0&tmpid=2192&RD_PARM1=https%253A%252F%252Fitunes.apple.com%252Fjp%252Fapp%252Fsmartever-sakusaku-shieru%252Fid493990103%253Fmt%253D8%2526uo%253D4%2526partnerId%253D30" target="_blank" rel="nofollow"><img src="http://r.mzstatic.com/htmlResources/2338/images/viewinitunes_jp.png" style="vertical-align:bottom;" width="90" alt="App"></a><br> カテゴリ: 仕事効率化, ユーティリティ<br> 販売元: <a href="http://click.linksynergy.com/fs-bin/stat?id=Q0goZPzeHEw&offerid=94348&type=3&subid=0&tmpid=2192&RD_PARM1=https%253A%252F%252Fitunes.apple.com%252Fjp%252Fartist%252Fmakoto-setoh%252Fid297356141%253Fuo%253D4%2526partnerId%253D30" target="_blank" rel="nofollow">Makoto Setoh - Makoto Setoh</a>（サイズ: 3.8 MB）<br style="clear: both;">

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 12017<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/Applescript-Definitive-Guide-Matt-Neuburg/dp/0596102119%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D0596102119" target="_blank">Applescript: The Definitive Guide</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/Applescript-Definitive-Guide-Matt-Neuburg/dp/0596102119%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D0596102119" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51T-jIjWOrL._SL160_.jpg" border="0" alt="Applescript: The Definitive Guide" /></a></td><td valign="top"><font size="-1">Matt Neuburg <br /><br />Oreilly & Associates Inc  2006-01<br />売り上げランキング : 104021<br /><br /><br /><a href="http://www.amazon.co.jp/Applescript-Definitive-Guide-Matt-Neuburg/dp/0596102119%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D0596102119" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

