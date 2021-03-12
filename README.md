---
description: BoxJs 是一款运行在 Surge、QuanX、Loon 环境下的脚本！
---

# 介绍

## 安装

### Surge

{% code title="Surge Module" %}
```bash
# 安装路径: 
 ​ 首页 > 模块 > 安装新模块

# BoxJs 稳定版
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.sgmodule

# BoxJs 测试版
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.tf.sgmodule

```
{% endcode %}

### QuanX

{% code title="QuanX Rewrite" %}
```bash
# 安装路径: 
 ​ 风车 > 重写 > 引用

# BoxJs 稳定版
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.conf

# BoxJs 测试版
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.tf.conf

```
{% endcode %}

### Loon

{% code title="Loon Plugin" %}
```bash
# 安装路径: 
 ​ 配置 > 插件 > 插件
 
# BoxJs 稳定版
 ​ https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.loon.plugin

# BoxJs 测试版
  https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.loon.tf.plugin

```
{% endcode %}

### Shadowrocket

{% code title="Shadowrocket Rewrite" %}
```bash
# 安装路径
  配置 > 点击使用中的配置文件 > 编辑纯文本
  
# 在 [Script] 标签下增加以下内容，如果没有 [Script]，可自行增加
  
# BoxJs 稳定版
  Rewrite: BoxJs = type=http-request,pattern=^https?://boxjs.com,script-path=https://raw.githubusercontent.com/chavyleung/scripts/master/chavy.box.js, requires-body=true, timeout=120

# BoxJs 测试版
  Rewrite: BoxJs = type=http-request,pattern=^https?://boxjs.net,script-path=https://raw.githubusercontent.com/chavyleung/scripts/master/box/chavy.boxjs.js, requires-body=true, timeout=120

```
{% endcode %}

{% hint style="warning" %}
 安装完成后，请重启一次代理 
{% endhint %}

## 访问

商店版: [http://boxjs.com](http://boxjs.com)

测试版: [http://boxjs.net](http://boxjs.net)

