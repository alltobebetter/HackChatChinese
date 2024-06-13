# 开发环境

1. [克隆](https://help.github.com/articles/cloning-a-repository/)仓库。
    * 终端命令：`git clone https://github.com/hack-chat/main.git hackchat`
2. 在终端中进入目录。
    * 终端命令：`cd hackchat`
3. 使用npm安装。
    * 终端命令：`npm install`
4. 启动应用程序。
    * 终端命令：`npm start`

# 实时部署安装

1. (按上述步骤1 - 3操作)
2. 使用PM2启动后端服务器。
    * 终端命令：`pm2 start ./server/main.js --node-args="-r esm" --name hackchat`
    * 参见下方提示，使服务器在启动时自动启动。
3. 将`./hackchat/client`的内容迁移到您的Web服务器的任何适当目录。HackChat附带了`http-server`，仅用于开发目的，强烈建议您使用更好的Web服务器，如Nginx或Apache。
4. (可选) 清理；您可以删除`hackchat/clientSource`和`hackchat/documentation`。

# 提示

* 如果您打算使用SSL提供客户端服务，则需要使用**反向代理**，因为hack.chat服务器软件不原生支持TLS（这可能会在将来的版本中更改）。
* **不要使用root用户。** 在使用root帐户安装或以root权限安装时，将导致类似以下错误的错误：
`npm WARN lifecycle hack.chat-v2@2.1.92~postinstall: cannot run in wd hack.chat-v2@2.1.91 cd ./clientSource && npm install && cd .. & cd ./server && npm install && npm run config (wd='/dir')`
* 可以配置PM2在启动时启动后端服务器，请阅读[https://pm2.keymetrics.io/docs/usage/startup/](https://pm2.keymetrics.io/docs/usage/startup/)
* **不要使用** `sudo apt install nodejs` **安装NodeJS**，而应使用以下命令：
   ```bash
   cd ~
   curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh
   sudo bash nodesource_setup.sh
   sudo apt install nodejs
   ```
* 快速设置脚本，在Ubuntu 18上测试通过。
  * `cd ~`
  * `nano ./hc_install.sh`
  * 粘贴：
    ```bash
    #!/bin/bash
    cd ~
    sudo apt update
    sudo apt install build-essential git
    curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh
    sudo bash nodesource_setup.sh
    sudo apt install nodejs
    nodejs -v
    npm -v
    git --version
    git clone https://github.com/hack-chat/main.git hackchat
    cd hackchat
    npm install
    ```
  * `Ctrl + x`
  * `Y`
  * `chmod u+x ./hc_install.sh`
  * `./hc_install.sh`
