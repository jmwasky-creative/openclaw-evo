# 测试向量索引

这是一个测试文件，用于验证 OpenClaw 记忆索引功能。

## 关键信息

- **测试日期**: 2026-02-23
- **测试目标**: 验证 FTS 全文搜索是否工作
- **关键词**: 测试、索引、搜索、向量、FTS

## 技术栈

- OpenClaw 版本: 2026.2.21-2
- 数据库: SQLite
- 搜索引擎: FTS (Full-Text Search)
- 状态: FTS-only 模式（无向量嵌入）

## 预期结果

运行 `openclaw memory search "测试"` 应该能找到这个文件。
