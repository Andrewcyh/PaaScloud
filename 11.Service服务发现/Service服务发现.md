# Service服务发现

## 本章总结

- Service的基本概念
- 如何使用Service进行服务发现 
- CoreDNS
- Headless Service

## 本章介绍

本章节主要介绍了Kubernetes服务发现相关知识，包括Service的概念与定义，集群内DNS，如何对外暴露服务，什么是headless服务等。

你可以带着这些问题去学习：

1. 如何使用service对象
2. 什么是core-dns
3. 什么是headless服务

<img src=".\Service服务发现.assets\image-20201007223728838.png" alt="image-20201007223728838" style="zoom:80%;" />



主要介绍了Kubernetes服务发现相关知识，包括Service的概念与定义，集群内DNS，如何对外暴露服务，什么是headless服务等

- 使用Kubernetes中Service对象
- 使用core-dns的基本功能
- 使用headless服务

## Service服务发现

### service的功能和模型

**详细内容要点：**

1. Service保证在pod进行变化时，业务都能被访问
2. Kubernetes Service 定义了一种抽象
3. Service模型包括endpoints, endpoint controller, kube-proxy等

#### Service基本概念

##### Pod的特征

![image-20201007232151422](.\Service服务发现.assets\image-20201007232151422.png)

**一种解决方案**

![image-20201007232501543](.\Service服务发现.assets\image-20201007232501543.png)

##### Service

![image-20201007232538944](.\Service服务发现.assets\image-20201007232538944.png)

### 服务发现—Service模型

![image-20201008000252741](.\Service服务发现.assets\image-20201008000252741.png)

#### Endpoint Controller

![image-20201008001707104](.\Service服务发现.assets\image-20201008001707104.png)

#### Kube-proxy iptables

![image-20201008001902744](.\Service服务发现.assets\image-20201008001902744.png)

####  Kube-proxy IPVS

![image-20201008002245477](.\Service服务发现.assets\image-20201008002245477.png)

### Service创建实验

本小节主要讲解了Service创建实验的操作。

**实验内容：**

1. 创建service
2. 对外暴露service服务

详见Service实验手册

### 集群中的DNS

#### CoreDNS

![image-20201008091302156](.\Service服务发现.assets\image-20201008091302156.png)

### Headless Service

![image-20201008101640637](.\Service服务发现.assets\image-20201008101640637.png)

![image-20201008103359586](.\Service服务发现.assets\image-20201008103359586.png)

## 实训任务

步骤 1 创建deployment1，要求：2副本，镜像类型httpd

步骤 2 创建deployment2，要求：3副本，镜像类型httpd

步骤 3 创建service1，service1后端为deployment1和deployment2中所有pod。

步骤 4 创建service2，service2后端为deployment1中的第一个pod和deployment2中的第一个pod。

步骤 5 在clientpod中使用域名访问service2中第一个pod（wget命令）。 

步骤 6 删除本次实验创建的pod，deployment和service，注意！千万不要删除kubernetes服务！

## Service服务发现实训任务演示

步骤1

<img src=".\Service服务发现.assets\image-20201008104859666.png" alt="image-20201008104859666" style="zoom:80%;" />

步骤2

<img src=".\Service服务发现.assets\image-20201008110424653.png" alt="image-20201008110424653" style="zoom:80%;" />

步骤3

<img src=".\Service服务发现.assets\image-20201008135951748.png" alt="image-20201008135951748" style="zoom: 67%;" />

步骤4

<img src=".\Service服务发现.assets\image-20201008144224578.png" alt="image-20201008144224578" style="zoom:67%;" />

步骤5

<img src=".\Service服务发现.assets\image-20201008144457394.png" alt="image-20201008144457394" style="zoom:67%;" />

步骤6

 