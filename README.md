Sublime Text 3 常用快捷键 

# 常规

    F6                        检测语法错误
    F11                       全屏模式
    Shift + F11               全屏免打扰模式，只编辑当前文件
    Esc                       退出光标多行选择，退出搜索框，命令框等。
    Ctrl + Shift + P          打开命令面板

# 移动

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

# 选择

    Ctrl + D                  选词
    Alt  + F3                 选择所有相同的词
    Ctrl + Shift + M          选择括号内的内容
    Ctrl + L                  选择整行（按住-继续选择下行）
    Ctrl + Shift + L          选中多行，按下快捷键，即可同时编辑这些行

# 操作

## 增：

    Ctrl + Enter              下方插入新行
    Ctrl + Shift + Enter      上方插入新行
    Ctrl + Shift + D          复制光标所在整行，插入在该行之前

## 删：

    Ctrl + KK                 删除到行尾
    Ctrl + Shift + K          删除整行
    Ctrl + X                  删除当前行

## 改：

    Ctrl + J                  合并行
    Ctrl + K + U              改为大写
    Ctrl + K + L              改为小写
    Ctrl + /                  注释当前行
    Ctrl + Shift + /          注释已选择内容
    Ctrl + Shift + ↑          可以移动此行代码，与上行互换
    Ctrl + Shift + ↓          可以移动此行代码，与下行互换

## 查：

    Ctrl + F                  搜索内容
    ctrl + shift + F          在文件夹内查找
    Ctrl + H                  替换

# 配置项

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
[
  { "keys": ["alt+shift+f"], "command": "reindent" }
]
```
# 安装 Package Control

```
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```

常用插件：

-   Markdown Editing
    
    提供了Markdown格式的高亮显示

-   Markdown Preview
    
    预览生成HTML的效果

    `Shift+Ctrl+P` 查看可用选项

    深入了解: 
    <a href="http://www.cnblogs.com/IPrograming/p/Sublime-markdown-editor.html" target="_blank">http://www.cnblogs.com/IPrograming/p/Sublime-markdown-editor.html</a>


# 中文输入 
解决Ubuntu下Sublime Text 3无法输入中文：

<a href="http://www.jianshu.com/p/bf05fb3a4709" target="_blank">http://www.jianshu.com/p/bf05fb3a4709</a>
