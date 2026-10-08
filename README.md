# AGI Skills · Dual16 Agent Harness

中文多 Agent 编排与评测项目，包含 **AGI Harness** 和 **AGI Super Power**：任务归属、双主控 + 16 Worker 协议、离线验证、失败注入与回放。

## 下载完整源码

本次以完整源码 ZIP 形式发布，保留项目目录结构。**725 个文件**包含 Python / JavaScript 源码、Skills、测试、文档、样例和历史验证记录。

**[下载 AGI-Skills-Source.zip](./AGI-Skills-Source.zip)**（打开后点击下载按钮）

解压后的主要目录：

| 目录 | 内容 |
| --- | --- |
| `agi-harness/` | AGI Harness `1.0.0rc1`，编排、评估、回放和离线验证 |
| `agi-super-power/` | AGI Super Power `3.4.0-rc.7`，Dual16 协议、Bridge、Skills 与测试 |
| `integrations/` | MCP 配置示例；使用前自行替换占位符 |

## 快速开始

要求 Python 3.12+。下载并解压源码 ZIP，进入解压目录后执行：

```bash
cd agi-harness
python -m agi_harness doctor
python scripts/verify_v1.py --out runs/my-first-check
```

输出目录 `runs/my-first-check` 必须尚不存在。以上是离线检查，无需 API Key；详细说明见解压后的 `agi-harness/README.md`。

AGI Super Power 的离线验证：

```bash
cd ../agi-super-power
python -B scripts/validate_dual16.py --out ../dual16-check-new
```

## 能力边界

- 项目为研究与工程迭代候选版，不是 OpenAI 或 Anthropic 官方产品。
- 离线夹具与测试进程不等于真实模型 Agent；18 个独立原生模型会话的完整实机验收尚未完成。
- 包内测试报告是历史记录，本次发布不代表重新运行全部测试。
- 真实模型调用需自行配置凭据、授权和预算。不要将密钥、客户数据或私有日志上传到仓库。

## 许可与贡献

自有代码采用 [MIT License](./LICENSE)。第三方材料遵循源码包内的 `agi-super-power/THIRD_PARTY_NOTICES.md` 及其各自许可。

欢迎下载复现、提交问题和改进建议。反馈请附最小复现、运行环境、执行命令及预期与实际结果。安全说明见 [SECURITY.md](./SECURITY.md)。

**English:** AGI Skills is an experimental Dual16 orchestration and evaluation workbench. Download the complete source archive to explore both AGI Harness and AGI Super Power, run offline checks, and contribute reproducible improvements. Native 18-session LLM validation is not complete.
