# Security & responsible use / 安全说明

- 此公共源码包移除了已识别的个人 Supabase 项目 ID，改为 `YOUR_SUPABASE_PROJECT_ID` 占位符。请自行创建项目并设置 Secret，不要把原账号或密钥写入 README / Issues / PR。
- `*.env.example` 是字段说明，不能写入真实 API Key。`.gitignore` 只能防止常规误提交，仍需在提交前运行密钥扫描。
- 端到端 18 个原生模型会话 **NOT_EXECUTED**。进程级模拟或 18 个上下文 ID 不等同于 18 个真实模型 Agent。
- 任何联网调用之前，必须先获得用户授权、实际验证供应商零付费保护、确认域名白名单。测试/示例中出现的假密钥字符串不可用于登录。
- 不接受含身份信息、访问令牌、生产数据库连接串或客户订单明细的公开问题报告。
- 这里是代码示例与评估工具，不自带模型服务，不绕过宿主对 Agent 数量与并发的限制。

For security reports, open a private communication channel instead of posting secrets in a public GitHub issue.
