# Changelog
##v0．1．0
* **Requires Brackets 1.1 or higher**
* Modified to Show Japanese 2-byte spaces
* Japanese Localization Added
* Changed default colors for empty lines
* **動作環境:Brackets 1.1以上**
* 全角空白を四角で表示されるように変更
* メニュー項目を日本語化
* 空白のみの行のデフォルトカラーを変更


**Below is the Changelog of the original "Show Whitespace" by [Dennis Kehrig](https://github.com/DennisKehrig)**
## v2.1.0 - Unreleased

* **Requires Brackets 1.1 or higher**
* Remove CodeMirror 2 support
* Add new `cm-dk-whitespace-empty-line-space` and `cm-dk-whitespace-empty-line-tab` tokens for recoloring blank lines
* Add user-configurable colors using the Brackets preferences system
* Add support for built-in Brackets dark theme
* Add localization support
* Update events listeners to use event system introduced in Brackets 1.1
* Minor code cleanup

## v2.0.1 - 2014/5/59

* Support Brackets v0.38+
* Update use of PreferencesManager to remove deprecation warnings

## 2012/11/14

Changed the name to "Show Whitespace" as all whitespace is visualized now.

## 2012/06/29

Instead of adding a separate `<div>` with an entry for the indentation of each line, the HTML code that CodeMirror itself produces is augmented. This makes the extension much more reliable and faster. Support for inline editors then is gratis, too - except for refresh calls when the setting is toggled.
