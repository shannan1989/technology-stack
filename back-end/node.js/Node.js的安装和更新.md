## 官网下载

Node.js 各平台下载地址（含npm）： https://nodejs.org/en/download/

npm 官网： https://www.npmjs.com/get-npm

## 查看版本和更新

查看 node 和 npm 版本
```
    node -v

    npm -v
```

更新 node

推荐使用 n 模块，该模块专门用来管理node.js的版本。

```
    # 安装
    npm install -g n

    # 使用
    n stable
    n latest
    n v9.2.0
```

**注意：n 模块不支持Windows系统！**

Windows系统 去官方下载最新版 Node.js 覆盖安装即可。

更新 npm

```
    npm install -g npm@latest
```

## 安装淘宝镜像

安装淘宝镜像的包命令行管理工具cnpm
```
    npm install -g cnpm --registry=http://registry.npm.taobao.org
```
