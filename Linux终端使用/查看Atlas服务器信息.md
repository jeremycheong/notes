- [1. 查看内核与系统版本](#1-查看内核与系统版本)
- [2. 查看npu信息](#2-查看npu信息)

### 1. 查看内核与系统版本
```sh
uname -a
cat /proc/version
```

### 2. 查看npu信息
必须切换到root用户，在普通用户下即使使用`sudo`也不行。
```sh
npu-smi info
```
