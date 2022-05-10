---
description: BoxJs 是一款运行在 Surge、QuanX、Loon、Shadowrocket、Stash 环境下的脚本！
---

# 介绍

## 安装

### Surge

{% code title="Surge Module" %}
```bash
# 安装路径: 
 ​ 首页 > 模块 > 安装新模块

# 模块地址: 
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.sgmodule
```
{% endcode %}

### QuanX

{% tabs %}
{% tab title="Rewrite (简单)" %}
#### 一键安装

> 如果你使用的是 **v1.0.29 (670)** 及以上版本，你可以直接复制以下链接并在 [`Safari`](quantumult-x:///add-resource?remote-resource=%7B%22rewrite_remote%22%3A%5B%22https%3A%2F%2Fgithub.com%2Fchavyleung%2Fscripts%2Fraw%2Fmaster%2Fbox%2Frewrite%2Fboxjs.rewrite.quanx.conf%2Ctag%3Dboxjs%22%5D%7D) 中打开

```
quantumult-x:///add-resource?remote-resource=%7B%22rewrite_remote%22%3A%5B%22https%3A%2F%2Fgithub.com%2Fchavyleung%2Fscripts%2Fraw%2Fmaster%2Fbox%2Frewrite%2Fboxjs.rewrite.quanx.conf%2Ctag%3Dboxjs%22%5D%7D
```



#### 手动安装

{% code title="QuanX Rewrite" %}
```bash
# 安装路径: 
 ​ 风车 > 重写 > 引用

# 重写路径: 
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.conf
  
```
{% endcode %}
{% endtab %}

{% tab title="HTTP Backend" %}
HTTP Backend 需要通过 IP+端口 的形式访问

如果你觉得这样不够优雅，可参考 \`Rewrite + HTTP Backend (进阶)\` 实现域名访问

{% code title="HTTP Backend" %}
```bash
# 安装路径: 
 ​ 风车 > 工具&分析> HTTP Backend > 添加

# 标签: boxjs
# 处理请求的路径: ^/

# 脚本路径
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/chavy.boxjs.js

# 访问地址:
  http://127.0.0.1:9999

# 注意事项
  注意配置 HTTP Backend 的地址为 0.0.0.0 端口为 9999
  配置完成后确保打开了 HTTP Backend 的开关
  然后 全部更新 > 重启代理
```
{% endcode %}
{% endtab %}

{% tab title="Rewrite + HTTP Backend (进阶)" %}
```bash
# 第一步
同时配置 HTTP Backend 和 Rewrite 
全部更新 > 重启代理
配置后应该通过 http://127.0.0.1:9999 访问下页面后是否正常

# 第二步
# http://boxjs.com
# http://boxjs.net 
# http://127.0.0.1:9999
进入 BoxJs > 应用(底栏) > 内置应用 > 偏好设置

# 第三步
在 `HTTP Backend (Quantumult X)` 中填入 HTTP Backend 的地址
如: http://127.0.0.1:9999

# 然后就可以通过`域名`的方式访问 BoxJs 了

# 原理
通过 Rewrite 可以实现域名的形式访问 BoxJs
通过 偏好设置 可以让 BoxJs 的数据请求走 HTTP Backend

# 感谢 https://github.com/chouchoui PR
# 详见 https://github.com/chavyleung/scripts/pull/327
```
{% endtab %}
{% endtabs %}

### Loon

如果你使用的是 **v2.1.19 (385)** 及以上的版本，你可以直接: [一键安装](loon://import?plugin=https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.loon.plugin)

{% code title="Loon Plugin" %}
```bash
# 安装路径: 
 ​ 配置 > 插件 > 插件
 
# 插件地址: 
 ​ https//raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.loon.plugin
```
{% endcode %}

### Shadowrocket

{% tabs %}
{% tab title="Module (推荐)" %}
{% code title="Shadowrocket Module" %}
```bash
# 安装路径: 
 ​ 配置 > 模块 > 右上角加号

# 模块地址: 
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.sgmodule

# 感谢
  @JOJOforshaun PR
```
{% endcode %}
{% endtab %}

{% tab title="Rewrite" %}
{% code title="Shadowrocket Rewrite" %}
```bash
# 安装路径:
  配置 > 点击使用中的配置文件 > 编辑纯文本
  
# 在 [Script] 标签下增加以下内容，如果没有 [Script]，可自行增加

# 重写地址:
  Rewrite: BoxJs = type=http-request,pattern=https?:\/\/boxjs\.(com|net),script-path=https://raw.githubusercontent.com/chavyleung/scripts/master/box/chavy.boxjs.js, requires-body=true, timeout=120
  
```
{% endcode %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
安装完成后，最好重启一次代理
{% endhint %}

### Stash

{% code title="Stash stoverride" %}
```bash
# 安装路径: 
  首页 > 覆写 > 安装覆写
  
​# 覆写地址: 
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.stash.stoverride
```
{% endcode %}

## 访问

1. [http://boxjs.com](http://boxjs.com)
2. [http://boxjs.net](http://boxjs.net)
