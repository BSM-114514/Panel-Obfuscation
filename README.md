# BPB-Code-Obfuscation

一个用于混淆BPB代码的项目

------

## 关于本项目

##### 本项目的目的

------

本项目是将[BPB-Worker-Panel]((github.com/bia-pain-bache/BPB-Worker-Panel))项目中的“worker.js”代码进行混淆，以通过Cloudflare的审查。

##### 为什么会有这个项目？

------

还不是因为Cloudflare！

由于很多人在Cloudflare Workers/Pages中使用了BPB项目搭建了可以上外网的代理节点（相当于VPN，但和VPN有着本质上的区别，区别将在后文提到），导致Cloudflare认为这不符合使用Workers/Pages来搭建网页的目的（当然也有可能是会影响他们的WARP的用户，因为两者的用途很相似），于是Cloudflare更新了用户政策并封杀了相关的Workers/Pages（被封杀后相关网页会显示1101错误，同时代理工具会无法连接或测试延迟时会提示超时）。为了应对Cloudflare的行为，BPB的作者便对成品worker.js代码进行混淆，以通过Cloudflare的审查，但很多人直接使用BPB作者发布的worker.js来部署，导致Cloudflare发现后进行了封禁。不过，只要将BPB的worker.js代码混淆成一个全新的代码，并且这个代码只能自己使用，那Cloudflare就不会封你的BPB节点了，这也便是本项目的由来之一了。

OK，讲了这么多，那我们来看看如何在Cloudflare上部署BPB项目吧！

## 部署BPB项目

> [!NOTE]
>
> 懒得写了……以后再写了
>
> 教程请看https://www.haoyep.com/posts/cf-bpb-vpn/

