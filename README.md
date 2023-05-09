# An eMule ed2k link search engine for Movie/TV

[中文版](./README_CN.md)

---
### Introduction
* This is web based eMule ed2k link search engine for Movie/TV, developed by Go. It searches file link from eMule KAD network. User search input will be firstly validated via DouBan or MTime, and then send eMule KAD network for searching. Results will be classcified and then display on browser.
* KAD search egnine is independent in case you don't want file links to be filtered. It's easy to use it without dependency. Check **main.go** and **web/web.go** to see how to use it.
* Currently, the web page is displayed in Chinese, but it's easy to guess how to use it.
* full emule Client，Support search and download https://github.com/chenjia404/emule_helper

---
### How to build
- It's developed with VS code on Windows. So you can open project by VS code and build it.
- For Linux, e.g. on Ubuntu(64bit), you can use below commands to build it
    * go build -trimpath -ldflags="-w -s"

---
### How to run
- Local side(e.g. Windows)
    * Run hahajing.exe (here web server is started at **localhost:2021**)
    * Open browser to visit [localhost:2021](localhost:2021)
- Server side(e.g. Ubuntu)
    * nohup hahajing server &
    * Open browser to visit the server

- docker side
```bash
   docker run --it -p 127.0.0.1:8080:80 chenjia404/hahajing
```
    
- **Note**: Make sure executable file is at same directory with **config** directory.

---

### releaser

goreleaser release --skip-publish --rm-dist

### What it looks like
![home](./doc/home.png)
![result](./doc/result.png)

---
### License
MIT
