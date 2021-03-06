# README

一个关于 Kustomize 的使用范例。


## 依赖

kubectl > 1.14 版本

[安装kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)


## 快速开始

```
kubectl kustomize | kubectl apply -f -
```


## 概念理解

### kubectl

kubectl是k8s的CLI客户端管理工具

使用kubectl直接执行

```ecma script level 4
kubectl apply -f ./original
```

### kustomize

[kustomize](https://kustomize.io/)是一个k8s配置的模板化工具，他的优点是：

1. 抛弃传统的模板化语言的思路，使用 dict merge的思路来完成多环境的扩展
1. 作者来自Google，与k8s保持非常高的互动
1. 目前已经进入到了kubectl官方的子命令

### 了解k8s

k8s的系统学习难度其实还是挺高的，这需要大量丰富的前置运维研发的基础知识，
但是对于上层的开发者来说，可以重点关注以下几个知识点：

1. 如何撰写deployment
1. 如何仿写一个service
1. 如何仿写一个ingress声明

### 环境隔离

隔离拥有多种策略，具体情况具体分析，客户请自行对照我们的实施方案：

1. 物理环境隔离
1. namespace隔离，这种我们会为客户创建 biz-dev/biz-test 两种namespace 

### 配置撰写

[私密配置撰写](https://kubernetes.io/docs/concepts/configuration/secret/#using-secrets-as-environment-variables)
