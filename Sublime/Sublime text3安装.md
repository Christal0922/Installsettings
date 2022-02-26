Sublime text3安装
# 安装package control
+ 直接安装，在安装文件夹新建名为Data的文件夹
+ 破解注册码
```
Member J2TeaM
Single User License
EA7E-1011316
D7DA350E 1B8B0760 972F8B60 F3E64036
B9B4E234 F356F38F 0AD1E3B7 0E9C5FAD
FA0A2ABE 25F65BD8 D51458E5 3923CE80
87428428 79079A01 AA69F319 A1AF29A4
A684C2DC 0B1583D4 19CBD290 217618CD
5653E0A0 BACE3948 BB2EE45E 422D2C87
DD9AF44B 99C49590 D2DBDEE1 75860FD2
8C8BB2AD B2ECE5A4 EFC08AF2 25A9B864
```

# Package Contrl的安装
+ Ctrl+Shift+P 调出控制面板，输入install package control安装package control
+ 安装成功后，按住Ctrl+Shift+P 输入pci，可以安装包
+ Package Control的用户自定义配置  
Preferences -> Package settings -> Package Control -> Settings -> User
添加如下代码
```
{
	"bootstrapped": true,
	"channels":
	[
		"E:\\Program\\Sublime Text 3\\Sublime Text 3\\Channel\\channel_v3.json"
	]
}

```


# channel_v3.json下载
+ 文件获取
你用浏览器访问这个网址：https://packagecontrol.io/channel_v3.json
这是一个json，如果你联网了并且可以访问到，那么保存它，将其命名为channel_v3.json
+ 修改schema_version
打开这个channel_v3.json的文件，全文查找，找到schema_version，你会发现后面跟着的是3.0.0，修改以下，换成2.0，对！就是2.0，不是2.0.0！
将其保存着安装目录下，可新建Channel文件夹并进行保存

# 修改显示设置
+ 打开Preferences –>>Settings(Settings User),在右侧添加如下代码（font_face及font_size可根据个人喜好更改）
# 修改注释颜色
默认的注释颜色是灰色，如果看起来不舒服的话，使用如下方法进行修改
+ 打开命令面板，搜索”Package ResourceViewer:Open Resource”
+ 搜索“Color Scheme -Default”，搜索”Monokai.sublime-color-scheme”,并打开文件
+ 搜索关键字“comment”，按照自己的喜欢修改颜色,如改成#BABABA
![图片](https://note.youdao.com/s/947BkqTv)

# 常用插件
## PackageResourceViewer 查看文件
如 Ctrl+Shift+P -> PackageResourceView:Open Resource
-> 输入python -> 选择Python.sublime-build
## sublime Tmpl Python 模板文件
+ 在Preferences->Browse Packages->SublimeTmpl->templates中找到对应的模板文件即可编辑
```
'''
!/usr/bin/env python
-*- coding: utf-8 -*-

+----------------------------------------------------------------------------+
@File Name   : ${saved_filename}
@Description :
@Date        : ${date}
@Author      : ${author} (${email})
@Link        : ${link}
@Version     : \$Id\$
@CSDN        : ${link}
+----------------------------------------------------------------------------+
'''

${1:import os}
```
+ 模板文件支持使用变量，变量在Preferences->Package Settings -> SublimeTmpl->Settings - User添加如下类型的键值对即可设置
+ Python默认快捷键为Ctrl+Alt+M,可以在此修改
    进入Preferences->Package Settings -> SublimeTmpl -> Key Bindings - User
```
[
    {
        "caption": "Tmpl: Create python",
        "command": "sublime_tmpl",
        "keys": ["ctrl+alt+m"],
        "args": {"type": "python"}
    }
]
```

## Anaconda
+ Ctrl+Shift+P打开控制面板，输入pci,输入Anaconda
+ Preferences->Package Settings->Anaconda->Settings Default,修改"python_interpreter"为实际Python安装路径
+ Preferences->Package Settings->Anaconda->Settings User，添加如下内容
```
{
    "python_interpreter":"E:\\Program\\Anaconda\\python.exe",
    "suppress_word_completions":true,
    "suppress_explicit_completions":true,
    "comlete_parameters":true,
    "swallow_startup_errors":true,
    "anaconda_linting":false
}
```
## SublimeREPL 实现python交互
+ SublimeREPL快捷键的设置
```
    {   
    "keys":["f5"],
    "command": "repl_open",
    "caption": "Python - RUN current file",
    "id": "repl_python_run",
    "mnemonic": "R",
    "args": {
        "type": "subprocess",
        "encoding": "utf8",
        "cmd": ["python", "-u", "$file_basename"],
        "cwd": "$file_path",
        "syntax": "Packages/Python/Python.tmLanguage",
        "external_id": "python",
        "extend_env": {"PYTHONIOENCODING": "utf-8"}
        }
    },

    {
    "keys": ["f8"],
    "command": "repl_open",
    "caption": "Python - PDB current file",
    "id": "repl_python_pdb",
    "mnemonic": "D",
    "args": {
        "type": "subprocess",
        "encoding": "utf8",
        "cmd": ["python", "-i", "-u", "-m", "pdb", "$file_basename"],
        "cwd": "$file_path",
        "syntax": "Packages/Python/Python.tmLanguage",
        "external_id": "python",
        "extend_env": {"PYTHONIOENCODING": "utf-8"}
        }
    },
```
+ Python.exe位置修改
    + 找到安装包位置，打开文件SublimeREPL/config/Python/Main.sublime-menu
    + 在cmd项修改第一个元素，即你的python命令文件位置，这个cmd选项对应插件运行python的选项。选错了的话是无法正常运行的
+ SublimeREPL -> Settings-user
```
{
    "default_extend_env": {"PATH":"E:\\PythonT\\venv\\Python310a\\Scripts"}
}
```

# 可选插件
## Markdown Preview 预览网页结果
+ 快捷键 Alt+M
    + 快捷键的设置
    ```
    {
        "keys": ["alt+m"],
        "command": "markdown_preview",
        "args": {
            "target": "browser",
            "parser":"markdown"}
    },
    ```
## ConvertToUTF 
-解决中文乱码问题
## AutoFileName 
-提示文件路径，快速输入文件名，在输入文件路径时会自动提示，如路径名、图片选取等
## Virtualenv 虚拟环境
## SideBarEnhancement 侧边栏优化
## SublimeCodeIntel 
部分语言增强自动完成功能，包括了 Python 。这个插件同时也可以让你跳转到符号定义的地方，通过按住 alt 并点击符号。非常方便
