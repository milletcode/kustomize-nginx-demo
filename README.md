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