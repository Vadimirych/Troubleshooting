# Kali - package installation issues

## Problem

```
┌──(root㉿kali)-[~]
└─# sudo gobuster dir -u 192.168.215.52 -w /usr/share/wordlists/dirb/common.txt -t 5
sudo: gobuster: command not found
                                                                                                                    
┌──(root㉿kali)-[~]
└─# apt-get install gobuster
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package gobuster
```

## Solution

```
apt-get update & apt-get install gobuster
```


