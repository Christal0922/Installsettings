Windows virtualenv和anaconda的使用
# 创建项目的虚拟环境
E:
cd E:\PythonT\venv
python -m pip install virtualenv # 安装virtualenv

# Virtualenv 
1. virtualenv Pythonana # 创建名为Pythonana的虚拟环境
2. 根据已安装的Python版本创建名为Python310a的虚拟环境
virtualenv -p D:\Users\qian9\AppData\Local\Programs\Python\Python310\python3.exe Python310a
3. virtualenvwrapper进行虚拟环境管理（待研究）

# 激活虚拟环境
Pythonana\Scripts\activate.bat #激活
Python310a\Scripts\activate.bat
python --version #查看python版本

# 退出虚拟环境
deactivate

# 删除虚拟环境
cd E:/PythonT/venv
rm -rf Pythonana

# 安装全局环境的第三方包
如果你需要和全局环境使用相同的第三方包。可以使用如下方法：
1. 导出依赖包 # 待研究requirements.txt为空
pip freeze > requirements.txt
2. 安装依赖包
pip install -r requirements.txt
