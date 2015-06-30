English / [Japanese・日本語](https://github.com/in3etween/brackets-show-whitespace-Japanese/blob/JapaneseCompatible/README.ja.md)
# Show Whitespace Japanese Compatible

> A [Brackets](http://brackets.io/) extension to visualize whitespace (both spaces and tabs) in the same style as [Sublime Text](http://www.sublimetext.com/).

This bracket extension is a modification of [Brackets Show Whitespace](https://github.com/DennisKehrig/brackets-show-whitespace/) by Dennis Kehrig.

This version of the extension is modified to display 2-byte full width (*Zenkaku*) spaces. The menu string is translated into Japanese. The menu text is also localized to Japanese.

## Usage

Activate using `View > Show Whitespace` or by using the shortcut `Ctrl-Shift-W` (`Command-Shift-W` on Mac OS X). The extension state is remembered across Brackets launches. Whitespace in all editor windows are visualized, including inline editors.

## Technical Details

This extension uses [CodeMirror](http://codemirror.net/) overlays to construct and render whitespace for both spaces and tabs. Each individual character is wrapped in a `<span></span>` with an appropriate denoting class. The following are all the classes this extension uses and their purpose. Do note that tabs and 2-byte spaces follow this same structure, with the word `space` replaced with `tab`. Japanese 2-byte spaces (*zenkaku spaces*) are replaced with `zenkaku`.

* `.cm-dk-whitespace-space`: Whitespace between any characters
* `.cm-dk-whitespace-leading-space`: Whitespace that makes up any indentation
* `.cm-dk-whitespace-empty-line-space`: Any lines that consist solely of whitespace
* `.cm-dk-whitespace-trailing-space`: Whitespace at the end of a line after any characters

The primary extension styling is defined in `styles/main.less`, which is compiled into CSS, while whitespace colors are defined in Brackets preferences and rendered into `styles/whitespace-colors-css.tmpl`. Both files are then loaded into Brackets on startup.

## Install

~Method 1: Open the Brackets Extension Manager and search for "show whitespace Japanese"~*To be implemented soon~

Method 2: Download the [latest revision](https://github.com/in3etween/brackets-show-whitespace-Japanese/archive/JapaneseCompatible.zip) in `.zip` archive directly from GitHub and drag it onto the "Drag .zip here" area in the Extension Manager. Alternatively, use the "Install from URL..." link also in the Extension Manager.

## Known Issues

* CodeMirror overlays have a side effect of slowing down the editor in many aspects, including typing and scrolling. If the slowdown is too unbearable, it may be worthwhile to disable the extension except when required.

## License

[MIT](LICENSE)
**The original extension was created by Dennis Kehrig, and modifications to support 2-byte spaces created by zoomSK.**