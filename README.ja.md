[English](https://github.com/in3etween/brackets-show-whitespace-Japanese/blob/JapaneseCompatible/README.md) / Japanese・日本語
# Brackets空白表示エクステンション  (全角スペース対応版)

> [Brackets](http://brackets.io/)で空白を[Sublime Text](http://www.sublimetext.com/)風に表示するエクステンションの日本語全角スペース対応版です。

このエクステンションはDennis Kehrig氏の[Brackets Show Whitespace](https://github.com/DennisKehrig/brackets-show-whitespace/)を改良したものです。
全角スペースを四角として表示します。また、メニュー項目も日本語にローカライズしています。

## 使用方法

メニューから`表示 > 空白を表示`を選択するか、`Ctrl-Shift-W` (OS Xでは`Command-Shift-W`)のショートカットで有効に出来ます。エクステンションの状態はBracketsを修了しても保持されます。インライン編集を含めて全てのウィンドウで空白を表示します。

## 技術的詳細

このエクステンションは[CodeMirror](http://codemirror.net/)のオーバーレイ機能を使ってスペースやタブなどの空白を可視化します。各空白文字は対応するクラスをつけた`<span></span>`タグで閉じられます。このエクステンションで使用されているクラスは以下の通りです。タブや全角スペースはそれぞれ`space`の代わりに`tab`、`zenkaku`に置き換えられます。

* `.cm-dk-whitespace-space`: 文字に挟まれた空白
* `.cm-dk-whitespace-leading-space`: インデントに使用されている空白
* `.cm-dk-whitespace-empty-line-space`: 空白のみを含む行
* `.cm-dk-whitespace-trailing-space`: 空白以外の文字があり、空白で終わる行の空白

エクステンションの基本的なレイアウトは`styles/main.less`で定義されていて使用時にCSSにコンパイルされます。空白の色はBracketsの環境設定ファイルで定義され、`styles/whitespace-colors-css.tmpl`のものが書き込まれます。両ファイルともBrackets起動時に読み込まれます。

## インストール方法

~~方法1: Bracketsの拡張起動マネージャーを開いて"show whitespace Japanese"で検索してください。~~*実装予定*

方法2: Githubから[最新版](https://github.com/in3etween/brackets-show-whitespace-Japanese/archive/JapaneseCompatible.zip)をダウンロードし、`.zip`ファイルをそのままBracketsの拡張機能マネージャーの ".zipをここにドラッグ"にドラッグしてください。また、"URLからインストール"リンクからインストールできます。

## 既知の問題

* CodeMirrorオーバーレイによってスクロール時や入力時にエディタが重くなる場合があります。重すぎると感じたらエクステンションを無効にすると改善する可能性があります。

## License

[MIT](LICENSE)
**このエクステンションはDennis Kehrig氏が作成し、日本語および全角空白はzoomSKが実装したものです。**