# hack.chat

[hack.chat](https://hack.chat/) 是一个极简、无干扰、无需账户、无日志记录、消息自动消失的聊天服务，可以轻松部署为您自己的服务。当前的客户端集成了由[KaTeX](https://github.com/Khan/KaTeX)提供的LaTeX渲染和由[highlight.js](https://github.com/isagalaev/highlight.js)提供的代码语法高亮功能。

您可以在[第三方软件列表](https://github.com/hack-chat/3rd-party-software-list)仓库中找到为hack.chat框架开发的软件列表，包括机器人、客户端、Docker容器等。

这是对[Andrew Belt](https://github.com/AndrewBelt/hack.chat)工作的向后兼容延续。服务器代码已更新为ES6，新增了多项功能，包括新命令和命令/协议的热重载。还提供[文档](documentation/index.html)。

# 安装

## 先决条件

- [node.js v16.14.0](https://nodejs.org/) 或更高版本
- [npm 8.5.4](https://nodejs.org/) 或更高版本

## 开发者安装

1. [克隆](https://help.github.com/articles/cloning-a-repository/)仓库：`git clone https://github.com/hack-chat/main.git`
2. 切换到目录：`cd main`
3. 安装依赖项：`npm install`
4. 启动：`npm start`

## 实时部署安装

参见[DEPLOY.md](documentation/DEPLOY.md)

# 贡献

- 使用两个空格进行缩进。
- 使用驼峰命名法命名文件。

# 鸣谢

* [**Marzavec**](https://github.com/marzavec) - *初始工作*
* [**MinusGix**](https://github.com/MinusGix) - *基础更新*
* [**Neel Kamath**](https://github.com/neelkamath) - *基础文档*
* [**Carlos Villavicencio**](https://github.com/po5i) - *语法高亮集成*
* [**OpSimple**](https://github.com/OpSimple) - *新增模块：dumb.js & speak.js*
* [**Andrew Belt**](https://github.com/AndrewBelt)，原始基础工作
* [**SuLin**](https://github.com/alltobebetter)，汉化工作
* [**wwandrew**](https://github.com/wwandrew)，发现服务器缺陷（包括攻击向量）并提交~~___非常详细___~~的错误报告
* [**其他所有人**](https://github.com/hack-chat/main/graphs/contributors)参与了这个项目。

# 许可证

该项目在[MIT许可证](LICENSE)下许可。
