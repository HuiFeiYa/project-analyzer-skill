---
name: project-analyzer
description: 自动分析项目结构、识别技术栈、生成结构化文档和Mermaid图表
version: 1.0.0
---

# Project Analyzer Skill

## 技能信息

- **技能名称**: project-analyzer
- **版本**: 1.0.0
- **描述**: 自动分析项目结构、识别技术栈、生成结构化文档和Mermaid图表
- **作者**: Trae AI

## 功能说明

- **项目结构扫描**: 递归扫描项目目录，生成文件树
- **技术栈识别**: 分析依赖文件和配置文件，识别技术栈
- **核心模块分析**: 识别入口文件、核心模块和关键API
- **文档生成**: 基于分析结果生成结构化文档和Mermaid图表
- **文档存储**: 将生成的文档存储在 `.trae/repowiki` 目录下
- **元数据管理**: 生成和维护 `repowiki-metadata.json` 文件

## 工作流程

1. **项目扫描**: 递归遍历项目目录，收集文件和目录信息
2. **技术栈识别**: 分析依赖文件、配置文件和代码特征，识别项目使用的技术栈
3. **核心模块分析**: 识别项目的入口文件、核心模块和关键API
4. **文档生成**: 基于分析结果，使用模板生成结构化文档和Mermaid图表
5. **文档存储**: 将生成的文档存储在 `.trae/repowiki/content/` 目录下
6. **元数据更新**: 更新 `.trae/repowiki/meta/repowiki-metadata.json` 文件

## 使用方式

### 基本使用

```
/project-analyzer
```

技能会自动分析当前目录的项目结构并生成文档。

### 更新文档

```
/project-analyzer --update
```

重新分析项目并更新文档。

## 输出格式

### 文档结构

```
.trae/
└── repowiki/
    ├── content/
    │   ├── 项目概述.md
    │   ├── 快速开始.md
    │   ├── 架构设计.md
    │   ├── 核心模块.md
    │   ├── API参考.md
    │   ├── 数据库模型.md
    │   └── 开发指南.md
    └── meta/
        └── repowiki-metadata.json
```

### 文档内容

- **项目概述**: 项目基本信息、技术栈、主要功能
- **快速开始**: 安装步骤、运行方法、开发环境搭建
- **架构设计**: 系统架构、模块关系、数据流
- **核心模块**: 核心功能模块、关键组件、实现细节
- **API参考**: 主要API接口、参数说明、返回值
- **数据库模型**: 数据结构、表设计、关系模型
- **开发指南**: 编码规范、开发流程、部署说明

### Mermaid图表

- **系统架构图**: 展示系统的整体架构和组件关系
- **模块关系图**: 展示各个模块之间的依赖和调用关系
- **数据流图**: 展示数据在系统中的流动路径
- **业务流程图**: 展示核心业务流程的执行步骤

## 配置文件

- **agents/agent.yaml**: 代理配置文件
- **references/analysis-template.md**: 分析模板文件
- **references/tech-stack-detectors.md**: 技术栈检测器配置
- **references/mermaid-templates.md**: Mermaid图表模板

## 技术栈检测

支持检测的技术栈包括：

- **前端**: React、Vue、Angular、Svelte、Next.js、Nuxt.js等
- **后端**: Node.js、Python、Java、Go、Ruby、PHP等
- **数据库**: MySQL、PostgreSQL、MongoDB、Redis等
- **工具链**: Webpack、Vite、Rollup、Babel等
- **部署**: Docker、Kubernetes、AWS、GCP等

## 注意事项

- 技能会自动忽略 `.git`、`node_modules` 等常见的忽略目录
- 对于大型项目，分析可能需要较长时间
- 生成的文档会覆盖现有的 `.trae/repowiki` 目录内容
- 使用 `--update` 参数可以更新已有的文档

## 示例

### 输入

```
/project-analyzer
```

### 输出

```
✅ 项目分析完成！

已生成以下文档：
- .trae/repowiki/content/项目概述.md
- .trae/repowiki/content/快速开始.md
- .trae/repowiki/content/架构设计.md
- .trae/repowiki/content/核心模块.md
- .trae/repowiki/content/API参考.md
- .trae/repowiki/content/数据库模型.md
- .trae/repowiki/content/开发指南.md

已更新元数据：
- .trae/repowiki/meta/repowiki-metadata.json

📚 文档已准备就绪，您可以在 Trae IDE 中查看。
```