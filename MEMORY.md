# MEMORY.md - Long-term Memory

## User: easy

- **Name:** easy
- **Timezone:** Asia/Shanghai (UTC+8)
- **Core Philosophy:** 追求变异（多样性）、变易（变简单）、做正反馈的事件
- **Status:** 长期践行这套方法论的老手，不是刚开始摸索

## CC (Assistant)

- **Name:** CC
- **Vibe:** Cool, sardonic, secretly caring, slightly mysterious
- **Emoji:** 🎭
- **Avatar:** https://ui-avatars.com/api/?name=CC&background=4a2c4a&color=fff&size=256

---

## System Configuration

### OpenClaw Setup
- **Version**: 2026.2.21-2 (upgraded from 2026.2.9 on 2026-02-23)
- **Node**: v22.22.0 (nvm managed)
- **Workspace**: /root/.openclaw/workspace
- **Config**: ~/.openclaw/openclaw.json
- **Service**: systemd user service (enabled)
- **Model**: glmcode/glm-4.7 (primary)

### Installed Plugins
- **qqbot**: @sliverp/qqbot@1.4.2 (appId: 102842234)
- **ddingtalk**: git+https://cnb.cool/lighthouse/lighthousebackend/openclaw-dingtalk.git
- **wecom**: git+https://cnb.cool/lighthouse/lighthousebackend/openclaw-wecom.git
- **adp-openclaw**: 0.0.24
- **feishu**: built-in (missing @larksuiteoapi/node-sdk dependency)

### Channels
- **QQ Bot**: enabled, fully functional
- **Email**: QQ SMTP (964692548@qq.com)

### EvoMap Integration
- **Node ID**: node_cc_a1b2c3d4e5f6
- **Claim Code**: GNNB-WPRQ
- **Status**: Registered, awaiting account binding
- **Skill**: ~/.agents/skills/evomap (installed 2026-02-21)

---

## Key Decisions & Preferences

### Technical Preferences
- Prefers simple, practical solutions over complex frameworks
- Values diversity and mutation in approaches
- Positive feedback loop focused
- Automation-first mindset

### Platform Choices
- **Primary**: QQ Bot for daily communication
- **Backup**: Email for important notifications
- **Development**: Local workspace with git
- **Memory**: File-based (MEMORY.md + memory/YYYY-MM-DD.md)

### Completed Projects
1. **EvoMap跨境电商搜索** (2026-02-22)
   - Discovered 22,466 total assets
   - Identified market gap in cross-border e-commerce tools
   - High-value assets: HTTP retry (GDI 70.9), order processing (GDI 63.0)

2. **OpenClaw升级** (2026-02-23)
   - Version 2026.2.9 → 2026.2.21-2
   - Fixed Feishu dependency issue
   - Gateway running on 127.0.0.1:18789

---

## Maintenance Notes

### Regular Tasks
- Daily logs: memory/YYYY-MM-DD.md
- Weekly MEMORY.md review and consolidation
- Monthly dependency updates

### Known Issues
- Gateway shows "unreachable" status (cosmetic, functional)
- System Node 22+ not installed (using nvm)
- Feishu plugin dependency missing (unused)

### File Structure
```
/root/.openclaw/workspace/
├── MEMORY.md              # This file
├── memory/
│   ├── 2026-02-21.md
│   ├── 2026-02-22.md
│   └── 2026-02-23.md
├── skills/
│   ├── clawlist/
│   ├── agent-browser/
│   └── ...
└── SOUL.md, USER.md, etc.
```
