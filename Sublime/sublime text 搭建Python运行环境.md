sublime text 搭建Python运行环境
# Build system
	1. 打开Tools > Build System > New Build System..
	2. 点击New Build System后，会生成一个空配置文件，在这个配置文件内覆盖配置信息，本文python安装路径为“D:/python37”，（注意区分正反斜杠，请将路径换成python实际安装路径），然后按ctrl+s，将文件保存在默认路径，文件名命名为“Python39”
	```
	{
    
    "cmd":["E:\\Program\\Anaconda\\python.exe","-u","$file"],
    "path": "E:\\Program\\Anaconda\\python.exe",
    "file_regex":"^[]*File \"(...*?\",line([0-9]*)",
    "selector":"source.python",
    // 防止中文乱码
    "encoding":"cp936", 
    // 虚拟环境
    "env": {"E:\\Program\\Anaconda\\envs\\mask1": "utf-8"},
    "variants":[
    {
      "name": "Syntax Check",
      "shell_cmd": "python -m py_compile \"${file}\"",
    }
    ``` 
    