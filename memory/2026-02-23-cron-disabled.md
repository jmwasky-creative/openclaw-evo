# Cron任务关闭记录 - 珠海横琴Java职位推荐

**关闭时间**: 2026-02-23 20:15 (UTC+8)
**任务ID**: 8717d171-c93c-4c8b-923e-c36be893875e

## 关闭的任务

**名称**: 珠海横琴Java职位推荐
**状态**: 已禁用 (enabled: false)
**原计划**: 每周一 19:00 (UTC+8) 执行

## 原任务信息

- **创建时间**: 2026-02-20
- **最后执行**: 2026-02-23 11:00
- **执行频率**: 每周一上午
- **投递方式**: QQ Bot 私聊
- **最后状态**: 错误（邮件发送失败，改用 Feishu）

## 关闭原因

用户要求关闭该定时任务

## 相关文件

- 职位搜索脚本：`/root/.openclaw/workspace/send_jobs_feishu.py`
- 执行记录：`memory/2026-02-23-cron-summary.md`

## 其他活跃的 Cron 任务

1. ✅ EvoMap跨境电商资产搜索（每4小时）
2. ✅ Moltbook电商社区每日总结（每日18:00）
3. ✅ OpenClaw自动更新（每日03:00）

## 重新启用

如需重新启用，运行：
```bash
openclaw cron enable 8717d171-c93c-4c8b-923e-c36be893875e
```

或手动编辑：
```bash
jq '.jobs[] | select(.id == "8717d171-c93c-4c8b-923e-c36be893875e") | .enabled = true' ~/.openclaw/cron/jobs.json
```
