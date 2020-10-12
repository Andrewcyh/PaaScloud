# Kubernetes Dashboard

## 本章总结

- Dashboard是什么
- Dashboard的两种认证方式：token和Kubeconfig
- Dashboard的界面架构和各个界面内容
- Dashboard的功能：增删改查
- 如何使用Dashboard部署应用

## 本章介绍

本章主要介绍Kubernetes Dashboard界面结构和功能，并通过Dashboard部署应用。

你可以带着这些问题来学习：

1. Kubernetes Dashboard能提供哪些功能？
2. 如何通过Dashboard部署应用？
3. Dashboard相对于命令行的优势是什么？

![image-20201011120525666](./Kubernetes Dashboard.assets/image-20201011120525666.png)

- 作为Kubernetes的Web用户界面，用户可以通过Dashboard在Kubernetes集群中部署容器化的应用，对应用进行问题处理和管理，并对集群本身进行管理
- 通过Dashboard，用户可以查看集群中应用的运行情况，同时也能够创建或修改Kubernetes的资源
- 通过部署向导，用户能够对部署的应用进行扩缩容、滚动更新、重启Pod，也可以部署新的应用
- 当然，通过Dashboard也能够查看Kubernetes资源的状态

目标

- 描述Dashboard的功能
- 区分Dashboard不同的认证方式
- 熟悉Dashboard界面结构
- 熟练使用Dashboard管理Kubernetes集群
- 熟练使用Dashboard部署应用

## Kubernetes Dashboard

本小节介绍了Kubernetes Dashboard的界面结构和相关功能，并通过Dashboard部署应用。

**详细内容要点：**

1. Dashboard界面布局和结构
2. Dashboard增删改查的各项功能
3. Dashboard部署应用的方式和参数解析

### Dashboard介绍

#### Dashboard是什么

![image-20201011121940183](./Kubernetes Dashboard.assets/image-20201011121940183.png)

#### Dashboard认证 

![image-20201011123011832](./Kubernetes Dashboard.assets/image-20201011123011832.png)

#### Dashboard界面结构

![image-20201011123128728](./Kubernetes Dashboard.assets/image-20201011123128728.png)

##### Cluster

![image-20201011123252340](./Kubernetes Dashboard.assets/image-20201011123252340.png)

![image-20201011123304939](./Kubernetes Dashboard.assets/image-20201011123304939.png)

![image-20201011123319187](./Kubernetes Dashboard.assets/image-20201011123319187.png)

##### Namespace

![image-20201011123407357](./Kubernetes Dashboard.assets/image-20201011123407357.png)

**Overview**

![image-20201011123435768](./Kubernetes Dashboard.assets/image-20201011123435768.png)

**Workloads**

![image-20201011124048130](./Kubernetes Dashboard.assets/image-20201011124048130.png)

![image-20201011124104771](./Kubernetes Dashboard.assets/image-20201011124104771.png)

**Discovery and Load Balancing**

![image-20201011124831311](./Kubernetes Dashboard.assets/image-20201011124831311.png)

**Config and Storage**

![image-20201011124928528](./Kubernetes Dashboard.assets/image-20201011124928528.png)

### Dashboard功能

#### 增加

![image-20201011125005562](./Kubernetes Dashboard.assets/image-20201011125005562.png)

#### 删除

![image-20201011125046556](./Kubernetes Dashboard.assets/image-20201011125046556.png)

#### 修改

![image-20201011125108851](./Kubernetes Dashboard.assets/image-20201011125108851.png)

![image-20201011125125792](./Kubernetes Dashboard.assets/image-20201011125125792.png)

#### 查找

![image-20201011125216621](./Kubernetes Dashboard.assets/image-20201011125216621.png)

![image-20201011125254021](./Kubernetes Dashboard.assets/image-20201011125254021.png)

![image-20201011125317258](./Kubernetes Dashboard.assets/image-20201011125317258.png)

### Dashboard部署应用

![image-20201011125411268](./Kubernetes Dashboard.assets/image-20201011125411268.png)

**高级选项**

![image-20201011131625581](./Kubernetes Dashboard.assets/image-20201011131625581.png)



## Kubernetes实验演示

本小节主要演示使用Kubernetes Dashboard创建应用的几种方法：

**实验内容：**

1. CREATE AN APP
2. CREATE FROM TEXT INPUT
3. CREATE FROM FILE

详见k8s Dashboard实验手册