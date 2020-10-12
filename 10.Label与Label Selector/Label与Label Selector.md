# Label与Label Selector

## 本章总结

- 标签的定义与使用
- 标签选择器的定义与使用

## 本章介绍

本章节主要讲述标签和标签选择器相关知识，包括定义、如何使用标签和标签选择器，不同类型的标签选择器等。

你可以带着这些问题去学习：

1. 如何使用标签标注Kubernetes对象？
2. 如何使用标签选择器筛选kubernetes对象？

![image-20201006200645971](.\Label与Label Selector.assets\image-20201006200645971.png)

- 使用标签标注Kubernetes对象
- 使用标签选择器筛选Kubernetes对象
- 区别不同类型的标签选择器

## Label与Label Selector

这节课主要讲解了标签相关知识：

**详细内容要点：**

1. 标签（Label）是附在kubernetes对象（如pod，deployment等）上的键值对（key-value）
2. 标签由一组键值对构成
3. 通过标签选择器，用户或客户端可以指定批量的对象进行操作

### Label

![image-20201006202740569](.\Label与Label Selector.assets\image-20201006202740569.png)

### 动机

![image-20201006202955295](.\Label与Label Selector.assets\image-20201006202955295.png)

### 标签的语法

![image-20201006210016990](.\Label与Label Selector.assets\image-20201006210016990.png)

###  Label实验

![image-20201007202158588](.\Label与Label Selector.assets\image-20201007202158588.png)

![image-20201007202320767](.\Label与Label Selector.assets\image-20201007202320767.png)

![image-20201007202402728](.\Label与Label Selector.assets\image-20201007202402728.png)

### 标签选择器Labels Selector

![image-20201007202507229](.\Label与Label Selector.assets\image-20201007202507229.png)

#### 基于等值的标签选择器

![image-20201007202637180](.\Label与Label Selector.assets\image-20201007202637180.png)

`-L`指的是显示键的值

![image-20201007202953130](.\Label与Label Selector.assets\image-20201007202953130.png)

![image-20201007203315703](.\Label与Label Selector.assets\image-20201007203315703.png)

![image-20201007205233315](.\Label与Label Selector.assets\image-20201007205233315.png)

#### 基于集合的标签选择器

![image-20201007205308601](.\Label与Label Selector.assets\image-20201007205308601.png)

##### 实验

![image-20201007205923956](.\Label与Label Selector.assets\image-20201007205923956.png)

