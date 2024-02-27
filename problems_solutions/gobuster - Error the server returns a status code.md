# Gobuster - The server returns a status code that matches the provided options for non existing urls

## Problem
The server returns a status code that matches the provided options for non existing urls.
https://acf51fdf1ef3226bc0c107b5001d0039.web-security-academy.net/5a5ad98b-471c-4dee-a868-dbf7b56088d5 => 302 (Length: 0). To continue please exclude the status code

## Solution
We need to exclude length of 0.
Example: 
```
gobuster dir -u http://offsecwp -w /usr/share/wordlists/dirb/big.txt -p pattern -t 5 --exclude-length 0 
```