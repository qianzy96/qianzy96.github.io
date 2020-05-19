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

    1  yum install -y wget
    2  history
    3  yum install -y node
    4  yum install node
    5  node
    6  yum install go
    7  yum install golang
    8  cd /
    9  ls
   10  cd usr
   11  ls
   12  wget https://npm.taobao.org/mirrors/node/v14.2.0/node-v14.2.0-linux-x64.tar.xz
   13  ls
   14  wget https://studygolang.com/dl/golang/go1.14.1.windows-amd64.zip
   15  ls
   16  uname -r
   17  yum update
   18  yum remove docker docker-common docker-selinux docker-engine
   19  yum install -y yum-utils device-mapper-persistent-data lvm2
   20  yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
   21  yum list docker-ce --showduplicates | sort -r
   22  yum install docker-ce
   23  systemctl start docker
   24  systemctl enable docker
   25  docker version
   26  git version
   27  java version
   28  java
   29  java -version
   30  uname -a
   31  ls
   32  tar -xvf node-v14.2.0-linux-x64.tar.xz
   34  mv node-v14.2.0-linux-x64 nodejs
   40  wget https://studygolang.com/dl/golang/go1.14.1.linux-amd64.tar.gz
   42  tar -xvf go1.14.1.linux-amd64.tar.gz
   54  source /etc/profile
   55  ls -s /usr/nodejs/bin/node /usr/local/bin/
   56  ls -s /usr/nodejs/bin/npm /usr/local/bin/
   57  source /etc/profile
   58  node -v
   59  npm -v
   60  vi /etc/profile
   61  source /etc/profile
   62  go env
   63  source /etc/profile
   64  vi /etc/profile
   65  source /etc/profile
       export NODE_HOME=/usr/nodejs
       export PATH=$NODE_HOME/bin:$PATH

       export GOROOT=/usr/go
       export GOPATH=/home/go
       export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
       export GOPROXY=https://goproxy.io,direct
   67  cd /home
   68  mkdir go
   69  cd /usr
   71  vi /etc/profile
   72  source /etc/profile
   73  go env
   78  wget -O /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo
   79  yum update
   80  yum install ntfs-3g
   99  wget https://www.jetbrains.com/go/download/#section=linux
   100 cd /usr/shar/applications
   101 toch goland.desktop
   102 vi goland.desktop
       
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


