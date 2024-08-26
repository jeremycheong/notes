### 使用`apt`安装
1. 配置公共知识库
   ```sh
    curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
    && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
    sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
    sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
   ```
   可选择将版本库配置为使用实验软件包:
   ```sh
   sed -i -e '/experimental/ s/^#//g' /etc/apt/sources.list.d/nvidia-container-toolkit.list
   ```
2. 更新软件包列表
   ```sh
   sudo apt-get update
   ```
3. 安装套件
   ```sh
   sudo apt-get install -y nvidia-container-toolkit
   ```