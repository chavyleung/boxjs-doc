---
description: 如果使用 BoxJs 的过程中遇到白屏，无法打开等症状，可以尝试手动运行以下脚本！
---

# 急救

### 抹掉全局备份

{% hint style="danger" %}
如果在全局备份后出现 VPN 自动断连、日志出现内存警告，可尝试抹掉备份！
{% endhint %}

> 出现这个问题，是因为备份的数量过多，内存不足引起的，建议把备份数量控制在 3 个以内。

```bash
# Surge & Loon
$persistentStore.write('', 'chavy_boxjs_globalBaks')
$done()

# QuanX
# 先把 QX 的示例代码全部删掉，再粘贴下面两行代码！
$prefs.setValueForKey('', 'chavy_boxjs_globalBaks')
$done()
```

### 

### 抹掉订阅缓存

{% hint style="danger" %}
如果你在添加订阅后，出现白屏现象，可尝试抹掉订阅缓存！
{% endhint %}

> 抹掉订阅缓存是非常安全的操作，不会对已保存的会话、设置产生任何影响，可以放心抹掉。

```bash
# Surge & Loon
$persistentStore.write('', 'chavy_boxjs_app_subCaches')
$done()

# QuanX
# 先把 QX 的示例代码全部删掉，再粘贴下面两行代码！
$prefs.setValueForKey('', 'chavy_boxjs_app_subCaches')
$done()
```



### 如何运行脚本

```bash
# Surge
首页 > 脚本 > 编辑器 > 把脚本粘进去 > 执行

# QuanX
风车 > 调试 > 构造请求 > 添加 > 下一步 > 把示例代码`全部`删掉 > 把脚本粘进去 > 执行

# Loon
配置 > 脚本 > 本地JS文件 > 添加 > 创建新脚本 > 随便填个脚本名字 > 把脚本粘进去 > 运行
```

