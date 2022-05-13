---
description: 本文介绍如何配置 BoxJs 订阅文件
---

# 配置文档 (\*.boxjs.json)

## &#x20;​全量配置

待完善

## 场景介绍

### 安装事件 (onInstall)

如果希望用户在添加 BoxJs 后，自动安装重写 (.sgmodule, .snippet……)

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
      "QuanX": "",
      "Loon": "loon://update?sub=all",
      "Shadowrocket": "",
      "Stash": ""
    }
  },
  "apps": [
    {}, {}, ...
  ]
}

```
