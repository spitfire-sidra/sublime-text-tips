sublime-text-tips
=================

<link rel="stylesheet" href="http://michaelhue.com/keyscss/keyscss/keys.css" type="text/css" />

## Useful Shortcuts (Mac OS X)

### 指令輸入視窗 (Command Palette)

- command + shift + P

### Python Console

Ctrl+`

### 多重選取

- 選取文字之後 一直按 `command + d` 可以一個個將相同的文字選起來 然後就可以一次修改

- 選取文字之後，按 `ctrl + command + G` 就可以一次將所有相同文字都選起來

### 行操作

- 合併多行成一行 選起要合併的文字之後 按 `command + j`

- 上下行互換 `command + ctrl + 上/下 方向鍵`

- 多行註解 選取文字之後 `command + shift + /`, 單行是 `command + /`

- 多行註解 選取文字之後 `command + shift + P` 輸入 toggle comment, toggle block comment

### 文字編輯

- 大小寫轉換 選取文字之後  `command + k, u/U`

- 大小寫轉換  選取文字之後 `command + shift + P` 輸入 title, lower case, upper case

### 搜尋/取代

- 全專案搜尋 ＆ 取代  `command + shitf + f`

### 游標操作

- 跳去某一行 command + p 輸入 :行數

- 跳到對應的 大小括號 中括號 `ctrl + m`

- 跳至第幾行 `ctrl+G` 後輸入行號

### 捲軸操作

- 移動捲軸 `ctrl + alt + 上/下 方向鍵`

### 分頁操作

- 分頁間切換 `command + alt + 左右方向鍵`

- 水平切割視窗 `command + alt + shift + 2/3/4`

- 垂直切割視窗 `command + alt + 2/3/4`

### HTML

關閉目前的 html 標籤 `command + alt + .`


更多: http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/reference/keyboard_shortcuts_osx.html


## 基本設定 (Mac OS X)

Preferences > Settings — User 可以打開設定檔 (快捷鍵: `command + ,`)

貼上以下設定 (註：Sublime Text所有設定檔都是 JSON 格式)

```
{
	"always_show_minimap_viewport": true, // 顯示右邊的縮圖
	"draw_minimap_border": true, // 右邊的縮圖要畫邊線
	"caret_style": "solid",  // 將游標變 no blinking
	"wide_caret": true, // 將游標變寬
	"file_exclude_patterns": // 要忽略的檔名格式
    [
        ".DS_Store",
        "*.pid",
        "*.pyc"
    ],
	"folder_exclude_patterns": // 會被Sublime Text忽略的資料夾名，不會顯示在 Sidebar
	[
		".svn",
		".git",
		".hg",
		"CVS",
		"__pycache__"
	],
	"font_size": 18,
	"ignored_packages":
	[
	    "vintage" // 如果想打開 vi 模式，就刪除此行
	],
	"rulers": // 尺標，寫程式經常要注意是否寫太長，就可以用尺標提醒自己
 	[
		72,
		79
	],
	"tab_size": 4, // Tab 的寬度，4 個 Space 的寬度
	"translate_tabs_to_spaces": true, // 強制將 Tab 用 Space 來取代
	"trim_trailing_white_space_on_save": true,  // 存檔時，自動將行尾的空白去掉
	"ensure_newline_at_eof_on_save": true,
}
```
## 不同語言不同設定檔

For language specific settings click Sublime Text > Preferences > Settings – More > Syntax Specific – User. Then save the file using the following format: LANGUAGE.sublime-settings. So, for Python-specific settings, save the file as `Python.sublime-settings`.

```
{
    // editor options
    "draw_white_space": "all",

    // tabs and whitespace
    "auto_indent": true,
    "rulers": [79],
    "smart_indent": true,
    "tab_size": 4,
    "trim_automatic_white_space": true,
    "use_tab_stops": true,
    "word_wrap": true,
    "wrap_width": 80
}
```

更多設定資訊 http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/reference/settings.html

## 更換字體

推薦程式用的字體下載 http://www.slant.co/topics/67/~what-are-the-best-programming-fonts

```
    // Font設定範例
    "font_face": "Ubuntu Mono",
    "font_size": 16.0,
    "font_options": ["subpixel_antialias", "no_bold"],
    "line_padding_bottom": 0,
    "line_padding_top": 0,
```

## 必裝 Packages

- Package Control https://sublime.wbond.net/installation#st3

## 推薦的Packages

### 佈景主題類

- Flatland

```
{
  "theme": "Flatland Dark.sublime-theme",
  "color_scheme": "Packages/Theme - Flatland/Flatland Dark.tmTheme"
}
```

- Color Scheme - Tomorrow Night 黑暗系的 Color Theme

- Theme - Soda Dark Themes 

color theme 影響的是文字的配色

theme 影響的是sublime text視窗的配色

### vim 愛用者

- Vintageous

### 功能強化類

- SideBarEnhancements 強化SideBar功能 
- SublimeCodeIntel 自動補完功能
- GitGutter 會在編輯器的行數顯示旁邊，依照 Git 編輯的狀態，顯示不同的圖標，例如新增刪除修改
- sublimelinter 提供一個linter的框架，讓你可以安裝不同的 linter  https://github.com/SublimeLinter/SublimeLinter3 
- HTML-CSS-JS Prettify 自動排版 (輸入指令HTMLPrettify 就可以自動排版)


## 如何換佈景主題(Theme)

- colorsublime
    
        http://colorsublime.com/how-to-install-a-theme

- 其他佈景主題

        https://github.com/mediachicken/sublimetext-defaultplus-theme


## 將 Sublime Text 設定為 終端機指令 之一

```
ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

就可以用 `subl` 打開檔案

```
subl helloworld.py
```

## 將 sublime 作為 預設編輯器

要先將Sublime Text 設定為 終端機指令 之一


```
alias nano="subl"
export EDITOR="subl"
```


## 將 Sublime 作为 Git 預設編輯器使用

要先將Sublime Text 設定為 終端機指令 之一

```
export GIT_EDITOR="subl --wait --new-window"
```


## Python 開發者值得一看的設定文章

https://realpython.com/blog/python/setting-up-sublime-text-3-for-full-stack-python-development/


## 前端開發者值得一看的設定文章

http://blog.miniasp.com/post/2014/01/07/Useful-tool-Sublime-Text-3-Quick-Start.aspx





## reference

https://realpython.com/blog/python/setting-up-sublime-text-3-for-full-stack-python-development/

