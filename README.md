# CSCA — 网络安全与AI咨询专家

CSCA（Cybersecurity & AI Consulting Agent）是一个面向 Claude Code 的专业咨询 skill，用于产出符合咨询公司交付标准的网络安全与AI咨询交付物。

## 设计理念

三条核心原则：

1. **咨询优先**：先理解、分析、规划，再生成内容。不跳过分析直接输出。
2. **四阶段交付**：所有面向客户的交付物经过「分析 — 规划 — 生成 — 审查」完整流程。
3. **去AI化**：交付物消除AI写作痕迹，输出读起来像资深顾问手笔，可直接交付客户。

## 能力覆盖

### 网安咨询

| 领域 | 典型场景 |
|------|---------|
| 安全评估 | 渗透测试、代码审计、日志分析、数据安全 |
| 咨询规划 | 需求分析、安全建设方案、等保咨询、成熟度评估 |
| 培训赋能 | 课程设计、PPT课件、CTF题目、实验环境 |
| 研发支持 | 安全Demo开发（Java/Python/Go）、安全工具、漏洞PoC |
| 商务支撑 | 报价方案、人天计算、预算编制、招投标文件 |
| 专业写作 | 咨询报告、制度文档、技术方案、合规审计 |

### AI咨询（双方向）

| 方向 | 典型场景 |
|------|---------|
| AI赋能网安 | AI威胁检测、SOC Copilot、AI代码审计、AI渗透测试、AI威胁情报、AI+SOAR/SIEM |
| 安全赋能AI | OWASP LLM Top 10评估、大模型红队测试、AI合规/算法备案/TC260-003 |
| AI战略 | AI成熟度评估、路线图规划、模型选型、RAG与Agent架构设计、Make vs Buy |


## 文件结构

```
.claude/
├── CLAUDE.md                          # 工作空间配置
└── skills/csca/
    ├── SKILL.md                        # Skill 入口：激活规则、四阶段框架、能力路由
    ├── identity.md                     # 八大咨询角色定义与角色分配表
    ├── principles.md                   # 核心原则、非目标约束、专业伦理
    ├── workflow.md                     # 八阶段工作流细则与轻量级任务规则
    ├── writing.md                      # 写作规范核心：160+禁用词（七类）、表格去AI规则、语体分级、视觉格式
    ├── review.md                       # 两轮审查标准：关键点事实核查 + 七维度质量评分
    ├── knowledge/                      # 领域知识库（按需加载）
    │   ├── industry-standards.md        # 等保/ISO 27001/NIST/行业监管标准
    │   ├── methodologies.md             # OWASP/PTES/STRIDE/ATT&CK方法论
    │   ├── compliance.md                # 网络安全法/数据安全法/个人信息保护法/密评
    │   ├── tech-domains.md              # 网络安全/AI安全/数据安全/云安全技术域
    │   ├── ai-consulting.md             # AI双方向咨询知识速查
    │   └── business-practices.md        # 报价/人天/招投标商务实践
    ├── templates/                      # 交付物模板（八种）
    │   ├── pentest-report.md            # 渗透测试报告
    │   ├── security-assessment.md       # 安全评估报告
    │   ├── risk-assessment.md           # 风险评估报告
    │   ├── incident-report.md           # 应急响应/事件分析报告
    │   ├── solution-proposal.md         # 安全建设方案
    │   ├── compliance-audit.md          # 合规审计报告
    │   ├── training-plan.md             # 培训方案/课件
    │   └── project-bid.md               # 报价/投标文件
    └── examples/                       # 交付物示例
        ├── security-assessment-example.md
        ├── solution-proposal-example.md
        └── training-plan-example.md
```

## 安装与使用

### 前提条件

- Claude Code CLI 或支持的 IDE 扩展（VS Code / JetBrains）
- 将本仓库 `.claude/` 目录放置于项目根目录

### 启动方式

**手动调用**：输入 `/csca` 或「启动CSCA」「用咨询专家模式」。

**自动激活**：描述安全或AI咨询需求时，Skill 根据场景关键词自动匹配并激活。例如：
- 「帮我写一份渗透测试报告」
- 「设计一个等保三级整改方案」
- «评估这个AI应用的安全性（OWASP LLM Top 10）»
- «规划企业AI安全治理框架»

激活后，CSCA 按照「分析 — 规划 — 生成 — 两轮审查」流程完成交付。

## 写作规范要点

交付物严格执行去AI化规则，核心要求：

- **禁用词**：160+ 项，七类（空话套话、AI连接词、营销腔、论文腔、机械句式、口语词、AI符号）
- **语体**：默认 L1 正式语体，零口语词、零感叹句、零AI符号
- **格式**：正文黑色文字；表格允许灰度色系专业配色，禁用高饱和度彩色；风险等级只用文字；强调只用加粗
- **证据**：每个论断须有依据（标准引用、行业实践、逻辑推导、经验判断、测试数据）
- **自检**：25 项自检清单，全通过才交付

## 版本

当前版本：**v2.2**

详见 [CHANGELOG.md](CHANGELOG.md)

## 许可

本项目仅供授权咨询场景使用。渗透测试模板和工具使用须遵守适用法律法规，在获得明确授权后方可执行。
