# LaraDockCN

LaraDockCN 完全从 [LaraDock](https://github.com/LaraDock/laradock)引用，结合国内[DaoCloud Docker 加速器](http://www.daocloud.io/)，将基于**docker**的**lavarel**开发提速.


![](http://s18.postimg.org/fhykchl09/new_laradock_cover.png)

<br>
## 内容


- [介绍](#Intro)

- [问题](#Help)



<a name="Intro"></a>
## 介绍

LaraDockCN主要是借鉴[LaraDockCN](https://github.com/LaraDock/laradock)引用，结合国内[DaoCloud Docker 加速器](http://www.daocloud.io/)。但在国内由于某种原因导致下载这些镜像速度慢，所以结合国内[DaoCloud Docker 加速器](http://www.daocloud.io/)，将下载提速。

1. 启动docker：```docker-machine start default```
2. **在laradockcn文件夹下**，使用Docker ToolBox下可以使用以下命令进入终端：```docker-machine ssh default``` 
3. 安装加速器：```curl -sSL https://get.daocloud.io/daomonit/install.sh | sh -s d471398ea4f0b6df****05ed633d8931f41f6d37```，参考[加速器](https://dashboard.daocloud.io/mirror).
4. 接下来就可以先把需要的images通过**加速器命令**：```dao pull ubuntu```下载所需的images:
	如：
	- ```dao pull jedisct1/phusion-baseimage-latest:16.04```
	- ```dao pull pacur/debian-jessie:latest```
	- ```dao pull nginx:1```
	- ```dao pull mysql:5.5.49```
	- ```docker pull daocloud.io/library/php:7-fpm```
	- ```dao pull redis:2```
	- ```dao pull jeffprestes/apt-get-updated:latest```
	- ```dao pull mariadb:5```
	- ```dao pull neo4j:2.3```
	- ```dao pull memcached:1.4.26```
5. 最后使用和[LaraDockCN](https://github.com/LaraDock/laradock)一样，只需命令：```docker-compose up -d nginx mysql workspace```
6. 修改apt-get下载源：
  
  ```RUN sed -i 's/http:\/\/archive\.ubuntu\.com\/ubuntu\//http:\/\/cn\.archive\.ubuntu\.com\/ubuntu\//g' /etc/apt/sources.list```



## Help & Questions

有问题，欢迎扫扫微信二维码来拍砖：

![](http://ww2.sinaimg.cn/large/3ce6af96jw1f51tji340rj209d0cggmz.jpg)


## License

[MIT License](https://github.com/laradock/laradock/blob/master/LICENSE) (MIT)
