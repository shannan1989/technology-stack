在macOS终端下执行如下命令时：
```
brew install xxx
```
结果报如下错：
```
Error: Another active Homebrew update process is already in progress.
Please wait for it to finish or terminate it to continue.
```
解决方法：
```
rm -rf /usr/local/var/homebrew/locks
```
