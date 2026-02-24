# 项目分析模板

## 1. 项目概述

### 1.1 基本信息

- **项目名称**: {{projectName}}
- **项目路径**: {{projectPath}}
- **创建时间**: {{createTime}}
- **最后修改时间**: {{lastModifiedTime}}

### 1.2 技术栈

{{#each techStack}}
- **{{category}}**: {{#each items}}{{name}}{{#unless @last}}, {{/unless}}{{/each}}
{{/each}}

### 1.3 项目结构

```
{{projectTree}}
```

### 1.4 主要功能

{{#each mainFeatures}}
- {{this}}
{{/each}}

## 2. 快速开始

### 2.1 环境要求

{{#each environmentRequirements}}
- {{this}}
{{/each}}

### 2.2 安装步骤

{{#each installationSteps}}
{{@index}}. {{this}}
{{/each}}

### 2.3 运行方法

{{#each runSteps}}
{{@index}}. {{this}}
{{/each}}

### 2.4 开发环境搭建

{{#each devSetupSteps}}
{{@index}}. {{this}}
{{/each}}

## 3. 架构设计

### 3.1 系统架构

```mermaid
{{systemArchitectureDiagram}}
```

### 3.2 模块关系

```mermaid
{{moduleRelationshipDiagram}}
```

### 3.3 数据流

```mermaid
{{dataFlowDiagram}}
```

### 3.4 核心流程

```mermaid
{{coreProcessDiagram}}
```

## 4. 核心模块

{{#each coreModules}}
### 4.{{@index}} {{name}}

#### 4.{{@index}}.1 模块描述

{{description}}

#### 4.{{@index}}.2 主要功能

{{#each features}}
- {{this}}
{{/each}}

#### 4.{{@index}}.3 关键文件

{{#each keyFiles}}
- {{this}}
{{/each}}

#### 4.{{@index}}.4 依赖关系

{{#each dependencies}}
- {{this}}
{{/each}}

{{/each}}

## 5. API参考

{{#each apis}}
### 5.{{@index}} {{name}}

#### 5.{{@index}}.1 API描述

{{description}}

#### 5.{{@index}}.2 请求参数

| 参数名 | 类型 | 必填 | 描述 | 默认值 |
|--------|------|------|------|--------|
{{#each parameters}}
| {{name}} | {{type}} | {{required}} | {{description}} | {{default}} |
{{/each}}

#### 5.{{@index}}.3 返回值

| 字段名 | 类型 | 描述 |
|--------|------|------|
{{#each returnValues}}
| {{name}} | {{type}} | {{description}} |
{{/each}}

#### 5.{{@index}}.4 示例

```
{{example}}
```

{{/each}}

## 6. 数据库模型

{{#each databaseModels}}
### 6.{{@index}} {{name}}

#### 6.{{@index}}.1 表结构

| 字段名 | 数据类型 | 约束 | 描述 |
|--------|----------|------|------|
{{#each fields}}
| {{name}} | {{type}} | {{constraints}} | {{description}} |
{{/each}}

#### 6.{{@index}}.2 关系

{{#each relationships}}
- {{this}}
{{/each}}

{{/each}}

## 7. 开发指南

### 7.1 编码规范

{{#each codingStandards}}
- {{this}}
{{/each}}

### 7.2 开发流程

{{#each devProcess}}
{{@index}}. {{this}}
{{/each}}

### 7.3 部署说明

{{#each deploymentSteps}}
{{@index}}. {{this}}
{{/each}}

### 7.4 常见问题

{{#each commonIssues}}
#### 7.4.{{@index}} {{title}}

{{description}}

**解决方案**: {{solution}}

{{/each}}

## 8. 附录

### 8.1 依赖项

{{#each dependencies}}
- {{name}}: {{version}}
{{/each}}

### 8.2 配置文件

{{#each configFiles}}
- {{name}}: {{path}}
{{/each}}

### 8.3 外部资源

{{#each externalResources}}
- {{name}}: {{url}}
{{/each}}

### 8.4 版本历史

{{#each versionHistory}}
- **{{version}}**: {{date}} - {{changes}}
{{/each}}