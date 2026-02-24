# Project Analyzer Skill

## 项目简介

Project Analyzer Skill 是一个自动分析项目结构、识别技术栈、生成结构化文档和Mermaid图表的技能。它可以帮助开发团队快速理解项目结构，为新手提供项目文档，同时为团队提供项目文档的自动维护机制。

## 核心功能

- **项目结构扫描**: 递归扫描项目目录，生成文件树
- **技术栈识别**: 分析依赖文件和配置文件，识别技术栈
- **核心模块分析**: 识别入口文件、核心模块和关键API
- **文档生成**: 基于分析结果生成结构化文档和Mermaid图表
- **文档存储**: 将生成的文档存储在 `.trae/repowiki` 目录下
- **元数据管理**: 生成和维护 `repowiki-metadata.json` 文件

## 安装方式

### 方法一：通过 npx 安装

```bash
npx skills add D:\playground\project-analyzer-skill
```

### 方法二：手动安装

1. 克隆或下载项目到本地目录
2. 打开 Trae IDE
3. 点击 "技能管理"
4. 点击 "添加技能"
5. 选择项目目录
6. 点击 "确认"

## 使用方式

### 基本使用

在 Trae IDE 的命令行中输入：

```
/project-analyzer
```

技能会自动分析当前目录的项目结构并生成文档。

### 更新文档

在 Trae IDE 的命令行中输入：

```
/project-analyzer --update
```

重新分析项目并更新文档。

### 自定义参数

| 参数名 | 类型 | 描述 | 默认值 |
|--------|------|------|--------|
| update | boolean | 更新已有的文档 | false |
| depth | number | 目录扫描深度 | 5 |
| ignore | array | 忽略的目录和文件 | ["node_modules", ".git", ".trae", "dist", "build"] |

## 工作流程

1. **项目扫描**: 递归遍历项目目录，收集文件和目录信息
2. **技术栈识别**: 分析依赖文件、配置文件和代码特征，识别项目使用的技术栈
3. **核心模块分析**: 识别项目的入口文件、核心模块和关键API
4. **文档生成**: 基于分析结果，使用模板生成结构化文档和Mermaid图表
5. **文档存储**: 将生成的文档存储在 `.trae/repowiki/content/` 目录下
6. **元数据更新**: 更新 `.trae/repowiki/meta/repowiki-metadata.json` 文件

## 文档结构

生成的文档结构如下：

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

### 文档内容说明

- **项目概述**: 项目基本信息、技术栈、主要功能和项目结构
- **快速开始**: 环境要求、安装步骤、运行方法和开发环境搭建
- **架构设计**: 系统架构、模块关系、数据流和核心流程的图表
- **核心模块**: 核心功能模块的详细说明，包括功能、关键文件和依赖关系
- **API参考**: 主要API接口的参数说明、返回值和使用示例
- **数据库模型**: 数据结构、表设计和关系模型
- **开发指南**: 编码规范、开发流程、部署说明和常见问题

## 技术栈支持

### 前端技术栈
- React
- Vue
- Angular
- Svelte
- Next.js
- Nuxt.js
- Vite
- Webpack
- Babel

### 后端技术栈
- Node.js
- Python
- Java
- Go
- Ruby
- PHP
- NestJS
- Express
- Koa

### 数据库技术栈
- MySQL
- PostgreSQL
- MongoDB
- Redis
- SQLite

### 工具链
- Docker
- Kubernetes
- Git
- ESLint
- Prettier
- Jest
- Mocha

### 部署技术栈
- AWS
- GCP
- Azure
- Heroku

### 移动应用技术栈
- React Native
- Flutter
- Ionic

## 配置文件

### 技能定义文件
- **SKILL.md**: 定义技能名称、描述和功能

### 代理配置文件
- **agents/agent.yaml**: 配置代理接口信息

### 分析模板文件
- **references/analysis-template.md**: 定义项目分析的模板结构

### 技术栈检测器配置
- **references/tech-stack-detectors.md**: 定义各种技术栈的检测规则

### Mermaid图表模板
- **references/mermaid-templates.md**: 提供系统架构、模块关系等图表的模板

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

## 注意事项

- 技能会自动忽略 `.git`、`node_modules` 等常见的忽略目录
- 对于大型项目，分析可能需要较长时间
- 生成的文档会覆盖现有的 `.trae/repowiki` 目录内容
- 使用 `--update` 参数可以更新已有的文档

## 故障排除

### 常见问题

1. **分析失败**
   - 检查项目目录是否存在
   - 检查项目是否有足够的权限
   - 检查是否有循环依赖

2. **技术栈识别不准确**
   - 检查项目的依赖文件是否完整
   - 检查代码中是否有明显的技术特征
   - 可以手动更新技术栈检测规则

3. **文档生成不完整**
   - 检查项目结构是否规范
   - 检查是否有足够的代码注释
   - 可以手动补充文档内容

### 日志查看

技能执行的日志可以在以下位置查看：
- **技能日志**: `${SKILL_DIR}/logs/agent.log`
- **Trae IDE 日志**: Trae IDE 的 "日志" 面板

## 版本历史

### v1.0.0
- 初始版本
- 支持项目结构扫描
- 支持技术栈识别
- 支持核心模块分析
- 支持文档生成和存储
- 支持元数据管理

## 贡献指南

欢迎贡献代码和改进建议！请按照以下步骤进行：

1. Fork 项目
2. 创建功能分支
3. 提交更改
4. 推送到分支
5. 打开 Pull Request

## 许可证

MIT License

## 联系方式

如有问题或建议，请联系：
- 邮箱: support@trae.io
- GitHub: https://github.com/trae-io/project-analyzer-skill