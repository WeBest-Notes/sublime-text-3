# 基础

## 常规

    F6                        检测语法错误
    F11                       全屏模式
    Shift + F11               全屏免打扰模式，只编辑当前文件
    Esc                       退出光标多行选择，退出搜索框，命令框等。
    Ctrl + Shift + P          打开命令面板

## 移动

    Alt + 数字                切换打开第N个文件

    Ctrl + G                  ：跳转到相应的行
    Ctrl + R                  @ 快速列出/跳转到某个函数
    Ctrl + ;                  # 查找变量名
    Ctrl + P                  查找当前项目中的文件和快速搜索；
                              输入 @ 查找文件主标题/函数
                              输入 # 查找变量名
                              输入 : 跳转到文件某行

    Ctrl + ←                  向左单位性地移动光标，快速移动光标。
    Ctrl + →                  向右单位性地移动光标，快速移动光标。

    Ctrl + F2                 设置/取消书签
    F2                        下一个书签
    Shift + F2                上一个书签

## 选择

    Ctrl + D                  选词
    Alt  + F3                 选择所有相同的词
    Ctrl + Shift + M          选择括号内的内容
    Ctrl + L                  选择整行（按住-继续选择下行）
    Ctrl + Shift + L          选中多行，按下快捷键，即可同时编辑这些行

# 常用操作

## 增加

    Ctrl + Enter              下方插入新行
    Ctrl + Shift + Enter      上方插入新行
    Ctrl + Shift + D          复制光标所在整行，插入在该行之前

## 删除

    Ctrl + KK                 删除到行尾
    Ctrl + Shift + K          删除整行
    Ctrl + X                  删除当前行

## 修改

    Ctrl + J                  合并行
    Ctrl + K + U              改为大写
    Ctrl + K + L              改为小写
    Ctrl + /                  注释当前行
    Ctrl + Shift + /          注释已选择内容
    Ctrl + Shift + ↑          可以移动此行代码，与上行互换
    Ctrl + Shift + ↓          可以移动此行代码，与下行互换

## 查询

    Ctrl + F                  搜索内容
    ctrl + shift + F          在文件夹内查找
    Ctrl + H                  替换

# 配置项

## 编辑器配置

```javascript
{
    // Encoding used when saving new files, and files opened with an undefined
    // encoding (e.g., plain ascii files). If a file is opened with a specific
    // encoding (either detected or given explicitly), this setting will be
    // ignored, and the file will be saved with the encoding it was opened
    // with.
    "default_encoding": "UTF-8",

    // Determines what character(s) are used to terminate each line in new files.
    // Valid values are 'system' (whatever the OS uses), 'windows' (CRLF) and
    // 'unix' (LF only).
    "default_line_ending": "unix",

    // Note that the font_face and font_size are overridden in the platform
    // specific settings file, for example, "Preferences (Linux).sublime-settings".
    // Because of this, setting them here will have no effect: you must set them
    // in your User File Preferences.
    "font_size": 10,

    // Columns in which to display vertical rulers
    "rulers": [80],


    // The number of spaces a tab is considered equal to
    "tab_size": 2,

    // Set to true to insert spaces when tab is pressed
    "translate_tabs_to_spaces": true,

    // Disables horizontal scrolling if enabled.
    // May be set to true, false, or "auto", where it will be disabled for
    // source code, and otherwise enabled.
    "word_wrap": "false",
}
```

## 快捷键配置

```javascript
[
  { "keys": ["alt+shift+f"], "command": "reindent" }
]
```

# 常见问题

## 调出 console

```
Ctrl + `
```

## 安装 Package Control

详细： <https://packagecontrol.io/installation>

```
import urllib.request,os; 
pf = 'Package Control.sublime-package'; 
ipp = sublime.installed_packages_path(); 
urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); 
open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```

## Ubuntu下无法输入中文 

1.  安装搜狗输入法

2.  下载需要的文件

    ```
    git clone https://github.com/lyfeyaj/sublime-text-imfix.git
    ```

3.  将 subl 移动到/usr/bin/，将 sublime-imfix.so 移动到/opt/sublime_text/

    ```
    cd ~/sublime-text-imfix
    sudo cp ./lib/libsublime-imfix.so /opt/sublime_text/
    sudo cp ./src/subl /usr/bin/
    ```

4.  用 subl 命令启动sublime

5.  详细

    <http://www.jianshu.com/p/bf05fb3a4709>

# 插件

## 参考资料

-   [Sublime Text 最佳插件列表](http://www.uis.cc/content-9-344-1.html)

-   [一些必不可少的Sublime Text 2插件](http://www.qianduan.net/essential-to-sublime-the-text-2-plugins/)

## WebInspector

-   简介
    
    在 JavaScript调试方面，这是一个令人惊讶的工具

-   官方

    <https://github.com/sokolovstas/SublimeWebInspector>

## sublime_debugger

-   简介

    调试工具

-   官网

    <https://github.com/shuky19/sublime_debugger>

## Emmet

-   简介

    快速编写 HTML/CSS 的编辑器中最流行的插件之一
    
-   官网

    <http://ipestov.com/the-best-plugins-for-sublime-text/>
    
## Zen Coding

-   简介

    Emmet 的前身

-   官网

    <https://bitbucket.org/sublimator/sublime-2-zencoding>

-   详细

    [《Zen Coding: 一种快速编写HTML/CSS代码的方法》](http://www.qianduan.net/zen-coding-a-new-way-to-write-html-code)

## Git
    
-   简介

    使用编辑器直接和Git协同工作

-   官网

    <https://github.com/kemayo/sublime-text-git>

## Glue

-   简介

    会在界面下方显示一个小窗口，你可以在那里写Shell脚本。

-   官网

    <https://github.com/chrissimpkins/glue>

## GitGutter & Modific

-   简介

    这些插件可以高亮相对于上次提交有所变动的行，换句话说是实时的diff工具。

-   简介

    <https://github.com/jisaacks/GitGutter>

    <https://github.com/gornostal/Modific>

## BracketHighlighter

-   简介

    打开/折叠代码，高亮匹配

-   官网

    <https://sublime.wbond.net/packages/BracketHighlighter>

## AutoFileName

-   简介

    自动补全文件路径

-   官网

    <https://github.com/BoundInCode/AutoFileName>

## AllAutocomplete

-   简介

    基于已打开的文件补全代码

-   官网

    <https://github.com/alienhard/SublimeAllAutocomplete>

## DocBlockr

-   简介

    编写代码注释的有效工具

-   官网

    <https://github.com/spadgos/sublime-jsdocs>

-   详细

    <https://sublime.wbond.net/packages/DocBlockr>

## ColorPicker & GutterColor & ColorHighlightergutter

-   简介

    调色盘，写 CSS 非常方便

-   官网

    <https://github.com/weslly/ColorPicker>

    <https://github.com/ggordan/GutterColor>

    <https://github.com/Monnoroch/ColorHighlighter>

## Colorcoder

-   简介

    高亮所有变量

-   官网

    <https://github.com/vprimachenko/Sublime-Colorcoder>

## PlainTasks

-   简介

    杰出的待办事项表

-   官网

    <https://github.com/aziz/PlainTasks>

## MarkdownEditing

-   简介

    提供了Markdown格式的高亮编辑显示

-   官网

    <https://github.com/ttscoff/MarkdownEditing>

## MarkdownPreview

-   简介

    预览生成HTML的效果

-   官网

    <https://github.com/revolunet/sublimetext-markdown-preview>

-   深入了解: 

    <http://www.cnblogs.com/IPrograming/p/Sublime-markdown-editor.html>

## Vintage & ActualVim

-   简介

    支持 vi 编辑器的操作

-   官网

    <https://github.com/sublimehq/Vintage>

    <https://github.com/lunixbochs/actualvim>

## Inc-Dec-Value

-   简介

    增加或减少数字, 日期, 十六进制彩色值等等

-   官网
    
    <https://github.com/rmaksim/Sublime-Text-2-Inc-Dec-Value>


## Alignment

-   简介

    Package Control作者写的简单到极致的多行选择和多行选择对齐插件

    ”=”号对齐, 变量定义太多，长短不一，可一键对齐

-   官网

    <https://github.com/wbond/sublime_alignment>

-   使用

    默认快捷键Ctrl+Alt+A和QQ截屏冲突，可设置其他快捷键如：Ctrl+Shift+Alt+A；先选择要对齐的文本

## SublimeAlignment

-   简介

    用于代码格式的自动对齐

-   官网

    <https://github.com/wbond/sublime_alignment>

## Clipboard History

-   简介

    粘贴板历史记录，方便使用复制/剪切的内容

-   官网

    <https://github.com/kemayo/sublime-text-2-clipboard-history>

-   使用：

    Ctrl+alt+v：显示历史记录

    Ctrl+alt+d：清空历史记录
    
    Ctrl+shift+v：粘贴上一条记录（最旧）
    
    Ctrl+shift+alt+v：粘贴下一条记录（最新）


## IMESupport

-   简介

    sublime中文输入法

    还在纠结 Sublime Text 中文输入法不能跟随光标吗？试试「IMESupport 」这个插件吧！
    目前只支持 Windows，在搜索等界面不能很好的跟随光标。

-   官网

    <https://github.com/chikatoike/IMESupport>

-   使用

    Ctrl + Shift + P →输入pci →输入IMESupport →回车

## SublimeLinter

-   简介

    一个支持lint语法的插件，可以高亮linter认为有错误的代码行

-   官网

    <https://github.com/kronuz/SublimeLinter/>

## Nettuts-Fetch

-   简介

    可以自动更新一些开源库

-   官网

    <https://github.com/weslly/Nettuts-Fetch>

## JsMinifier

-   简介

    该插件基于Google Closure compiler，自动压缩js文件。

-   官网

    <https://github.com/cgutierrez/JsMinifier>

## ConvertToUTF8

-   简介

    将文件编码从GBK转黄成UTF8，快捷键Ctrl+Shift+C

-   官网

    <http://www.sublimetext.com/forum/viewtopic.php?f=5&p=22274>

# 主题和配色方案

## 参考资料

-   [主题](https://github.com/daylerees/colour-schemes)

-   [配色方案](http://colorsublime.com/)

## Soda

-   官网

    <http://buymeasoda.github.io/soda-theme/>

## Spacegray

-   官网

    <http://kkga.github.io/spacegray/>

## Flatland

-   官网

    <https://github.com/thinkpixellab/flatland>

## Tomorrow

-   官网

    <https://github.com/chriskempson/tomorrow-theme>

## Base 16

-   官网

    <https://github.com/chriskempson/base16>

## Solarized

-   官网

    <http://ethanschoonover.com/solarized>

## Predawn

-   官网

    <https://github.com/jamiewilson/predawn>

## itg.flat

-   官网

    <https://sublime.wbond.net/packages/Theme%20-%20itg.flat>

