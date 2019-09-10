# Redis
### 安装redis
```
$ yum install redis
```

### 启动redis
```
$ service redis start
```
### 停止redis
```
$ service redis stop
```
### 查看redis运行状态
```
$ service redis status
```
### 查看redis进程
```
$ ps -ef | grep redis
```

### 设置redis为开机启动
```
$ chkconfig redis on
```

### 进入redis服务
```
$ redis-cli
```
### 列出所有key
```
$ keys *
```

# 安装PHP的Redis扩展
```
$ cd /tmp
$ wget http://pecl.php.net/get/redis-3.1.6.tgz
$ tar -zxvf redis-3.1.6.tgz
$ rm -rf ./redis-3.1.6.tgz
$ cd ./redis-3.1.6
$ yum install php-devel
$ phpize
$ ./configure
$ make && make install
```
