# docker介绍以及基础指令

## 什么是docker

Docker是一个开源的应用容器引擎，它基于go语言开发，并遵从Apache2.0开源协议。使用Docker可以让开发者封装他们的应用以及依赖包到一个可移植的容器中，然后发布到任意的Linux机器上，也可以实现虚拟化。Docker容器完全使用沙箱机制，相互之间不会有任何接口，这保证了容器之间的安全性。

Docker诞生于2013年初，目前有两个版本，Community Edition（CE，社区版）和Enterprise Edition（EE，企业版）。其中Docker社区版是免费开源的，对于个人和小团队来说是比较理想的选择；Docker企业版则是收费的，是专门为企业和大型IT团队提供的，用于要求比较严格的商业应用中。

## docker的特点

1．更快速的交付和部署

开发者可以使用一个标准的Docker镜像来构建一套开发容器，开发完成之后，运维人员可以直接使用这个容器来部署代码。Docker可以快速创建容器以及快速迭代应用程序，并让整个过程全程可见，使团队中的其他成员更容易理解应用程序是如何创建和工作的。Docker容器轻，且启动速度快，可以大量地节约开发、测试和部署的时间。

2．更高效的虚拟化

Docker容器在运行时，不需要额外的虚拟机程序的支持。由于它是内核级的虚拟化，所以可以实现更高的性能和效率。

3．更轻松的迁移和扩展

Docker容器几乎可以在任意的平台上运行，包括物理机、虚拟机、公有云、私有云、个人电脑和服务器等。这种良好的兼容性可以让用户把一个应用程序从一个平台直接迁移到另外一个平台，十分有利于应用的迁移和扩展。

4．更简单的管理

使用Docker，只需要小小的修改，就可以替代以往大量的更新工作。所有的修改都以增量的方式被分发和更新，从而实现自动化并且高效的管理。

## 相关基础指令

### 启动docker

```jsx
systemctl start docker
```

### 关闭docker

```jsx
systemctl stop docker
```

### 重启docker

```jsx
systemctl restart docker
```

### 查看docker运行状态

```jsx
systemctl status docker
```

查看docker版本号信息

```jsx
docker version
docker info
```

### docker帮助命令

用于忘记了某些命令可以进行查看与回顾

```jsx
docker --help
```

### 查看自己服务器中docke镜像列表

```jsx
docker images
```

### 列出运行中的容器

```jsx
docker ps #列出运行中的容器
docker ps -a  #查看所有容器，包括未运行
```

### 停止容器

```jsx
docker stop 容器id或name
docker kill 容器id：强制停止容器
```

### 删除容器

```jsx
docker rm 容器id或name：删除已停止的容器
docker rm -f 容器id：删除正在运行的容器
```