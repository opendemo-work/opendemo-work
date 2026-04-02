# OpenDemo · 智能化技术演示平台

<p align="center">
  <img src="https://img.shields.io/badge/demos-532%2B-0056b3?style=flat-square" alt="532+ Demos">
  <img src="https://img.shields.io/badge/stacks-12-00a3e0?style=flat-square" alt="12 Stacks">
  <img src="https://img.shields.io/badge/license-MIT-28a745?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/status-active-7b42bc?style=flat-square" alt="Active">
</p>

<p align="center">
  <b>从代码到云原生的一站式技术演示平台</b><br>
  532+ 生产级 Demo · 12 大技术栈 · 智能 CLI 工具 · 统一命名规范 · 体系化学习路径
</p>

<p align="center">
  <a href="./index.html">🏠 项目主页</a> •
  <a href="https://github.com/opendemo/opendemo">📦 主仓库</a> •
  <a href="https://github.com/opendemo/opendemo/tree/main/opendemo-cli">🔧 CLI 文档</a> •
  <a href="#learning-paths">🛤️ 学习路径</a> •
  <a href="#contribute">🤝 参与贡献</a>
</p>

---

## 🎯 项目简介

**OpenDemo** 是一个面向真实生产场景的综合性技术学习与演示平台。我们不仅提供代码示例，更提供从基础语法到企业级架构的完整技术百科全书：

- **532+ 个经过验证的技术 Demo**，覆盖 Kubernetes、AI/ML、Go、Node.js、Java、Python、数据库、Linux 等 12 大技术栈
- **智能化 CLI 工具** (`opendemo-cli`)，支持 Demo 搜索、AI 自动生成、质量校验、README 自动同步
- **每栈一套生产级命名规范** (`NAMING_CONVENTIONS.md`)，让团队协作零歧义
- **每栈一份专业 CLI 速查表**，运维排障拿来即用
- **四条体系化学习路径**，从初学者到 AI 工程师循序渐进

> 🌐 **在线主页**: 打开 [`index.html`](./index.html) 即可浏览本项目的可视化主页。
> 🌐 **Bilingual**: 主页支持一键 **中文 / English** 切换。

---

## 🚀 快速开始

### 1. 浏览项目主页

```bash
# 方式一：直接用浏览器打开
open index.html

# 方式二：启动本地服务器
python -m http.server 8080
# 然后访问 http://localhost:8080
```

### 2. 探索主项目

```bash
# 克隆主仓库
git clone https://github.com/opendemo/opendemo.git
cd opendemo

# 查看项目结构
tree -L 2

# 安装并使用 CLI 工具
cd opendemo-cli
pip install -e .
opendemo --help
```

### 3. CLI 常用命令

```bash
# 搜索 Demo
opendemo search "goroutines" --stack go

# AI 生成新 Demo
opendemo generate kubernetes "canary-deployment"

# 质量校验
opendemo verify --auto-fix

# 列出某技术栈全部 Demo
opendemo list demos --stack python
```

---

## ✨ 核心亮点

| 特性 | 说明 |
|------|------|
| 🧠 **AI 智能生成 Demo** | 输入主题即可自动生成完整代码、配置、文档与元数据 |
| 🔍 **多维度智能检索** | 按技术栈、关键词、难度、时长精准定位，支持 weighted scoring |
| ✅ **质量校验与自动化** | 自动检查代码规范、README 完整性、元数据一致性，支持一键修复 |
| 📋 **统一命名规范** | 每技术栈配备生产环境级命名规范，保障团队协作 |
| ⚡ **CLI 速查表** | k8s-cli、linux-cli、database-cli 等专业命令行速查表 |
| 🛤️ **体系化学习路径** | 初学者 → 全栈 → 企业级 → AI 工程师，成长路线清晰 |
| 🌐 **双语主页** | 项目主页支持一键 **中文 / English** 切换，服务全球开发者 |

---

## 🏗️ 技术栈覆盖

| 技术栈 | Demo 数量 | 特色亮点 |
|--------|----------|----------|
| **Kubernetes** | 170 | 云原生编排、Kubeflow、LLMOps、Operator、服务网格 |
| **Go** | 95 | 并发编程、微服务、性能优化、云原生工具链 |
| **Node.js** | 71 | 全栈 Web、实时通信、部署运维、限流熔断 |
| **Python** | 56 | 数据科学、异步编程、系统工具、测试实践 |
| **Database** | 38 | 高可用架构、性能优化、容灾备份、云数据库 |
| **Java** | 23 | 面向对象、JVM 诊断、企业级开发规范 |
| **Linux** | 19 | 系统监控、网络诊断、生产运维、安全日志 |
| **AI / ML** | 15 | LLM 训练/微调/推理/运维、MLOps、RAG、联邦学习 |
| **Container** | 8 | Docker、Containerd、RunC 容器化最佳实践 |
| **Traffic** | 8 | Nginx、HAProxy、Higress 负载均衡与 API 网关 |
| **Monitoring** | 7 | Prometheus、Grafana、ELK/EFK、可观测性 |
| **Messaging** | 4 | RocketMQ 消息队列、事务消息、延迟消息 |

> 数据来源: [`opendemo/README.md`](https://github.com/opendemo/opendemo/blob/main/README.md) 与 [`DETAILED_STRUCTURE.md`](https://github.com/opendemo/opendemo/blob/main/DETAILED_STRUCTURE.md)

---

## 🏛️ 平台架构

OpenDemo 采用 **搜索 → 生成 → 验证 → 同步** 的四位一体工作流：

```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│ DemoSearch  │ → │ DemoGenerator│ → │ DemoVerifier│ → │ReadmeUpdater│
│  智能检索    │    │  AI 自动生成 │    │  质量校验    │    │ README 同步  │
└─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘
```

核心模块：
- **`DemoSearch`** — 基于 weighted scoring 的多维度搜索引擎
- **`DemoGenerator`** — 协调 AI 服务自动生成 Demo 内容与元数据
- **`DemoVerifier`** — 校验代码、文档与配置的规范性与一致性
- **`QualityChecker`** — 评估 Demo 完整度、清晰度与生产相关性
- **`ReadmeUpdater`** — 自动将新 Demo 汇总到主文档与交叉索引

---

<a name="learning-paths"></a>
## 🛤️ 学习路径推荐

### 🎓 初学者路径（3-6 个月）
```
Linux 基础 → Python 入门 → 数据库基础 → Node.js Web 开发
```
适合零基础，快速建立系统操作能力与编程思维。

### 💼 全栈开发者路径（6-12 个月）
```
Node.js 全套 → Go 后端 → 数据库优化 → Kubernetes → AI/ML 入门
```
构建端到端交付能力，从 Web 开发到云原生部署全覆盖。

### 🏢 企业级开发者路径（12-18 个月）
```
Java 企业级 → 微服务架构 → 数据库高可用 → 监控运维 → 安全合规
```
掌握大规模系统设计，聚焦高可用、可观测性与企业标准。

### 🚀 AI 工程师路径（18-24 个月）
```
数学基础 → 深度学习 → LLM 训练 → MLOps → 模型部署
```
从算法到工程化全链路覆盖，聚焦大模型训练、推理与服务化。

---

## 📁 目录映射

本仓库 (`opendemo-work`) 为项目主页与入口仓库，核心代码与 Demo 位于主仓库：

| 本仓库 | 主仓库对应路径 | 说明 |
|--------|---------------|------|
| `index.html` | — | 本项目的可视化主页 |
| `assets/` | — | 主页样式与静态资源 |
| `README.md` | `opendemo/README.md` | 主项目总览文档 |
| — | `opendemo/opendemo-cli/` | 智能化 CLI 工具 |
| — | `opendemo/DETAILED_STRUCTURE.md` | 完整目录结构清单 |
| — | `opendemo/PROJECT_STRUCTURE_ANALYSIS_REPORT.md` | 架构深度分析报告 |

---

<a name="contribute"></a>
## 🤝 参与贡献

OpenDemo 是一个开放共建的项目，欢迎各种形式的贡献：

- 🐛 **Bug 修复** — 完善现有 Demo 的功能和稳定性
- ✨ **新示例添加** — 补充各技术栈的实用案例
- 📚 **文档优化** — 改进 README、命名规范与使用说明
- 🔧 **工具改进** — 优化 opendemo-cli 与自动化脚本
- 🎨 **体验提升** — 改善项目结构、主页设计与用户界面

### 贡献步骤

1. Fork 主仓库 [`opendemo/opendemo`](https://github.com/opendemo/opendemo)
2. 创建你的功能分支 (`git checkout -b feature/amazing-demo`)
3. 提交更改 (`git commit -m 'Add some amazing demo'`)
4. 推送分支 (`git push origin feature/amazing-demo`)
5. 开启一个 Pull Request

---

## 📄 许可证

本项目采用 [MIT License](https://github.com/opendemo/opendemo/blob/main/LICENSE) 开源许可证。

---

<p align="center">
  Made with ❤️ by the OpenDemo Community
</p>
