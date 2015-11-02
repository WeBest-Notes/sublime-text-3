Sublime Text 3 常用快捷键 

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

## Ubuntu下无法输入中文 

<a href="http://www.jianshu.com/p/bf05fb3a4709" target="_blank">http://www.jianshu.com/p/bf05fb3a4709</a>

# 插件

## Package Control

```
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```

## Vintage

-   简介

    支持 vi 编辑器的操作

## Markdown Editing
    
-   简介

    提供了Markdown格式的高亮显示

## Markdown Preview
    
-   功能
    
    预览生成HTML的效果

-   简介

    `Shift+Ctrl+P` 查看可用选项

-   深入了解: 

    <a href="http://www.cnblogs.com/IPrograming/p/Sublime-markdown-editor.html" target="_blank">http://www.cnblogs.com/IPrograming/p/Sublime-markdown-editor.html</a>

## Alignment

-   功能：”=”号对齐

-   简介：变量定义太多，长短不一，可一键对齐

-   使用：默认快捷键Ctrl+Alt+A和QQ截屏冲突，可设置其他快捷键如：Ctrl+Shift+Alt+A；先选择要对齐的文本

## Doc​Blockr

-   功能：生成优美注释

-   简介：标准的注释，包括函数名、参数、返回值等，并以多行显示，手动写比较麻烦

-   使用：输入/*、/**然后回车，还有很多用法，请参照

-   <https://sublime.wbond.net/packages/DocBlockr>

## IMESupport

-   功能：sublime中文输入法

-   简介：还在纠结 Sublime Text 中文输入法不能跟随光标吗？试试「IMESupport 」这个插件吧！目前只支持 Windows，在搜索等界面不能很好的跟随光标。

-   使用：Ctrl + Shift + P →输入pci →输入IMESupport →回车

## AutoFileName

-   功能：快捷输入文件名

-   简介：自动完成文件名的输入，如图片选取

-   使用：输入”/”即可看到相对于本项目文件夹的其他文件


## Clipboard History

-   功能：粘贴板历史记录

-   简介：方便使用复制/剪切的内容

-   使用：

    Ctrl+alt+v：显示历史记录
    Ctrl+alt+d：清空历史记录
    Ctrl+shift+v：粘贴上一条记录（最旧）
    Ctrl+shift+alt+v：粘贴下一条记录（最新）

## Bracket Highlighter

-   功能：类似于代码匹配，可以匹配括号，引号等符号内的范围。

## Zen Coding

-   功能： 《Zen Coding: 一种快速编写HTML/CSS代码的方法》。
