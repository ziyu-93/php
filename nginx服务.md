# Mac Nginx

## 安装完成Nginx
>打开nginx
```
sudo nginx
```
网页输入localhost:8080 欢迎界面。

## 修改配置项 nginx.conf
```
vi /usr/local/etc/nginx/nginx.conf

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
