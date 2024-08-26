### 1. 卸载旧版本   
以下非官方软件包需要完全卸载：  
* docker.io
* docker-compose
* docker-compose-v2
* docker-doc
* podman-docker 
运行以下命令进行卸载：  
```sh
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
手动删除以下文件夹：
```sh
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```     
### 2. apt 安装
#### 2.1 Set up Docker's `apt` repository.
```sh
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
``` 
**Note:** 如果使用的是`Linux Mint`系统，需要将`VERSION_CODENAME` 替换为 `UBUNTU_CODENAME`   
#### 2.2 安装Docker包
```sh
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
### 3. 卸载docker-ce
#### 3.1 Uninstall the Docker Engine, CLI, containerd, and Docker Compose packages:
```sh
sudo apt-get purge docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin docker-ce-rootless-extras
```
#### 3.2 删除自定义配置文件及文件夹
```sh
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```