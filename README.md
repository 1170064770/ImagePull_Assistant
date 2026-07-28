# 镜像文件下载工具
## 📦 将需要下载的容器镜像写入images.txt中就会自动将多架构镜像打包并发布至Release
## 镜像大小问题：
- 如果镜像超过2G即Release限制上限，则会自动切分为以下这种文件：
- multi-arch-images-xxxx.tar.gz.part.aa
- multi-arch-images-xxxx.tar.gz.part.ab
- multi-arch-images-xxxx.tar.gz.part.ac
- 在服务器使用以下命令合并后再使用：
- cat multi-arch-images-xxxx.tar.gz.part.* > multi-arch-images-xxxx.tar.gz
