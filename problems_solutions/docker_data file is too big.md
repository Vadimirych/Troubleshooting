docker_data.vhdx file is too big
==========================================

## Problem
C:\Users\myuser\AppData\Local\Docker\wsl\disk\docker_data.vhdx file is too big


## Solution
1. Clean up docker data first
```
docker system prune -a --volumes
```
2. Shutdown Docker Desktop completely
3. WSL2 must be shut down
```
wsl --shutdown
```
4. Backup the file
5. Under admin shell run the following command to compact the VHDX file
```
Optimize-VHD -Path "C:\Users\myuser\AppData\Local\Docker\wsl\disk\docker_data.vhdx" -Mode Full
```
