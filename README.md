
# Immortal

---

# Status

⚠️ **Maintenance Mode**

该项目目前处于 **维护模式（maintenance mode）**：

* ✅ 接受 **Bug 报告**
* ❌ 不接受 **新功能请求 (Feature Request)**
* ❌ 不接受 **改进建议**
* ❌ 不接受 **Roadmap / 规划讨论**

如果 Issue 属于以上类型，可能会被直接关闭。

---


# Reporting Bugs

如果你发现 Bug，请通过 GitHub Issue 提交。

提交 Issue 前建议：

1. 确认问题在 **最新版本** 仍然存在
2. 搜索已有 Issue，避免重复提交
3. 尽量提供完整复现信息

提交 Bug 时请包含：

* **Bug 描述**
* **复现步骤**
* **期望行为**
* **实际行为**
* **运行环境**
* **日志或截图**

Bug Issue 地址：

[https://github.com/envyafish/Immortal/issues](https://github.com/envyafish/Immortal/issues)

---

# Unsupported Issues

以下 Issue **不会被处理**：

* Feature Requests
* Enhancement Suggestions
* API Design Discussions
* Product Ideas
* Usage Questions

这类 Issue 可能会被 **直接关闭 (closed without discussion)**。

---

# Changelog

[CHANGELOG.md](./CHANGELOG.md)

# Update Metadata

[latest.json](./latest.json)

[versions.json](./versions.json)

---

# Docker Compose

```yaml
services:
  immortal:
    image: envyafish/immortal:latest
    container_name: immortal
    ports:
      - "8000:8000"
    volumes:
      - ./data:/data
    environment:
      DATABASE_URL: <postgresql://user:password@host:port/db>
      # 或使用下面这组 PostgreSQL 配置，二选一
      POSTGRES_HOST: <HOST>
      POSTGRES_PORT: <PORT>
      POSTGRES_USER: <USER>
      POSTGRES_PASSWORD: <PASSWORD>
      POSTGRES_DB: <DB>
```

启动：

```bash
docker compose up -d
```

更新到新版本：

```bash
docker compose pull
docker compose up -d --force-recreate
```

如果你想查看更新内容：

- [CHANGELOG.md](./CHANGELOG.md)
- [latest.json](./latest.json)
- [versions.json](./versions.json)
