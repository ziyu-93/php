# Mac ox Nginx

## 安装完成Nginx
>打开nginx
```
sudo nginx
```
网页输入localhost:8080 欢迎界面。

## 修改配置项 nginx.conf
```
vim /usr/local/etc/nginx/nginx.conf

server{
    listen --;
    server_name --;
}
```
## 修改完成后，还需要修改 hosts 文件

```
vi /private/etc/hosts

127.0.0.1  想编辑的地址
```
>如果没有权限修改，右键显示简介修改权限。（读与写）
## 默认打开地址 /usr/local/var/www

```
cd /usr/local/var/www

```

## nginx 支持 php

1、先将 /usr/local/etc/nginx/nginx.conf 中支持php 的那段代码取消注释。

2、然后确定配置内容的正确性(如配置的port与 /usr/local/etc/php/7.0/php-fpm.d/www.conf 文件中的listen是否一致，默认的文件夹是否相同);

3、修改完成后，重新启动nginx 然后访问php文件。

## 编辑文件（显示隐藏文件）
```
defaults write com.apple.finder AppleShowAllFiles -bool true

```

## 隐藏文件
```
defaults write com.apple.finder AppleShowAllFiles -bool false
```

## 修改之后
```
nginx -s stop/reload
```
