# Homebrew

macOS（或 Linux）缺失的软件包管理器

能让你更快速地安装想要的工具，而不用考虑大量的依赖。

官网：https://brew.sh

## 安装 Homebrew
在终端执行
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## 使用 Homebrew

### 搜索
```sh
brew search mysql
```

### 查看
查看软件包信息（当前版本、注意事项等）及依赖关系
```sh
brew info mysql
```

### 访问软件包主页
```
brew home mysql
```

### 安装
```sh
brew install mysql
```

### 卸载
```sh
brew uninstall mysql
```

### 更新 Homebrew
在把软件包更新到最新版本之前，需要先把 brew 更新到最新版本
```sh
brew update
```

### 检查新版本
```sh
#列出所有有更新的软件包
brew outdated
```

### 升级
```sh
#升级所有软件包
brew upgrade
#升级指定的软件包
brew upgrade mysql
```

### 清理
清理不需要的软件包旧版本及其安装缓存
```sh
brew cleanup 
```

### 查看通过 brew 安装的系统服务，如nginx
```
brew services list
```

### 清除已卸载的无用的启动配置文件
```
brew services cleanup
```

### 重启服务，如nginx
```
brew services restart nginx
```

### 更多命令详见
```
man brew
```
