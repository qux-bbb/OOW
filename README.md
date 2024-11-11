# OOW

Ollama + Open WebUI, 配置成便携版的，解压即可使用。  

Ollama官网: https://ollama.com/  
Open WebUI官网: https://openwebui.com/  


## 下载
方式1: release  
&&&&&&&  

方式2: 夸克网盘  
链接: https://pan.quark.cn/s/c9aaf0ad7854  
提取码: TB6E  

下载后自行校验压缩包的sha256: 7d527edd7e3feecd9acf99a5155fb86509d61895a841e4dfbaafc00c1434efbd  


## 使用
解压后执行 start.bat  
浏览器访问 http://127.0.0.1:8080  
管理员邮箱: admin@localhost  
管理员密码: admin  

关闭窗口即可自动停止运行。


## 下载其他模型
如果需要下载其他模型，可以访问以下地址搜索：  
https://ollama.com/library  

如: https://ollama.com/library/qwen2.5:7b  
访问 http://127.0.0.1:8080, 点击左上角的"Arena Model"，搜索 qwen2.5:7b, 拉取模型使用即可  


## 配置过程
仅供了解配置过程，不需要自己操作。

```r
安装ffmpeg
下载解压到ffmpeg-release-full文件夹
https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z

安装Ollama
下载解压到ollama-windows-amd64文件夹
https://github.com/ollama/ollama/releases/download/v0.4.1/ollama-windows-amd64.zip

配置便携版python
下载解压到python-3.11.9-embed-amd64文件夹
https://www.python.org/ftp/python/3.11.9/python-3.11.9-embed-amd64.zip
编辑 python311._pth，取消注释 `import site`
下载 https://bootstrap.pypa.io/pip/get-pip.py 到python.exe所在文件夹
执行命令: .\python.exe get-pip.py

安装Open WebUI
.\python.exe -m pip install open-webui

执行start.bat
访问 http://127.0.0.1:8080
第一次运行会下载 sentence-transformers/all-MiniLM-L6-v2, 这一步可能需要代理

设置的邮箱: admin@localhost
设置的密码: admin

从这里搜索模型
https://ollama.com/library  
当前整合包下载了这2个模型：
llama3.2:3b
qwen2.5:3b

点击"麦克风"图标选择语音输入，第一次需要下载 WhisperModel, 这一步可能需要代理

设置->界面->语音->运行通话中的打断语音，设置为"开启"
设置->语音->语音播放速度，设置为"1.5x"
```
