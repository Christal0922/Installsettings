sublime text3
[TOC]
# 安装插件
+ Ctrl+Shift+P, install
Markdown Preview
MarkdownEditing

## markdown的使用
+ Ctrl+Shift+P mdp
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
+ 插入链接：Ctrl+Win+K
"mdl+tab"
[Markdown](https://blog.csdn.net/qazxswed807/article/details/51235792 "Sublime Markdown")
+ 插入图片：Shift+Win+K
![Alt text](/path/to/img.jpg "Optional title")

## markdown的快捷键1
+ 批量修改  
选中想要的元素后，一直按住Ctrl+D键可以选中所有相同的元素
    + 添加选择：Ctrl
    + 减少选择：Alt
+ 新建python文件：Ctrl+Alt+M (通过Key Bindings设置)
```
    {
        "caption": "Tmpl: Create python",
        "command": "sublime_tmpl",
        "keys": ["ctrl+alt+M"],
        "args": {"type": "python"}
    }
```
+ 多行光标批量快速操作  
    Ctrl+Alt+↓
    按end定位至行尾
+ 打开命令面板：Ctrl+Shift+P
+ 运行当前代码：Ctrl+B, 或者SublimeREPL插件定义的F5
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
