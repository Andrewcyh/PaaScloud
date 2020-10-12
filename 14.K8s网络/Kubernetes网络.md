# Kubernetes网络

## 本章总结

- Kubernetes的网络模型：容器间通信、Pod间通信、Service与Pod间的通信以及集群外部流量与Pod间的通信四种通信
- Kubernetes网络模型通过具备CNI接口外部网络插件来实现，如Flannel、Calico和Canal等
- Flannel支持host-gw、VXLAN和UDP等后端，默认为VXLAN

## 本章介绍

本章节主要介绍Kubernetes网络模型及其实现方式，主流CNI插件如Flannel等。

你可以带着这些问题来学习：

1. 不同业务类型的容器网络访问对于Kubernetes网络会有哪些要求？
2. Kubernetes平台通过什么模型来管理网络？

![image-20201009113352069](./Kubernetes网络.assets/image-20201009113352069.png)

- 描述Kubernetes网络模型及实现方式
- 区别主流CNI插件及相关技术

## Kubernetes网络模型

本小节介绍了Kubernetes网络模型和实现方式

**详细内容要点：**

1. Kubernetes四种网络模型
2. Pod网络的实现方式
3. 虚拟网络接口的实现方式

### Kubernetes的网络模型设计目标

<img src="./Kubernetes网络.assets/image-20201009114039533.png" alt="image-20201009114039533" style="zoom:80%;" />

#### 容器间通信

![image-20201009114127990](./Kubernetes网络.assets/image-20201009114127990.png)

#### Pod间通信

![image-20201009114230079](./Kubernetes网络.assets/image-20201009114230079.png)

##### Pod间通信示意图

![image-20201009115133720](./Kubernetes网络.assets/image-20201009115133720.png)

#### Service与Pod间的通信

<img src="./Kubernetes网络.assets/image-20201009115449214.png" alt="image-20201009115449214"  />

#### 集群外部访问

![image-20201009115804324](./Kubernetes网络.assets/image-20201009115804324.png)

## Pod网络实现方式

![image-20201009134748704](./Kubernetes网络.assets/image-20201009134748704.png)

### 虚拟网络接口的实现方式

![image-20201009134825685](./Kubernetes网络.assets/image-20201009134825685.png)

### 虚拟网络接口实现原理

![image-20201009134914090](./Kubernetes网络.assets/image-20201009134914090.png)

## CNI插件及常见的实现

### 容器网络模型规范CNI

![image-20201009135051685](./Kubernetes网络.assets/image-20201009135051685.png)

### CNI Drivers

![image-20201009135140724](./Kubernetes网络.assets/image-20201009135140724.png)

### 主流CNI插件项目

![image-20201009135240919](./Kubernetes网络.assets/image-20201009135240919.png)

## Flannel网络插件

本小节介绍了Kubernetes网络插件规范CNI和Flannel项目

**详细内容要点：**

1. Kubernetes网络插件规范CNI设计思路
2. CNI的常见项目Flannel，Calico，Canal
3. CNI项目flannel网络模型：Vxlan，host-gw，UDP

### Flannel网络插件

![image-20201009140059565](./Kubernetes网络.assets/image-20201009140059565.png)

### Flannel三种网络模型

![image-20201009140330332](./Kubernetes网络.assets/image-20201009140330332.png)

host-gw的缺点：各个node必须要在同一个网段中

host-gw的优点：不需要像VXLAN一样进行报文封装

### 部署Flannel

![image-20201009141554070](./Kubernetes网络.assets/image-20201009141554070.png)

### 测试Pod连通性

![image-20201009141703256](./Kubernetes网络.assets/image-20201009141703256.png)

### 查看Flannel参数

![image-20201009142636236](./Kubernetes网络.assets/image-20201009142636236.png)

### VXLAN

![image-20201009142727846](./Kubernetes网络.assets/image-20201009142727846.png)

### VXLAN后端和direct routing

<img src="./Kubernetes网络.assets/image-20201009142829244.png" alt="image-20201009142829244"  />

### 启用direct routing

![image-20201009143112737](./Kubernetes网络.assets/image-20201009143112737.png)

### 使配置生效

![image-20201009143206017](./Kubernetes网络.assets/image-20201009143206017.png)

### 网络策略

![image-20201009143324113](./Kubernetes网络.assets/image-20201009143324113.png)

## Kubernetes网络实验演示

本小节演示了Kubernetes网络实验（使用Flannel网络插件实现）

**实验内容：**

1. Node与Pod之间的通信
2. Pod和Pod间通信
3. 使用NodePort的方式实现了集群外访问平台内Pod业务

操作过程中，请注意在验证Pod间通信使用GET方法时，需要手动输入GET。

详见K8s实验手册

