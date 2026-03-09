# 乘法口诀实时答题挑战 🎯

一个面向小学二年级学生的乘法口诀答题挑战应用。

## ✨ 功能特性

- 🎮 **趣味答题**: 10 道随机乘法口诀题
- ⏱️ **实时计时**: 总计时 + 单题计时，精确到十分位
- 🏆 **实时排行榜**: 正确率优先，用时次之
- 📊 **详细成绩**: 答题详情、用时统计、排名信息
- 📱 **响应式设计**: 支持桌面和移动设备
- 🔒 **公平机制**: 每人只能答题一次

## 🛠️ 技术栈

- **前端**: HTML + Tailwind CSS (CDN)
- **后端**: Supabase (PostgreSQL)
- **部署**: Supabase Storage

## 📦 项目结构

```
乘法/
├── index.html              # 主应用文件
├── database/
│   └── init.sql           # 数据库初始化脚本
├── docs/
│   └── 部署指南.md        # 详细部署文档
└── README.md              # 项目说明
```

## 🚀 快速开始

### 1. 创建 Supabase 项目

访问 [supabase.com](https://supabase.com) 创建新项目

### 2. 初始化数据库

在 Supabase SQL Editor 中执行 `database/init.sql`

### 3. 配置应用

编辑 `index.html`，替换 Supabase 配置：

```javascript
const SUPABASE_URL = "你的项目URL";
const SUPABASE_ANON_KEY = "你的anon key";
```

### 4. 部署

上传 `index.html` 到 Supabase Storage 或其他静态托管平台

详细步骤请查看 [部署指南](docs/部署指南.md)

## 📖 使用说明

### 学生端

1. 输入姓名开始答题
2. 回答 10 道乘法口诀题
3. 查看成绩和排名

### 教师端

- 查看排行榜
- 导出成绩数据
- 重置学生记录

详细说明请查看 [部署指南](docs/部署指南.md)

## 🎯 答题规则

- 题目范围: 1×1 到 9×9
- 题目数量: 10 道
- 题目形式: 填空题
- 答题机会: 每人一次
- 排名规则: 正确率优先，用时次之

## 📊 数据库设计

- `users`: 用户信息表
- `quiz_records`: 答题记录表
- `answer_details`: 答题详情表
- `leaderboard_view`: 排行榜视图

## 🔧 自定义配置

### 修改题目数量

修改 `index.html` 中的 `generateQuestions()` 函数

### 修改题目范围

修改 `generateQuestions()` 函数中的循环范围

### 添加班级功能

1. 修改数据库表结构
2. 更新前端表单
3. 调整排行榜逻辑

## 📝 开发计划

- [ ] 添加班级管理功能
- [ ] 添加教师管理后台
- [ ] 支持多种题目类型
- [ ] 添加错题本功能
- [ ] 支持自定义题目数量
- [ ] 添加成就系统

## 📄 许可证

MIT License

## 👨‍💻 作者

开发于 2026 年 3 月

---

**注意**: 本项目仅供教育用途，请勿用于商业场景。
