Git - SSL unable to get local issuer certificate
------------------------------------------------

## Solution
```
git config --global http.sslbackend schannel
```