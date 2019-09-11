#### PHP Warning: ob_start(): output handler 'ob_gzhandler' conflicts with 'zlib output compression'

以上警告的解决办法：

在执行
```php
ob_start('ob_gzhandler');
```
之前加上一句
```php
ob_end_clean();
```
即可解决。
