# Kubernetes资源调度

## 本章总结

- 主要介绍了Kubernetes的资源调度机制，包括：
  - Kubernetes资源管理和Eviction机制
    - Hard模式和Soft模式
  - Kubernetes默认调度器scheduler
    - 节点预选、节点优选、节点选定
  - Kubernetes常用调度策略
  - Kubernetes调度优先级和抢占机制

## 本章介绍

本章主要介绍Kubernetes的资源管理，Kubernetes调度机制和常用调度策略，调度优先级和抢占机制。

你可以带着这些问题来学习：

1. 被Eviction驱逐的Pod是否还会再被拉起来？
2. Kubernetes调度的过程是怎样的？
3. Kubernetes调度失败后，会怎么处理？
4. Eviction和优先级的区别是什么？

![image-20201011012912582](./Kubernetes资源调度.assets/image-20201011012912582.png)

- Kubernetes资源管理和Eviction
- 描述Kubernetes资源调度过程
- 列举常用的Kubernetes资源调度策略
- 描述Kubernetes调度优先级和抢占机制

## Kubernetes资源管理

本小节介绍了Kubernetes资源管理和Eviction机制。

**详细内容要点：**

1. Kubernetes资源管理关键信息和capacity数据获取途径
2. Eviction的作用和触发阈值
3. Eviction的两种模式
4. Eviction驱逐Pod的规则

### 节点资源

![image-20201011013258894](./Kubernetes资源调度.assets/image-20201011013258894.png)

### capacity

![image-20201011013442236](./Kubernetes资源调度.assets/image-20201011013442236.png)

### Eviction

![image-20201011013550720](./Kubernetes资源调度.assets/image-20201011013550720.png)

![image-20201011013648403](./Kubernetes资源调度.assets/image-20201011013648403.png)

![image-20201011013818576](./Kubernetes资源调度.assets/image-20201011013818576.png)

![image-20201011013859295](./Kubernetes资源调度.assets/image-20201011013859295.png)

## Kubernetes调度

本小节介绍了Kubernetes调度过程及Kubernetes的优先级和抢占机制。

**详细内容要点：**

1. Kubernetes调度器和调度过程中的3个阶段
2. Kubernetes调度过程中的常用策略
3. Kubernetes调度的优先级和抢占机制，及其应用场景

### Kubernetes调度器

![image-20201011102722691](./Kubernetes资源调度.assets/image-20201011102722691.png)

![image-20201011103947026](./Kubernetes资源调度.assets/image-20201011103947026.png)

### Kubernetes调度策略

#### Predicates预选策略

![image-20201011104152438](./Kubernetes资源调度.assets/image-20201011104152438.png)

##### Predicates常用策略

![image-20201011104318714](./Kubernetes资源调度.assets/image-20201011104318714.png)

#### Priorities优选策略

![image-20201011104508085](./Kubernetes资源调度.assets/image-20201011104508085.png)

##### Priorities常用策略

![image-20201011104651667](./Kubernetes资源调度.assets/image-20201011104651667.png)

### Kubernetes调度优先级和抢占机制

![image-20201011113554571](./Kubernetes资源调度.assets/image-20201011113554571.png)

#### PriorityClass

![image-20201011113820605](./Kubernetes资源调度.assets/image-20201011113820605.png)

![image-20201011113918984](./Kubernetes资源调度.assets/image-20201011113918984.png)

![image-20201011113955772](./Kubernetes资源调度.assets/image-20201011113955772.png)

