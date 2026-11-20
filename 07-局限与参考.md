# 七、局限与参考

**局限**：本文的观察来自实际开发过程的总结和踩过的坑，没有统一的量化指标。文中出现的数字（如上下文使用率约 41%、新旧会话的耗时对比）只是特定场景下的现象，不能直接作为阈值。任务卡和对象映射会增加前期成本，收益需要在具体项目中权衡。文中提出的多数机制是建议，需要在项目中验证后再推广。

**不适用场景**：一次性脚本、边界清晰的单点修改、项目尚未形成任何文档或测试、团队对 Agent 输出没有审查能力时，本文的全流程可能成本过高，应当简化或不采用。

**外部实践**：Claude Code 的公开实践建议包括：按任务管理会话，新任务建立独立上下文，复杂任务先规划再实施，避免在已被证明不成立的方案上叠加补丁，用子 Agent 承担边界明确的调查任务。`/rewind`、`/clear`、`/compact` 是不同的处理方式，不能视为等价的清理按钮。OpenAI Codex 的公开实践建议包括：复杂任务先计划，将稳定的项目知识写入 AGENTS.md，以代码差异、测试结果和页面检查判断成果，而不是依赖口头总结。

**参考链接**（引用前请核对）：

- [Anthropic：Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [Anthropic：Claude Code 命令参考（含 /insights）](https://code.claude.com/docs/en/commands.md)
- [Anthropic：Using Claude Code — Session Management and 1M Context](https://claude.com/resources/articles/using-claude-code-session-management-and-1m-context)
- [OpenAI：How OpenAI Uses Codex to Accelerate Engineering](https://openai.com/business/guides-and-resources/how-openai-uses-codex/)
- [OpenAI：Harness Engineering](https://openai.com/index/harness-engineering/)
- [OpenAI：Custom Instructions with AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md)
- [dbaplus：向量数据库凉了？Claude Code、Cursor 为何集体抛弃 RAG？](https://dbaplus.cn/news-160-7481-1.html)
