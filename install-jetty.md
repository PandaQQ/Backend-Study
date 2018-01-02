# Install Jetty 9 on Ubuntu 16.04 as Jetty provides http server

#### A bit More About Jetty 9:
- Jetty is a fantastic open source Java HTTP web server & Java Servlet Container.
- Jetty is not only free for personal use but can also be used for commercial purpose.
- Jetty was initially developed as an open source project that later joined hands with the team of Eclipse.
- It can serve content from web server and application and now is often used for machine to machine communication in larger software framework.
  

#### Here are pre-requisites for Installing Jetty 9:
To install Jetty 9 on ubuntu 16.04, we need following two things:
- An Ubuntu 16.04 server with sudo (You can always use sudo, in both case"($,#)"users.) as Jetty needs Java to run.
- And Oracle JDK 8 instead of OpenJDK in this tutorial.
  
  
#### Step 1: Installing JDK 8
- Before starting with the installation..we have to ensure that our existing system is up to date with the latest packages.

``` bash
 $ sudo apt-get update
 $ sudo apt-get upgrade
```

- You are now running on the latest version of Ubuntu.
- then We are installing JDK 8 by using WebUpd8 team PPA Repository.
- We are using here WebUpd8 Repos which is consist of a script, which will automatically download and install JAVA 8.
- Run the following command:

``` bash

$ sudo apt-get install software-properties-common
 
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
python3-pycurl python3-software-properties unattended-    upgrades
Suggested packages:
libcurl4-gnutls-dev python3-pycurl-dbg bsd-mailx mail-    transport-agent
The following NEW packages will be installed:
python3-pycurl python3-software-properties software-  properties-common 
unattended-upgrades
0 upgraded, 4 newly installed, 0 to remove and 3 not upgraded.
Need to get 102 kB of archives.
After this operation, 800 kB of additional disk space will be used.
Do you want to continue? [Y/n]
  
  
$ sudo add-apt-repository ppa:webupd8team/java

Press [ENTER] to continue or ctrl-c to cancel adding it OK

$ sudo apt-get update
$ sudo apt-get -y install oracle-java8-installer
$ sudo java -version
java version "1.8.0_45"
Java(TM) SE Runtime Environment (build 1.8.0_45-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.45-b02, mixed mode)
```
> - Here in output, we are able to see the java version:
> - Java Version "1.8.0_45"
> - Perfect! You have completed Step 1 correctly..
> - ..let's move to Step 2 now.


#### Step 2: Install Jetty 9

- Run the following command in order to install Jetty 9 on your Ubuntu machine.
``` bash
sudo apt-get update
sudo apt-get install jetty9
```

#### Step 3: 

