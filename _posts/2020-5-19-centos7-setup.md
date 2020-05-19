---
layout:     post
title:      centos7 setup
subtitle:   centos7 setup
date:       2020-4-18
author:     油腻斜杠
header-img: img/post-bg-ios9-web.jpg
catalog:         true
tags:
    - centos7 go node goland
---

   *  cd usr
   *  wget https://npm.taobao.org/mirrors/node/v14.2.0/node-v14.2.0-linux-x64.tar.xz
   *  uname -r
   *  yum update
   *  yum remove docker docker-common docker-selinux docker-engine
   *  yum install -y yum-utils device-mapper-persistent-data lvm2
   *  yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
   *  yum list docker-ce --showduplicates | sort -r
   *  yum install docker-ce
   *  systemctl start docker
   *  systemctl enable docker
   *  docker version
   *  git version
   *  java version
   *  tar -xvf node-v14.2.0-linux-x64.tar.xz
   *  mv node-v14.2.0-linux-x64 nodejs
   *  wget https://studygolang.com/dl/golang/go1.14.1.linux-amd64.tar.gz
   *  tar -xvf go1.14.1.linux-amd64.tar.gz
   *  source /etc/profile
   *  ln -s /usr/nodejs/bin/node /usr/local/bin/
   *  ln -s /usr/nodejs/bin/npm /usr/local/bin/
   *  source /etc/profile
   *  node -v
   *  npm -v
   *  go env

   ```
    export NODE_HOME=/usr/nodejs
    export PATH=$NODE_HOME/bin:$PATH
    
    export GOROOT=/usr/go
    export GOPATH=/home/go
    export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
    export GOPROXY=https://goproxy.io,direct
   ```

   *  wget -O /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo
   *  yum update
   *  yum install ntfs-3g
   *  wget https://www.jetbrains.com/go/download/#section=linux
   *  cd /usr/shar/applications
   *  toch goland.desktop
   *  vi goland.desktop

   ```    
    [Desktop Entry]
    Version = 1.0
    Type = Application
    Name = Goland
    IcON = /usr/goland/bin/goland.png
    Exec = "/usr/goland/bin/goland.sh" %f
    Comment = The Drive to Develop
    Categories = Devlopment;IDE;
    Terminal = false
    StartupWMClass = jetbrains-goland
   ```

