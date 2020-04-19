---
layout:     post
title:      linux cheatsheet
subtitle:   linux命令行使用
date:       2020-4-18
author:     油腻斜杠
header-img: img/post-bg-ios9-web.jpg
catalog: 	 true
tags:
    - linux
---

# system

* uname -a     => display linux system information
* unmae -r     => display kernel release information
* uptime       => show how long the system has been running +load
* hostname     => show system host name
* hostname -r  => display the ip address of the host
* last reboot  => show system reboot history
* date         => show the current date and time
* cal          => show the month calendar
* w            => display whe is online
* whoami       => who you are logged is as
* finger user  => display information about user

# hardware

* dmesg        => detected hardware and boot messages
* cat /proc/cpuinfo => cpu model
* cat /proc/meminfo => memory information
* cat /proc/interrupts => lists the number of interrupts per cpu per i/o device
* lshw         => displays information on hardware configuration of the system
* lsblk        => displays block device related information in linux
* free -m      => used and free memory(-m for mb)
* lspci -tv    =>  show pci device
* lsusb -tv    => show usb devices
* dmidecode    =>  show hardware info form the BIOS
* hdparm -i /dev/sda => show info about disk sda
* hdparm -t /deb/sda => do a read speed test on disk sda
* badblocks -s /dev/sda => test for unreadable block on disk sda

# users

* id           => show the active user id with login and group
* last         => show last logins on the system
* who          => show who is logged on the system
* groupadd admin => add group "admin"
* useradd -c "sam" => g admin -m sam # create user "sam"
* userdel sam  => delete user sam
* adduser sam  => add user "sam"
* usermod      => modify user info

# file commands

* ls -al   => display all information about files/directories
* pwd      => show the path current directory
* rm file-name => delete file
* mkdir directory_name => create a directory
* rm -r directory_name => delete directory
* rm -f file-name   => forcefully remove file
* rm -rf directory-name => forcefully remove directory recursively
* cp file1 file2  => copy file1 to file2
* cp -f dir1 dir2 => cpy dir1 to dir2,create dir2 if doesn't exist
* mv file1 file2  => rename source to dest/move source to directory
* ls -s /path/to/file-name link-name => create symbolic link to file-name
* touch file => create or update file
* cat >file => place  standard input into file
* more file => output contents of file
* head file => output first 10 lines of file
* tail file => output last 10 lines of file
* tail -f file => output contents of file as it grows starting with the last 10 lines
* gpg  -c file => encrypt file
* wc  => print the number of bytes,word,and lines in files
* gpg file.gpg => decrypt file
* xargs => execute command lines from standard input

# process related

* ps    => display you currently active processes
* ps aux | grep 'telnet'  => find all process id related to telnet process
* pmap  => memory map of process
* top  => display all running process
* killpid => kill process with mentioned pid id
* killall proc => kill  all processes named proc
* pkill process-name => send  signal to a process with its name
* bg   => lists stopped or background jobs
* fg   => brings the most recent job to foreground
* fg n => brings job n to the foreground

# file permission related

* chmod octal file-name => change the permissions of file to octal example
* chmod 777 /data/test.c => set rwx permissions for owner,group,world
* chmod 755 /data/test.c => set rwx permissions for owner,rw for group and world
* chown owner-user file => change owner of the file
* chown owner-user:owner-group file-name => change owner and group owner of the file

# network

* ifconfig -a => display all network ports and ip address
* ifconfig eth0 => display specific ethernet port
* ethtool eth0 =>  linux tool to show ethernet status
* mii-tool eth0 => linux tools to show ethernet status
* ping host => send echo request to test connection
* whios domain => get who is information for domain
* dig domain => get DNS information for domain
* dig -x host  => reverse lookup host
* host google.com => lookup DNS ip address for the name
* hostname -i => lookup local ip address
* wget file => download file
* netstat -tupl => list active connections to/from system

# compression/archives

* tar cf home.tar home => create tar named home.tar containing home/
* tar xf file.tar => extract the file from file.tar
* tar czf file.tar.gz file => create a tar with gzip compression
* gzip file => compress file and renames it to file.gz

# install package

* rpm -i pkgname.rpm => install rpm based package
* rpm -e pkgname => remove package

# install from source

* ./configure
* make
* make install

# search

* grep pattern files => search for pattern in files
* grep -r pattern dir => search recursively for pattern in dir
* locate file => find  all instances of file
* find /home/tom  -name 'index' => find files name that start with "index"
* find /home -size +10000k => find files than 10000k in /home

# login(ssh and telnet)

* ssh user@host => connect to host as user
* ssh -p port user@host => connect to host using specific port
* telnet host => connect to the system using telnet port

# file transfer

* scp file.txgt server2:/tmp => secure copy file.txt to remote host /tmp folder
* rsync -a /home/apps /backup => synchronize source to destination

# disk usage

* df -h => show free space on mounted filesystem
* df -i => show free inodes on mounted filesystems
* fdisk -l => show disks partitions sizes and types
* du -ah => display disk usage in human readable form
* du -sh => display total disk usage on the current directory
