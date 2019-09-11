
一般我们通过 npm 命令来实现 package 的安装、删除和更新。

## 安装

```sh
# 安装但不写入package.json
$ npm install xxx

# 安装并写入package.json的"dependencies"中
$ npm install xxx –S 

# 安装并写入package.json的"devDependencies"中
$ npm install xxx –D

# 全局安装
$ npm install xxx -g

# 安装特定版本
$ npm install xxx@1.0.0
```
Tips:
- -S（等同于--save）表示正式打包时该依赖包会一并打包；
- -D（等同于--save-dev）表示该依赖包仅在开发环境下使用，正式打包时不会加到项目中。

## 删除

```sh
# 删除模块
$ npm uninstall xxx

# 删除全局模块
$ npm uninstall xxx -g
```

## 更新

列出可以更新的package：
```sh
$ npm outdated
```

### 更新某一个package

如果只需要更新某一个package，可使用如下命令：
```sh
# 可根据package的作用范围在后面加上 -D、-S 或 -g
$ npm update xxx
```
该更新命令只能按照 package.json 中标注的版本号进行更新，所以更新前记得先修改 package.json 中该package的版本号。

### 更新所有package

首先得更新 package.json 文件，可以使用 npm-check-updates 模块：

```sh
# 安装 npm-check-updates 模块
$ npm install -g npm-check-updates

# 检查可更新的模块
$ ncu
# 或
$ npm-check-updates

# 更新package.json的各模块版本号到最新
$ ncu -u
```

package.json 更新后，为了保险起见，可删除整个 node_modules 目录后，重新初始化项目。

Tips：
不建议一次性全部更新所有package，根据实际需求更新即可。全部更新有可能导致项目不稳定，甚至运行不起来，正式项目以稳定合适为优先。
