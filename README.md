### 脚本用途
在用科学上网的时候，我们经常会发现一个问题：明明已经科学上网了，但是为什么手机上的Google Play Store依然不能正常连接，只有手机设置为全局上网的时候才可以登陆Play Store (从服务器检索信息时出错。[DF-DFERH-01])。根本原因其实在于，国行手机里即使预装了Google的服务套件，其中的services.googleapis.com被修改为service.googleapis.cn，这个域名指向的是国内的IP，你当然不可以借此登陆到Play Store上啦。那怎么做可以让services.googleapis.cn指向真实的services.googleapis.com的IP呢？你可能会想到，修改DNS！是的，但是还有一个问题，google的服务器IP是经常会变动的，总不能每天去更新吧？这时候，shell script就派上用场了

本文是基于smartdns作为dnsmasq上游NDNS时，对smartdns的配置文件进行更改。如果只有dnsmasq，请参考类似方法，修改dnsmasq的配置文件
