Cookie Cadger
============

An auditing tool for Wi-Fi or wired Ethernet connections

[![Build Status](https://travis-ci.org/CookieCadger/CookieCadger.png?branch=master)](https://travis-ci.org/CookieCadger/CookieCadger)
![sullivanmatt](https://komarev.com/ghpvc/?username=sullivanmatt&color=blue&label=Sullivanmatt&style=social)
[![cookiecadger.com](https://img.shields.io/badge/cookiecadger.com-misc-red)](https://cookiecadger.com)
[![GitHub issues](https://img.shields.io/github/issues/sullivanmatt/CookieCadger.svg)](https://github.com/sullivanmatt/CookieCadger/issues)

----------------------------------------------
## Requirements
----------------------------------------------
1. Java 7 8 10
2. The Wireshark Suite (must include the 'tshark' binary)
3. An up-to-date version of Mozilla Firefox
4. Cookie Cadger has optional support for saving data to a MySQL database.  A MySQL installation is required for this feature.

----------------------------------------------
Installation & Operation
----------------------------------------------
1. Download the Cookie Cookie Cadger package from https://cookiecadger.com and extract
2. Run the Cookie Cadger JAR file by double-clicking it, or invoke from command line with java -jar CookieCadger.jar
3. Cookie Cadger's session detection features, if enabled, rely on leaving the automatic update checks enabled.  This allows Cookie Cadger to get newest plugins from the server.
4. If you wish to write your own plugins and use them, create a new directory in the same directory as the Cookie Cadger JAR file called 'plugins' and place them there.   

----------------------------------------------
## Purpose
----------------------------------------------
To see how cookies are used by websites for authentication, and [perform CSRF (Cross-Site Request Forgery)](https://samsclass.info/123/proj14/p11-cookie-cadger.html) attacks.

*Testing Networking
*Finding IP Address
*To make this easiest, set all virtual networks to Bridged mode.

If you don't use [fish](jhome/README.md), you can do something similar in bash:

~~~
#!/bin/bash
jhome () {
  export JAVA_HOME=`/usr/libexec/java_home $@`
  echo "JAVA_HOME:" $JAVA_HOME
  echo "java -version:"
  java -version
}
~~~
[switch.sh](switch.sh)

Then to switch between javas do:
~~~
$> jhome           #switches to latest java
$> jhome -v 1.7    #switches to java 1.7
$> jhome -v 1.6    #switches to java 1.6
~~~

Use jenv is an easy way.

*Install jenv, see [Getting started](https://github.com/jenv/jenv#1-getting-started)
*Config jenv
~~~
cd ~/.jenv/candidates/
mkdir java
cd java
mkdir 1.7
mkdir 1.8
~~~
Symlink the jdk path
~~~
ln -s /Library/Java/JavaVirtualMachines/jdk1.7.0_79.jdk/Contents/Home/bin ~/.jenv/candidates/java/1.7
ln -s /Library/Java/JavaVirtualMachines/jdk1.8.0_45.jdk/Contents/Home/bin ~/.jenv/candidates/java/1.8
~~~
*You are all set

switch command:
~~~
jenv use java 1.8
~~~
set default:
~~~
jenv default java 1.7
~~~

----------------------------------------------
## Downloading Cookie-Cadger
----------------------------------------------
~~~
wget https://www.cookiecadger.com/files/CookieCadger-1.08.jar
~~~

If that link doesn't work, use this command:
~~~
wget https://samsclass.info/123/proj14/CookieCadger-1.08.jar --no-check-certificate
~~~

----------------------------------------------
## Running Cookie Cadger
----------------------------------------------
~~~
java -jar CookieCadger-1.07.jar
~~~

----------------------------------------------
Example Usage & Supported Program Arguments
----------------------------------------------
java -jar CookieCadger.jar
* --tshark=/usr/sbin/tshark
* --headless=on
* --interfacenum=2 (requires --headless=on)
* --detection=on
* --demo=on
* --update=on
* --dbengine=mysql (default is 'sqlite' for local, file-based storage)
* --dbhost=localhost (requires --dbengine=mysql)
* --dbuser=user (requires --dbengine=mysql)
* --dbpass=pass (requires --dbengine=mysql)
* --dbname=cadgerdata (requires --dbengine=mysql)
* --dbrefreshrate=15 (in seconds, requires --dbengine=mysql, requires --headless=off)

----------------------------------------------
Support
----------------------------------------------

Feature requests / bug reports:

[CookieCadger-issues](https://github.com/sullivanmatt/CookieCadger/issues)

General information / anything else:

sullivan.matt@gmail.com

----------------------------------------------
License (FreeBSD)
----------------------------------------------
Copyright (c) 2013, Matthew Sullivan <MattsLifeBytes.com / @MattsLifeBytes>

Additional portions generously contributed by:
* Ben Holland <https://github.com/benjholla>
* Justin Kaufman <akaritakai@gmail.com>

All rights reserved.

 
Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:


1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.


THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE FREEBSD PROJECT OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
