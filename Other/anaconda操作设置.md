Anaconda
# conda常用命令
    1. conda list: 查看安装的包
    2. conda install package_name
    3. conda env list: 查看当前存在哪些虚拟环境
    4. conda update conda: 检查更新当前conda
# 虚拟环境
```
# 获取Anaconda的虚拟环境
conda info --envs
# 激活
conda activate E:\Program\Anaconda
# 查看python版本
python
# 退出python
exit()

# 创建虚拟环境
conda create --name Python310m python=3.10
# 切换到环境Python310m
conda activate Python310m
python --version
# 退出当前环境
conda deactivate
# 删除环境
conda remove --name Python310m --all
```
## Python版本问题
将原生Python安装位置的python.exe文件重命名为Python3
将Anaconda文件夹里的python.exe文件重命名为python-ana
```
# 输入Python3 启动原生的Python
# 查看当前python的版本
Python3 –m pip –-version
# 查看当前Python对应的pip安装的第三方库
Python3 –m pip list
# install
Python3 -m pip install NumPy
# 卸载
Python3 -m pip uninstall NumPy
# 升级pip命令
Python3 -m pip install -U pip

# 输入Python-ana 启动anaconda
Python-ana –m pip –-version
Python-ana –m pip list
Python-ana –m pip install 库名
Python-ana –m pip uninstall 库名
```
## Python版本与numpy版本不匹配
```
# 卸载当前包
Python3 -m pip uninstall numpy
Python3 -m pip install numpy==1.18.1
```