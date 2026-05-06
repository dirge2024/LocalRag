# LocalRAG 开发总览

## 模块列表

| 序号 | 模块 | 状态 | 说明 |
|------|------|------|------|
| 01 | 框架初始化 | ✅ | docker-compose + 父POM + 模块骨架 |
| 02 | storage | ✅ | MinIO composeObject + Redis 进度追踪 + MySQL |
| 03 | messaging | ✅ | Kafka 生产者封装 |
| 04 | document | ✅ | Tika 解析 + 三级降级分块 |
| 05 | embedding | ✅ | Qwen v4 / DeepSeek 双实现 |
| 06 | vector-store | ✅ | ES dense_vector + IK 分词 |
| 07 | retrieval | ✅ | KNN → BM25 → rescore 瀑布检索 |
| 08 | llm | ✅ | DeepSeek SSE 流式 + 会话管理 |
| 09 | 前端页面 | ✅ | 侧边栏四入口 + 五页面统一布局 |

## 文档结构

每个模块目录下保留：

- `需求分析.md` — 核心业务逻辑、关键决策、边界条件、技术难点
- 补充文档（如 `MySQL持久化.md`、`状态追踪与去重优化.md`）

其他开发记录已移至项目根目录 `doc/` 文件夹。
