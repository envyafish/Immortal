# CLAUDE.md

## 项目概述

这是一个版本说明项目，用于记录每次发布的功能点和修复内容。

## 功能说明

用户输入 `功能点` 或 `修复点` 后，AI 负责润色文字并添加合适的 emoji，使版本说明更加清晰和易读。

### 版本更新

当用户发布新版本时，AI 需要同步更新以下文件：

- `CHANGELOG.md` — 在顶部新增版本条目
- `latest.json` — 更新 version、docker_image 和 notes
- `versions.json` — 在 items 数组顶部插入新版本条目，并更新 latest 字段
