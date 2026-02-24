# 技术栈检测器配置

## 检测规则定义

技术栈检测通过以下方式进行：
1. **依赖文件识别**: 检查特定的依赖文件
2. **技术特征匹配**: 分析代码和配置文件中的技术特征
3. **配置文件分析**: 检查特定的配置文件

## 前端技术栈

### React
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: react, react-dom
  - 配置: .babelrc, webpack.config.js
  - 代码特征: import React from 'react'

### Vue
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: vue
  - 配置: vue.config.js
  - 代码特征: import Vue from 'vue'

### Angular
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: @angular/core
  - 配置: angular.json
  - 代码特征: import { Component } from '@angular/core'

### Svelte
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: svelte
  - 配置: svelte.config.js
  - 代码特征: <script>标签在.svelte文件中

### Next.js
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: next
  - 配置: next.config.js
  - 目录结构: pages/, public/

### Nuxt.js
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: nuxt
  - 配置: nuxt.config.js
  - 目录结构: pages/, static/

### Vite
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: vite
  - 配置: vite.config.js
  - 代码特征: import { defineConfig } from 'vite'

### Webpack
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: webpack
  - 配置: webpack.config.js
  - 代码特征: module.exports = {

### Babel
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: @babel/core
  - 配置: .babelrc
  - 代码特征: presets: [

## 后端技术栈

### Node.js
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: express, koa, nestjs
  - 配置: server.js, app.js
  - 代码特征: const express = require('express')

### Python
- **依赖文件**: requirements.txt, setup.py, pyproject.toml
- **特征匹配**:
  - 依赖: django, flask, fastapi
  - 配置: manage.py
  - 代码特征: import django

### Java
- **依赖文件**: pom.xml, build.gradle
- **特征匹配**:
  - 依赖: spring-boot-starter
  - 配置: application.properties
  - 代码特征: public class

### Go
- **依赖文件**: go.mod
- **特征匹配**:
  - 依赖: github.com/gin-gonic/gin
  - 配置: main.go
  - 代码特征: package main

### Ruby
- **依赖文件**: Gemfile
- **特征匹配**:
  - 依赖: rails
  - 配置: config.ru
  - 代码特征: require 'rails'

### PHP
- **依赖文件**: composer.json
- **特征匹配**:
  - 依赖: laravel/framework
  - 配置: index.php
  - 代码特征: <?php

### NestJS
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: @nestjs/core
  - 配置: main.ts
  - 代码特征: import { NestFactory } from '@nestjs/core'

### Express
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: express
  - 配置: app.js
  - 代码特征: const app = express()

### Koa
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: koa
  - 配置: app.js
  - 代码特征: const Koa = require('koa')

## 数据库技术栈

### MySQL
- **依赖文件**: package.json, requirements.txt
- **特征匹配**:
  - 依赖: mysql, mysql2
  - 配置: database.js
  - 代码特征: mysql://

### PostgreSQL
- **依赖文件**: package.json, requirements.txt
- **特征匹配**:
  - 依赖: pg, postgresql
  - 配置: database.js
  - 代码特征: postgresql://

### MongoDB
- **依赖文件**: package.json, requirements.txt
- **特征匹配**:
  - 依赖: mongodb, mongoose
  - 配置: database.js
  - 代码特征: mongoose.connect

### Redis
- **依赖文件**: package.json, requirements.txt
- **特征匹配**:
  - 依赖: redis
  - 配置: redis.js
  - 代码特征: redis.createClient

### SQLite
- **依赖文件**: package.json, requirements.txt
- **特征匹配**:
  - 依赖: sqlite3
  - 配置: database.js
  - 代码特征: sqlite://

## 工具链

### Docker
- **依赖文件**: Dockerfile, docker-compose.yml
- **特征匹配**:
  - 配置: Dockerfile
  - 代码特征: FROM node:alpine

### Kubernetes
- **依赖文件**: deployment.yaml, service.yaml
- **特征匹配**:
  - 配置: deployment.yaml
  - 代码特征: apiVersion: apps/v1

### Git
- **依赖文件**: .gitignore, .git
- **特征匹配**:
  - 配置: .gitignore
  - 目录结构: .git/

### ESLint
- **依赖文件**: package.json, .eslintrc
- **特征匹配**:
  - 依赖: eslint
  - 配置: .eslintrc
  - 代码特征: extends: ['eslint:recommended']

### Prettier
- **依赖文件**: package.json, .prettierrc
- **特征匹配**:
  - 依赖: prettier
  - 配置: .prettierrc
  - 代码特征: "semi": false

### Jest
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: jest
  - 配置: jest.config.js
  - 代码特征: test('should', () => {

### Mocha
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: mocha
  - 配置: mocha.opts
  - 代码特征: describe('test', () => {

## 部署技术栈

### AWS
- **依赖文件**: serverless.yml, cloudformation.yml
- **特征匹配**:
  - 配置: serverless.yml
  - 代码特征: provider: aws

### GCP
- **依赖文件**: app.yaml
- **特征匹配**:
  - 配置: app.yaml
  - 代码特征: runtime: nodejs14

### Azure
- **依赖文件**: azure-pipelines.yml
- **特征匹配**:
  - 配置: azure-pipelines.yml
  - 代码特征: pool: vmImage: 'ubuntu-latest'

### Heroku
- **依赖文件**: Procfile
- **特征匹配**:
  - 配置: Procfile
  - 代码特征: web: node app.js

## 移动应用技术栈

### React Native
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: react-native
  - 配置: metro.config.js
  - 代码特征: import { View } from 'react-native'

### Flutter
- **依赖文件**: pubspec.yaml
- **特征匹配**:
  - 依赖: flutter
  - 配置: pubspec.yaml
  - 代码特征: import 'package:flutter/material.dart'

### Ionic
- **依赖文件**: package.json
- **特征匹配**:
  - 依赖: @ionic/react, @ionic/angular
  - 配置: ionic.config.json
  - 代码特征: import { IonApp } from '@ionic/react'

## 检测优先级

技术栈检测的优先级如下：
1. **依赖文件检测** (最高优先级)
2. **配置文件检测**
3. **代码特征检测**
4. **目录结构检测** (最低优先级)

## 检测阈值

- **依赖文件**: 至少检测到1个依赖文件
- **技术特征**: 至少检测到2个技术特征
- **配置文件**: 至少检测到1个配置文件

## 忽略规则

以下目录和文件在检测时会被忽略：
- node_modules/
- .git/
- dist/
- build/
- .trae/
- *.log
- *.tmp
- *.temp