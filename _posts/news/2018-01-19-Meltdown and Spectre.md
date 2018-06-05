---
category: news
layout: news
title: " Centos 推出安全升级，修复 Intel 芯片漏洞：Meltdown 和 Spectre "
author: chensong && hongs
---

针对 Intel 的 “Meltdown"（熔断）和 “Spectre” （幽灵）漏洞，Centos 已经推出安全升级。

升级过程：
{% highlight ruby %}
# 更新yum源
yum update -y
# 安装补丁包 microcode_ctl 
yum install microcode_ctl
reboot 

{% endhighlight %}

注：升级后可能会降低系统性能（大概2%-19%的性能损失），请根据个人环境，斟酌升级。

详细见：[Performance Impact of Microcode and Security Patches for CVE-2017-5754 CVE-2017-5715 and CVE-2017-5753 using Red Hat Enterprise Linux](https://access.redhat.com/articles/3311301)

#### CentOS 6：

[Important CentOS 6 microcode_ctl Security Update](https://lists.centos.org/pipermail/centos-announce/2018-January/022700.html)

#### Cenos 7：

[Important CentOS 7 microcode_ctl Security Update](https://lists.centos.org/pipermail/centos-announce/2018-January/022697.html)
