Camel - a soft load balance midware
================

![logo](https://raw.githubusercontent.com/leonindy/camel/master/camel-admin/src/main/webapp/assets/images/camel_logo_blue.png)

[Camel](https://github.com/leonindy/camel) 是大众点评开发的软负载一体解决方案，承担了F5硬负载层后的软负载工作。Camel已成为大众点评网络流量中必不可缺的一层。

文档请见[Camel in Action](http://leonindy.coding.me/camel/)

![whole_picture](https://raw.githubusercontent.com/leonindy/camel/master/camel-admin/src/main/webapp/assets/images/whole_picture.png)

Camel在大众点评的应用规模如下：

1. nginx服务器集群：

  **18**个nginx集群，共**161**台nginx服务器

2. 站点及业务集群：

  **356**个站点域名，**857**个业务服务器集群

3. QPS：

  每天响应约**1.5**万次接口调用，其中有约**3000**次为nginx配置部署请求


Camel项目由`camel-admin`, `Dengine`\(基于Tengine开发的Web服务器\), `camel-agent`三个模块组成：
![component](https://raw.githubusercontent.com/leonindy/camel/master/camel-admin/src/main/webapp/assets/images/component.png)

1. `camel-admin`:

  Camel管理端：可以通过接口及页面两种方式对Nginx集群进行发布、重启、监控等操作。

2. `Dengine`:

  大众点评基于Tengine开发的Web服务器。在Tengine的基础上，添加了降级等功能。

3. `camel-agent`:

  部署在Nginx服务器上，管理本机的Nginx进程与配置文件。