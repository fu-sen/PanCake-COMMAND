## PanCake コマンド一覧

PanCake で使用できる命令を一覧しています。
0.8 以降のファームウェア対応です。
0.5 はバージョン表記のないコマンドが使用でき、
PANCAKE および PC を付けない形式となります。

Download ZIP でファイル一覧をダウンロードできます。<br />
GitHub・Git を使っている場合は Clone を使っても良いでしょう。

RAW で参照した場合、またファイルをダウンロードした場合<br />
.txt ファイルは文字コード Shift_JIS、改行コード CR+LF になります。<br />
Windows ではメモ帳を使用する事が可能です。

* IchigoJam (公式) http://ichigojam.net/
* PanCake (PCN 内) http://pcn.club/ns/pancake.html
* PCN http://pcn.club/
* イチゴジャム レシピ (公開元) http://15jamrecipe.jimdo.com/


### バイナリコマンド

PanCake では文字列でコマンドを送る以外に<br />
バイナリコマンドが存在します。

記載例: 色番号 10（水色）で画面を消去する（PANCAKE CLEAR 0A）<br />
128 4 0 10 または #80 #04 #00 #0A

これは Pancake 付属ドキュメント readme.txt では<br />
16進数表記で記載されています。この本書では # を頭に付けた値です。

80 04 00 0A

しかし、IchigoJam が当初16進数変換に対応していなかったため、<br />
この文章では10進数のキャラクターコードも記載しています。

これを IchigoJam から Pancake へ送る場合は<br />
例えば次のようになります。

PRINT CHR$(128,4,0,10);<br />
PRINT CHR$(#80,#04,#00,#0A);

PanCake (PCN 内)<br />
http://pcn.club/ns/pancake.html


### ライセンス

この文章は CC BY-NC で公開されている PanCake のページや<br />
Pancake 付属ドキュメント readme.txt<br />
Facebook グループ「IchigoJam-FAN」などの情報を元に<br />
志賀 慶一 (ふうせん Fu-sen.) が独自に文章化しているものです。

Facebook グループ IchigoJam-FAN<br />
https://www.facebook.com/groups/ichigojam/<br />

製作・公開公開にあたり、PanCake の著作者となる<br />
株式会社ナチュラルスタイル (NaturalStyle Co. Ltd.) より<br />
製作・公開許可をいただいています。

NaturalStyle Co. Ltd. http://na-s.jp/

Maked by 志賀 慶一 (ふうせん Fu-sen.) | Keiichi SHIGA ( BALLOON a.k.a. Fu-sen. ), 2015.

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/80x15.png" /></a>

この 文章 は <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">クリエイティブ・コモンズ 表示 - 非営利 4.0 国際</a> (CC BY-NC 4.0) ライセンスで<br />
提供しています。
