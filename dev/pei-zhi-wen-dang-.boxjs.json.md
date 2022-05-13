---
description: 本文介绍如何配置 BoxJs 订阅文件
---

# 配置文档 (\*.boxjs.json)

## &#x20;​全量配置

待完善

## 场景介绍 <a href="#scenes" id="scenes"></a>





### 安装事件 (onInstall) <a href="#scenes-oninstall" id="scenes-oninstall"></a>

如果希望用户在添加 BoxJs 后，自动安装重写 (.plugin, .snippet, ...)

{% hint style="info" %}
要求:&#x20;

BoxJs: v0.12.0

Loon: v2.1.19 (386)

Quantumult X: v1.0.29 (670)
{% endhint %}



**实现原理**

根据配置，用户在添加订阅后会打开一个指定的 URL，你可以配置一个 URL Scheme 或一个普通 URL，来实现自动安装重写、更新资源……，如：

```
loon://update?sub=all
```

**配置方式**

```json
{
  "id": "chavyleung.app.test.sub",
  ....
  "onInstall": {
    "title": "安装确认",
    "message": "本订阅包含重写资源, 是否需要自动安装?",
    "install": {
      "Surge": "",
      "QuanX": "quantumult-x:///add-resource?remote-resource=%7B%22rewrite_remote%22%3A%5B%22https%3A%2F%2Fgithub.com%2Fchavyleung%2Fscripts%2Fraw%2Fmaster%2Fbox%2Frewrite%2Fboxjs.rewrite.quanx.conf%2Ctag%3Dboxjs%22%5D%7D",
      "Loon": "loon://import?plugin=https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.loon.plugin",
      "Shadowrocket": "",
      "Stash": ""
    }
  },
  "apps": [
    {}, {}, ...
  ]
}

```
