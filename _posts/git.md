---
layout:     post
title:      git cheatsheet
subtitle:   git命令行使用
date:       2020-4-18
author:     BY
header-img: img/post-bg-ios9-web.jpg
catalog: 	 true
tags:
    - git
---


1  go env -w GO111MODULE = on
2  go env -w GO111MODULE=on
3  go env -w GOPROXY=https://goproxy.cn,direct
4  go env
29  git config --global --list
30  git config --system --list
31  git config --list
32  ssh-keygen -t rsa  -C "22842347@qq.com"
33  git clone git@github.com:qianzy96/bmxx.git
38  vi go.mod
39  go mod init github.com/qianzy96/bmxx
40  go get github.com/casbin/casbin
41  go get github.com/facebookgo/inject
42  go get github.com/gin-gonic/gin
43  go get github.com/dgrijalva/jwt-go
44  go get github.com/jinzhu/gorm
46  go get github.com/gin-contrib/sse
47  go get github.com/gin-contrib/pprof
48  go get github.com/lexkong/log
49  go get github.com/go-ini/ini
58  git config --global user.user "qianzy96"
59  git config --global user.email "22842347@qq.com"
72  git remote add origin git@github.com:qianzy96/bmxx.git
73  git commit -m "edit go.mod"
74  git push origin master
76  go get github.com/medivhzhan/weapp/v2
84  git add .
86  git commit -m "add project
87  git push origin master
88  git add .
89  git push origin master
90  git commit -m "edit project"
91  git push origin master
143  git add .gitignore README.md main.go
144  git commit -m  "edit readme.md,gitignore"
145  git push origin master
189  git add go.mod go.sum handler/sd/sd.go main.go router/rouer.go
190  git add go.mod go.sum handler/sd/sd.go main.go router/router.go
191  git status
192  git commit -m "拆分handler"
193  git log
194  git tag v0.2
195  git tag -l
196  git checkout v0.2
197  git push origin master
198  git push origin v0.2