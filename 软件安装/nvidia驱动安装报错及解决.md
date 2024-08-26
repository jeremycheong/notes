### 1. 安装Nvidia驱动出现 cc: error: unrecognized command-line option ‘-ftrivial-auto-var-init=zero’
一般为内核版本与显卡驱动版本不匹配，可以选择切换回低版本内核，比如`5.15版本`    
也可以更新`gcc`版本到`gcc-12`
### 2. 删除nvidia驱动
```sh
sudo apt-get purge *nvidia* && sudo apt-get autoremove
```
### 3. 更新gcc并替代方案
```sh
sudo apt-get install gcc-12
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-12 12
```
### 4. 链接`gcc`到`cc`
```sh
sudo ln -sf /usr/bin/gcc /usr/bin/cc
```
### 5. 重新安装驱动
