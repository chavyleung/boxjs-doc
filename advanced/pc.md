---
description: 通过外部设备的浏览器来访问手机上的 BoxJs，外部设备包括但不限于 PC、Mac、Linux、Android……
---

# 通过 PC 访问

> 说明：以下将安装有 BoxJs 的设备称为 A，访问 BoxJs 的设备称为 B

### Quantumult X

1. 将 A、B 两台设备置于同一局域网内
2. 【A设备】使用 HTTP Backend 的方式来配置 BoxJs
3. 【A设备】设置 HTTP Backend 的监听地址为 0.0.0.0，端口默认 9999 即可
4. 【A设备】通过自身浏览器访问 http://127.0.0.1:9999 验证是否正常访问
5. 【A设备】取得本设备的局域网地址，如：192.168.x.x
6. 【B设备】打开浏览器并访问：http://192.168.x.x:9999 即可



