# MXNet: 一个对于复杂分布式系统的灵活有效的机器学习库

## 前言

MXNet 是一个容易开发机器学习算法，尤其是深度神经网络，的多语言的机器学习库。嵌入主语言，用命令张亮计算混合声明符号表达。它提供自动求导来获得剃度。MXNet是计算和内存有效的，运行在各种复杂系统之上，从手机设备到分布式GPU集群。

这篇文章描述了MXNet的API设计和系统执行，并且解释了怎样用一种独特的方式来解决来嵌入符号表达和张量操作。我们起初的实验在使用多GPU机器的大规深度神经网络应用中取得可喜的成果。

## 介绍

机器学习算法的规模和复杂性正变得越来越大。几乎所有最近的ImageNet挑战获胜者使用非常深层次的神经网络，需要数十亿的浮点操作来处理一个单独的样本。结构和计算复杂性的提升对机器学习系统设计和执行产生了挑战。

大部分机器学习系统把领域专用语言（DSL）嵌入到一个主语言中（例如，Python，Lua，C＋＋）。