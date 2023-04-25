# eMule ed2k下载链接搜索引擎(电影/电视剧)

---
### 简介
* web化的eMule ed2k下载链接搜索引擎(电影/电视剧), 用Go开发。从eMule KAD网络搜索下载链接。 用户的搜索输入首先会经过豆瓣或者时光网的验证, 然后才发给eMule KAD网络查找。
* 如果你不想搜索链接被过滤，可以独立使用KAD搜索引擎. 可以参考**main.go**和**web/web.go** 里的代码。
* 完整emule客户端，支持搜索、下载 https://github.com/chenjia404/emule_helper

---
### 如何编译
- 这个项目是在Windows上的VS code开发，所以你也可以用VS code编译它。
- 对于Linux，比如Ubuntu(64bit)， 你可以用下面的命令编译它
    * set GOARCH=amd64
    * set GOOS=linux
    * go mod tidy
    * go build


---
### 如何运行
- 本地(比如Windows)
    * 运行hahajing.exe
    * 打开浏览器访问[localhost:2021](localhost:2021),输入关键词等待搜索结果
    * 使用迅雷等软件进行下载
- 服务器(比如Ubuntu)
    * nohup hahajing server &
    * 打开浏览器访问服务器
-- docker
```bash
   docker run -it -p 127.0.0.1:8080:80 chenjia404/hahajing
```

- 文件说明
    * config/kad/nodes.dat 可以使用emule里面的同名文件
    * config/web/home.html 前端页面，可以自己修改
- **注意**: 可执行文件一定要跟**config**目录在同一个目录夹下。

---

### 打包

goreleaser release --skip-publish --rm-dist

### 运行图示
![home](./doc/home.png)
![result](./doc/result.png)

---
### 协议
MIT
