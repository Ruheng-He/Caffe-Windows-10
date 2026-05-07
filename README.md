# GitHub link

https://github.com/Ruheng-He/Caffe-Windows-10

# 环境

- Windows 10

- Python 3.5.4

# 下载预编译文件

CAFFE 仓库

- https://github.com/BVLC/caffe/tree/windows

上述仓库的 READMD.md 里的链接已失效，在某个 issue 中找到可用链接。

- https://github.com/BVLC/caffe/issues/6618

- https://drive.google.com/file/d/1blEpBf9DI4DiA6QJ35gLxmTJJ9FLL7uM/view?usp=sharing

解压 VisualStudio2015-CPUonly-Python35.rar，找到 caffe.zip，解压得到如下内容。

```sh
bin
include
lib
python
share
```

# Python 配置

创建虚拟环境。

```sh
.\python.exe -m venv D:\venv
```

激活虚拟环境，升级 pip。

```sh
python -m pip install --upgrade pip
```

把解压 caffe.zip 得到的 python/caffe 文件夹复制到 Python 虚拟环境下的 Lib/site-packages 文件夹里。

尝试 `import caffe`，发现错误 ImportError: No module named 'numpy'。

参照如下命令安装一系列内容即可。

```sh
pip install numpy scikit-image skimage scipy six google protobuf
```
