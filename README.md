# laravel-package-yuntongxun

v0.1
# laravel-package-yuntongxun

本模块是基于laravel5.6，php7开发测试，简化云通讯短信接口调用。php5.6应该可用。


安装
cmposer require shangning/yuntongxun

添加  service provider
文件位置config/app.php
Shangning\Yuntongxun\YuntongxunServiceProvider::class,

'Yuntongxun' => Shangning\Yuntongxun\Facades\Yuntongxun::class,

发布
php artisan vendor:publish --provide=Shangning\Yuntongxun\YuntongxunServiceProvider

自动将拷贝配置文件至/config/yuntongxun.php，修改配置。

使用方法
$response = Yuntongxun::sms($phone,$datas,$tempId);
$response是调用返回值
