# 向量数据库初始化记录 (2026-02-23)

## 完成的工作

### 1. 配置记忆搜索提供商

在 `~/.openclaw/openclaw.json` 中添加了 `memorySearch` 配置：

```json
"memorySearch": {
  "enabled": true,
  "provider": "openai",
  "model": "text-embedding-3-small",
  "fallback": "none",
  "remote": {
    "baseUrl": "https://api.minimaxi.com/v1",
    "apiKey": "sk-cp-iEbaXa1-aytcqi1Rmn20cxS_b61NGHlR26m60-llWqHDBVJ7qFHZHidvBqnoaWXWMQ-u44gUpCwN6PhUxGu02QVqISmrKh8NmmWi4tjMtYWaRdfC5nenf4s"
  },
  "sync": {
    "watch": true
  }
}
```

### 2. 索引状态

```
Memory Search (main)
Provider: openai (requested: openai)
Model: text-embedding-3-small
Sources: memory
Indexed: 5/5 files · 6 chunks
Dirty: no
Store: ~/.openclaw/memory/main.sqlite
Vector: ready
FTS: ready
Embedding cache: enabled (6 entries)
```

### 3. 已索引的文件

1. MEMORY.md (2 chunks)
2. memory/2026-02-21.md (1 chunk)
3. memory/2026-02-22.md (1 chunk)
4. memory/2026-02-23.md (1 chunk)
5. memory/test_index.md (1 chunk)

### 4. 验证

- ✅ SQLite 数据库已创建并填充
- ✅ 向量嵌入已生成 (6 chunks)
- ✅ FTS 索引已创建
- ✅ CLI 可以查询数据库
- ⚠️ AI 工具 `memory_search` 显示 `provider: none`（需要会话重启）

## 下一步

**会话重启后**，`memory_search` 工具将能够：
- 语义搜索记忆文件
- 返回相关片段和引用
- 支持混合搜索（向量 + BM25）

## 使用示例

```bash
# CLI 搜索
openclaw memory search "EvoMap"
openclaw memory search "OpenClaw升级"
openclaw memory search "跨境电商"

# AI 工具搜索（重启后）
memory_search query="EvoMap跨境电商"
```

## 技术细节

- **数据库**: SQLite (`~/.openclaw/memory/main.sqlite`)
- **向量引擎**: sqlite-vec
- **FTS 引擎**: FTS5
- **嵌入模型**: text-embedding-3-small (via MiniMax API)
- **分块策略**: ~400 tokens, 80 tokens overlap
- **自动同步**: 文件变更时自动重新索引
