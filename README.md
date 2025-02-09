# OOW

本项目不再更新，可使用Ollama + Cherry Studio  
Ollama官网: https://ollama.com/  
Cherry Studio官网: https://cherry-ai.com/  

---
Ollama + Open WebUI, 配置成便携版的，解压即可使用。  

Ollama官网: https://ollama.com/  
Open WebUI官网: https://openwebui.com/  


## 下载
Release限制 2 GB，压缩包比较大，只能放网盘了。  
下载后可自行校验压缩包哈希值。  

### OOW_20241219.7z
```r
Ollama v0.5.4
Open WebUI v0.4.8
内置模型:
  llama3.2:3b
  qwen2.5:3b
链接: https://pan.quark.cn/s/ef24475cac55
提取码: xr8K
大小: 4.98 GB
sha256: 7f6bc3dfd297a44db3c21b93f576fa0293e4c239157533720c98d02c893d1c9d
```

### OOW_20241110.7z
```r
内置模型:
  llama3.2:3b
  qwen2.5:3b
链接: https://pan.quark.cn/s/c9aaf0ad7854
提取码: TB6E
大小: 4.96 GB
sha256: 7d527edd7e3feecd9acf99a5155fb86509d61895a841e4dfbaafc00c1434efbd
```

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


## 升级
### Ollama
删除或重命名 ollama-windows-amd64 文件夹  
https://github.com/ollama/ollama/releases 下载最新的ollama-windows-amd64.zip解压即可

### Open WebUI
到python.exe所在文件夹，执行命令：  
```r
.\python.exe -m pip install --upgrade open-webui
```


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
