# racoon

小浣熊，一个基于Express和genpac封装的工具

## 特性
* 根据默认配置和用户配置生成PAC文件
* 搭建一个本地Web服务器，用于提供PAC的网页浏览

## 要求
* Python with pip
* Nodejs

## 使用
### 基本使用 － 使用PAC
1.启动
```
cd racoon && npm start
```

2.获取PAC本地网址
```
http://localhost:3001/proxy.pac
```

3.配置PAC
![配置PAC](https://static.dingtalk.com/media/lALOjUKAU80Cds0FLg_1326_630.png)

### 高级使用 － 生成PAC
1.安装genpac
```
# 安装
$ pip install genpac
# 或从github安装开发版本
$ pip install https://github.com/JinnLynn/genpac/archive/master.zip   
# 更新
$ pip install --upgrade genpac
# 或从github更新开发版本
$ pip install --upgrade https://github.com/JinnLynn/genpac/archive/master.zip
# 卸载
$ pip uninstall genpac
```
2.编辑自定义规则
在项目目录genpac下，编辑两个规则文件user-rules-direct 和 user-rules-proxy，前者是指定不走代理的网址，后者是指定走代理的网址。

3.生成pac文件
```
./gen.sh
```
生成的proxy.pac文件在public目录下。

## 感谢
1. [JinnLynn/genpac](https://github.com/JinnLynn/genpac)
1. [expressjs](http://expressjs.com)

## 参考
1. [MAC平台PAC文件编写和自动代理配置](http://openwares.net/internet/mac平台pac文件编写和自动代理配置.html)
1. [Mac上shadowsocks使用pac代理给手机iOS安卓](http://www.akmumu.com/2015/07/07/367.html)
1. [使用 Pow 和 Privoxy 绕开 OS X 的沙盒限制和 SOCKS5 兼容问题](http://chrisyip.github.io/post/use-pow-and-privoxy-bypass-mac-sandbox-and-socks5-issue/)
1. [用代理自动配置文件pac给iphone和ipad设备添加socks代理](http://zhiwei.li/text/2015/08/16/用代理自动配置文件pac给iphone和ipad设备添加socks代理/)
1. [node.js express - mime type woff font returned as text/plain type](http://stackoverflow.com/q/20439783)

## License
```
Copyright (C) 2016 snowdream <yanghui1986527@gmail.com>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
