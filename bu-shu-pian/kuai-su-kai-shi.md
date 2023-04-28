# 快速开始

## 安装前的准备

* docker

因为是使用容器化一键部署，所以你需要提前安装好docker软件。

## 开始安装

1. 运行命令

```sh
docker run -idt  -p 80:80 --name bkrepo  bkrepo/bkrepo
```

2. 配置host

默认域名是bkrepo.example.com，配置DNS或者hosts文件，使域名指向你的服务器ip。

3. 访问bk-repo

启动需要一点时间，等待一分钟左右，访问http://bkrepo.example.com，即可登录。

## 指定域名

上面的是默认域名启动，你也可以配置自己的域名。

添加相关环境变量：

* BK\_REPO\_HOST：bk-repo域名
* BK\_REPO\_DOCKER\_HOST：docker  registry 域名

```sh
docker run -idt  -p 80:80 --name bkrepo -e BK_REPO_HOST="bkrepo.com" -e BK_REPO_DOCKER_HOST="docker.bkrepo.com" bkrepo/bkrepo
```

## 开启制品扫描功能

## 持久化部署
