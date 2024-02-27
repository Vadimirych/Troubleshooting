# Kali - wine32 is required

## Problem 

wine32 is required to run i386 windows executable from Kali

## Solution:
1. Edit sources 
```
vim /etc/apt/sources.list
```
2. Add 
```
deb-src http://http.kali.org/kali kali-rolling main contrib non-free
```
3. Install wine32

```
sudo apt-get update
sudo apt-get install wine32
```

4. Recreate wine configuration

```
sudo rm -r /root/.wine
winecfg
```
