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


*   go env -w GO111MODULE = on
*   go env -w GO111MODULE=on
*   go env -w GOPROXY=https://goproxy.cn,direct
*   go env
*   git config --global --list
*  git config --system --list
*  git config --list
*  ssh-keygen -t rsa  -C "22842347@qq.com"
*  git clone git@github.com:qianzy96/bmxx.git
*  vi go.mod
*  go mod init github.com/qianzy96/bmxx
*  go get github.com/casbin/casbin
*  go get github.com/facebookgo/inject
*  go get github.com/gin-gonic/gin
*  go get github.com/dgrijalva/jwt-go
*  go get github.com/jinzhu/gorm
*  go get github.com/gin-contrib/sse
*  go get github.com/gin-contrib/pprof
*  go get github.com/lexkong/log
*  go get github.com/go-ini/ini
*  git config --global user.user "qianzy96"
*  git config --global user.email "22842347@qq.com"
*  git remote add origin git@github.com:qianzy96/bmxx.git
*  git commit -m "edit go.mod"
*  git push origin master
*  go get github.com/medivhzhan/weapp/v2
*  git add .
*  git commit -m "add project
*  git push origin master
*  git add .
*  git push origin master
*  git commit -m "edit project"
*  git push origin master
*  git add .gitignore README.md main.go
*  git commit -m  "edit readme.md,gitignore"
*  git push origin master
*  git add go.mod go.sum handler/sd/sd.go main.go router/rouer.go
*  git add go.mod go.sum handler/sd/sd.go main.go router/router.go
*  git status
*  git commit -m "拆分handler"
*  git log
*  git tag v0.2
*  git tag -l
*  git checkout v0.2
*  git push origin master
*  git push origin v0.2
*  git rm _posts/ -r