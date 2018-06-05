---
category: news
layout: news
title: " OpenStack "
author: hongs
---

[OpenStack](http://www.openstack.org/) 是实现 IaaS（基础设施即服务）的开源软件，可以让任何组织或个人自行建立和提供云端运算服务，OpenStack 也可用作建立防火墙内的“私有云”（Private Cloud），提供个人或组织内各部门共享资源。OpenStack 系统由几个关键服务组成，它们可以单独安装。这些服务包括计算服务、认证服务、网络服务、镜像服务、块存储服务、对象存储服务、计量服务、编排服务和数据库服务。您可以独立安装这些服务、独自配置它们或者连接成一个整体。安装手册 [OpenStack Installation Tutorial for Red Hat Enterprise Linux and CentOS](http://docs.openstack.org/mitaka/zh_CN/install-guide-rdo/)

#### Centos 7 启用 OpenStack 库
{% highlight ruby %}
# 安装 openstack newton 源
yum install centos-release-openstack-newton
# 修改 CentOS-OpenStack-newton.repo 
vim /etc/yum.repos.d/CentOS-OpenStack-newton.repo
# 将 baseurl 中的 http://mirror.centos.org 修改成 https://mirrors.njcit.cn
baseurl=https://mirrors.njcit.cn/centos/7/cloud/$basearch/openstack-newton/
# 重建 yum cache
yum makecache 

{% endhighlight %}

#### RHEL 
{% highlight ruby %}

yum install https://mirrors.njcit.cn/openstack/rdo-release.rpm

{% endhighlight %}



