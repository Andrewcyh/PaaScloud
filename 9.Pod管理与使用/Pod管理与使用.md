# Pod管理与使用

## 本章总结

## 本章介绍

本章节主要讲述Pod的概念，如何使用Pod，如何编写Yaml格式文件，如何使用不同类型的Pod等。

你可以带着这些问题去学习：

1. 如何区分单容器Pod和多容器Pod
2. 如何区分运行常驻任务的Pod和运行一次性任务的Pod

<img src=".\Pod管理与使用.assets\image-20201005190534611.png" alt="image-20201005190534611" style="zoom:67%;" />

- 描述Pod特性
- 区分单容器Pod和多容器Pod
- 区分运行常驻任务的Pod和运行一次性任务的Pod

## Pod管理与使用

本小节主要讲解了Pod的理论知识。

**详细内容要点：**

1. Pod是Kubernetes管理的最小基础单元
2. Pod有只包含一个应用容器的pod和包含多个应用的pod
3.  一个pod中会分配一个pause容器，这也被称为根容器

### Pod的概念

![image-20201005221226502](.\Pod管理与使用.assets\image-20201005221226502.png)

###  Pod的两种模式

![image-20201005222456267](.\Pod管理与使用.assets\image-20201005222456267.png)

### Pod内部结构

![image-20201005225624667](.\Pod管理与使用.assets\image-20201005225624667.png)

### Pod生命周期

![image-20201005225733326](.\Pod管理与使用.assets\image-20201005225733326.png)

##  Pod实验

本小节主要讲解了Pod实验的操作。

**实验内容：**

1. 使用Yaml文件创建Pod	
2. 使用explain命令
3. 运行一次性的Pod

详见Pod实验手册

## 实训任务

- 步骤 1    创建一个Pod，包含两个容器。

  - 容器1为busybox进行
  - 容器2为httpd镜像

- 步骤 2    进入busybox容器命令行界面。在home目录下使用如下命令写入一个文件

  ```shell
  ]# cat > test.txt << EOF
  > i am busybox
  > EOF
  ```

## Pod管理与使用实训任务演示

步骤一

![image-20201006200129082](.\Pod管理与使用.assets\image-20201006200129082-1601985694368.png)

步骤二

![image-20201006200414580](.\Pod管理与使用.assets\image-20201006200414580.png)