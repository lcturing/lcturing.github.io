##海外域名申请与github pages应用实践

1. 选择一个域名提供商。选择一个稳定知名的服务商以购买域名比较重要，比如[GoDaddy](http://www.godaddy.com/)。个人认为，域名提供商类似一个域名控制端，具备了向域名服务器分发增删域名的权限。一般来说，域名服务商本身就提供类似一条龙的服务，域名注册、域名服务器、网络空间、网络服务器服务，当然也可以选择别的DNS服务器，比如为了稳定期间，采用[DNSPod](https://www.dnspod.cn)等国内的DNS，在域名提供商设定好DNS服务器后即可。
2. 设置DNS服务器。这里分为两种情况，如果你的网站部署在你租用的，具有公网IP的服务器上，则直接设置A记录，将域名指向你的IP；如果你的网站部署在VPS这种空间提供商，也许提供商会给你提供一个searver域名，则可以在CNAME中配置域名到server域名的映射。对于github而言，参考了阮一峰的日志中提供的IP直接设置了A记录即可。如果需要第三方DNS服务商，则在NS部分配置相关的name server地址。
3. github pages设置cname。这里的cname就是github pages仓库的根目录下新建CNAME文件，中间写入自己的域名即可。这里的作用就是告诉github以我的域名访问时该找到哪个具体的username.gihub.io。

以上三步基本可以建立一个以github pages服务为核心的静态博客网站了。


> Written with [StackEdit](https://stackedit.io/).