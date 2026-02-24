# 项目分析技能 (Project Analyzer Skill) 实现计划

## 项目结构创建

1. **创建主目录结构**
   - 创建 `agents/` 目录
   - 创建 `references/` 目录

2. **创建核心配置文件**
   - `SKILL.md` - 技能定义文件
   - `agents/agent.yaml` - 代理配置文件
   - `references/analysis-template.md` - 分析模板文件
   - `references/tech-stack-detectors.md` - 技术栈检测器配置
   - `references/mermaid-templates.md` - Mermaid 图表模板
   - `README.md` - 项目说明文件

## 核心文件实现

### 1. SKILL.md
- 定义技能名称为 "project-analyzer"
- 描述技能功能：自动分析项目结构、识别技术栈、生成结构化文档
- 详细说明工作流程：项目扫描 → 技术栈识别 → 核心模块分析 → 文档生成 → 存储
- 定义输出格式和文档结构
- 说明使用方式：`/project-analyzer` 和 `/project-analyzer --update`

### 2. agents/agent.yaml
- 配置代理接口信息
- 设置默认提示和显示名称
- 配置工作目录和环境变量

### 3. references/analysis-template.md
- 定义项目分析的模板结构
- 包含项目概述、快速开始、架构设计等章节
- 提供 Mermaid 图表生成的模板
- 定义文档输出格式

### 4. references/tech-stack-detectors.md
- 定义各种技术栈的检测规则
- 包含依赖文件识别和技术特征匹配
- 支持前端、后端、移动应用等多种项目类型

### 5. references/mermaid-templates.md
- 提供系统架构、模块关系等图表的模板
- 定义图表生成的规则和格式
- 支持流程图、关系图、时序图等多种图表类型

### 6. README.md
- 提供项目的安装和使用说明
- 详细介绍功能和工作流程
- 包含示例命令和使用场景

## 文档存储结构

技能将生成以下文档结构：

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

## 实现特点

- **自动化分析**：自动扫描项目结构，识别技术栈和核心模块
- **结构化文档**：生成标准化的项目文档，包含多个章节
- **可视化图表**：使用 Mermaid 生成架构和模块关系图表
- **元数据管理**：维护文档的元数据信息
- **易于使用**：通过简单的命令即可触发分析和文档生成

## 测试计划

1. 安装技能到 Trae IDE
2. 运行 `/project-analyzer` 命令分析示例项目
3. 验证生成的文档结构和内容
4. 运行 `/project-analyzer --update` 命令测试更新功能
5. 检查生成的 Mermaid 图表是否正确

该技能将帮助开发团队快速理解项目结构，为新手提供项目文档，同时为团队提供项目文档的自动维护机制。