## Linux Basics

## basic Linux Commands

`info [OPTION]... [MENU-ITEM...]`

    infocommand reads documentation in the info format. It will give detailed information for a command when compared with the man page. The pages are made using the texinfo tools because of which it can link with other pages, create menus and easy navigation.

`df`

    report file system disk space usage
![](2020-10-05-12-36-05.png)

`du`
    
    estimate file space usage
    show how much space is utilized by a folder / file passed as argument


![](2020-10-05-12-41-41.png)

why difference ??

![](2020-10-05-12-42-35.png)

## [env](https://en.wikipedia.org/wiki/Env)

    Run a program in modefied environment or view environment variables

`env`
![](2020-10-05-12-55-15.png)

![](2020-10-05-13-01-42.png)


`export`

    set env variables 

![](2020-10-05-13-02-59.png)


[Shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)) `#!`

`#!/usr/bin/env python3`

    refers to the python3 variable name in environment variables

`netstat`

![](2020-10-05-13-17-48.png)

`top` 

    displays processes

`htop`

    interactive process viewer    

`free`

    displays memory details 
![](2020-10-05-13-22-33.png)    

`/etc` - Usually contain the configuration files for all the programs that run on your Linux/Unix system.

[swap](https://www.cyberciti.biz/faq/linux-check-swap-usage-command/)

`swapon` or `swapoff` 


[less](https://linuxize.com/post/less-command-in-linux/)

    less > more

[Vim Cheatsheet](https://devhints.io/vim)
    
    vi starts vim in ubuntu by default

[umask](https://www.computerhope.com/unix/uumask.htm#:~:text=On%20Linux%20and%20other%20Unix,show%20you%20its%20current%20value.)
![](umask.png)


[Telnet vs SSH](https://study-ccna.com/telnet-ssh/)
    
    tenet - not secure - port 23
    ssh - secure public key encryption   - port 22



`truncate`

    shrink or exppand a file for specific size

files greater than specific size

`find . -size +10k -ls`


NAT vs Proxy

    These two technologies differ in their positions in the TCP/IP protocol stack. NAT works at the network layer while proxy at the application layer. NAT is transparent to various applications, whereas proxy must resort to the IP address of the proxy server specified in application programs. For example, to access a web page by using NAT, no configuration is required in the browser. To access a web page by using a proxy, you must specify the IP address of the proxy in the browser. If the proxy supports only HTTP, only web servers can be accessed through the proxy, but not FTP. In terms of Internet access, NAT delivers higher scalability than proxy, because NAT is not targeted at applications.

[How to Copy Files From a Remote System (ftp)](https://docs.oracle.com/cd/E19253-01/816-4555/remotehowtoaccess-87541/index.html)
    
    oracle docs

`scp [OPTION] [user@]SRC_HOST:]file1 [user@]DEST_HOST:]file2`


`sed` [stream editor](https://www.gnu.org/software/sed/manual/sed.html#Common-Commands)

[examples](https://www.geeksforgeeks.org/sed-command-in-linux-unix-with-examples/)

![](2020-10-05-15-53-07.png)

![](scommand.png)

[find](https://en.wikipedia.org/wiki/Find_(Unix)) 

    The related locate programs use a database of indexed files obtained through find (updated at regular intervals, typically by cron job) to provide a faster method of searching the entire file system for files by name.

`find ./GFG -name sample.txt -exec rm -i {} \;`

    {} means "the output of find". As in, "whatever find found". find returns the path of the file you're looking for, right? So {} replaces it; it's a placeholder for each file that the find command locates

    The \; part is basically telling find "okay, I'm done with the command I wanted to execute".


### [Symbolic Links](https://en.wikipedia.org/wiki/Symbolic_link)

To create a symbolic Link

`ln -s target_path link_path`



### [Cron](https://en.wikipedia.org/wiki/Cron)

    Job Scheduler

**Need Explore **
--- 

[Xargs](https://en.wikipedia.org/wiki/Xargs)
    
    Extended Arguments

[xargs examples](https://www.geeksforgeeks.org/xargs-command-unix/)



`awk`

    The basic function of awk is to search files for lines (or other units of text) that contain certain patterns. When a line matches one of the patterns, awk performs specified actions on that line. awk continues to process input lines in this way until it reaches the end of the input files.
[awk examples](https://www.geeksforgeeks.org/awk-command-unixlinux-examples/)


## **Set Vs Export**

    set is limited to current session
    export 

    export sets attribute value for a environment variable



archive - muliple files to single

tar - cvf c compress verbose f fillename x extract
z single enc technique 
tar -tgf g - gzip 
tar -tgf j - bzip2 -- more speed less compression

tar -x to unzip

tar.gz 
tar.bz2

-r folder


---



Create folder tree in single command
    
`mkdir -p /home/sub1/sub2`

`rm -r /home/sub1/sub2`

`cp -r  <source-folder-tree> <destination>`


`curl <link of the file> -O`

-O to save the file, else it just prints out

`wget <link_to_file> -O "filename"`

Check OS Version

`ls /etc/*release*`

`cat etc/*release*`
 
Cent OS package manager
RPM - RedHat Package Manager

![](2020-10-01-13-31-56.png)

RPM does not install the dependency pakages, it just installs the \<package_name>.rpm file.

YUM is a High Level Package manager that overcomes this problem.

`yum install <package-name>`

yum uses rpm to install packages

repo info is stored at `/etc/yum.repos.d`