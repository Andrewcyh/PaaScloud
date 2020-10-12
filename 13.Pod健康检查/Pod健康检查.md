# Pod健康检查

## 本章总结

介绍了两种探针：就绪探针和存活探针的使用方式和特性

## 本章介绍

本章节主要介绍了Kubernetes中如何使用探针进行Pod健康检查。

你可以带着这些问题去学习：

1. 探针是如何检测健康状态的？
2. 存活探针和就绪探针有什么区别？

<img src=".\Pod健康检查.assets\image-20201009080044691.png" alt="image-20201009080044691" style="zoom:67%;" />

- 掌握存活探针的概念和使用方式
- 掌握就绪探针的概念和使用方式

## Pod健康检查

本小节主要讲解了Pod探针基本概念用途。

**详细内容要点：**

1. 精准判断Pod状态的方式
2. Readiness探针和Liveness探针是两种常用探针
3. Kubelet会反馈检查结果

### Pod探针基本概念

#### Pod状态

![image-20201009080522804](.\Pod健康检查.assets\image-20201009080522804.png)

#### 更准确的判断Pod状态

![image-20201009080639806](.\Pod健康检查.assets\image-20201009080639806.png)

#### 容器探针

![image-20201009093717614](.\Pod健康检查.assets\image-20201009093717614.png)

#### 检查结果

![image-20201009095119855](.\Pod健康检查.assets\image-20201009095119855.png)

### 使用存活探针

#### **ExecAction**

![image-20201009100204657](.\Pod健康检查.assets\image-20201009100204657.png)

TCP类型存活探针和HTTP类型存活探针实验操作。

**实验内容：**

1. 创建使用HTTP类型存活探针的Pod。
2. 创建使用TCP类型存活探针的Pod。

#### HTTP

![image-20201009102724538](.\Pod健康检查.assets\image-20201009102724538.png)

#### TCP

![image-20201009103147716](.\Pod健康检查.assets\image-20201009103147716.png)

### 使用就绪探针

#### 就绪探针

![image-20201009104352574](.\Pod健康检查.assets\image-20201009104352574.png)

#### 存活探针和就绪探针对比

![image-20201009104609740](.\Pod健康检查.assets\image-20201009104609740.png)

#### ExecAction

![image-20201009105123878](.\Pod健康检查.assets\image-20201009105123878.png)



## 实训任务

步骤 1    创建一个http服务（包括deployment和service），deployment中包含3副本。

步骤 2    使用就绪探针和存活探针，存活探针使用execaction模式，就绪探针使用http模式。

1. httpd镜像提供的服务默认路径为/,默认端口为80

## 健康检查实训任务演示

步骤1

<img src=".\Pod健康检查.assets\image-20201009111517442.png" alt="image-20201009111517442" style="zoom:80%;" />

<img src=".\Pod健康检查.assets\image-20201009111537732.png" alt="image-20201009111537732" style="zoom:80%;" />

步骤2

<img src=".\Pod健康检查.assets\image-20201009112523217.png" alt="image-20201009112523217" style="zoom:80%;" />