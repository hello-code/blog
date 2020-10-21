---
title: "Go Cross Compile"
date: 2020-10-17T09:12:40+08:00
draft: false
---

## ubuntu 20.04
`sudo apt-get install gcc-mingw-w64`

### 32bit
```
env CGO_ENABLED=1 GOOS=windows GOARCH=386 CC=i686-w64-mingw32-gcc go build -o main.exe -ldflags="-H windowsgui"
```

### 64bit
```
env CGO_ENABLED=1 GOOS=windows GOARCH=amd64 CC=x86_64-w64-mingw32-gcc go build -o main.exe -ldflags="-H windowsgui"
```