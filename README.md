# P System - 权限管理系统

Permission Management System with Ant Design

## 🌐 本地访问地址

```
http://localhost:8006/
```

## 📋 系统功能

基于Ant Design的完整权限管理系统，支持多角色分组管理和灵活的权限控制。

---

## ✨ 核心功能

### 1️⃣ 员工信息管理

**Employee列**
- 员工头像 + 姓名
- CTW标签展示
- 固定在左侧，方便浏览

**Information列（可编辑）**
- 📌 **部门**：可点击编辑
- 📌 **职位**：可点击编辑
- 📌 **项目**：显示项目信息
- 📌 **组**：显示组信息
- 📌 **小队**：显示小队信息

点击任意信息字段即可快速编辑！

---

### 2️⃣ 角色权限管理（4大分组）

#### 🔵 **基础角色**（8个）
| 角色 | 说明 |
|------|------|
| CEO | 首席执行官 |
| Executive | 高管 |
| Department Manager | 部门经理 |
| Group Manager | 组经理 |
| Team Leader | 团队领导 |
| Interviewer | 面试官 |
| Global HR | 全球人力资源 |
| HR | 人力资源 |

#### 🟣 **CP角色**（5个）
| 角色 | 说明 |
|------|------|
| CP Manager | CP经理 |
| CP Dev | CP开发 |
| CP Operation | CP运营 |
| CP Monitor | CP监控 |
| A Manager | A经理 |

#### 🟢 **IP角色**（1个）
| 角色 | 说明 |
|------|------|
| IP Manager | IP经理 |

#### 🟡 **Expert角色**（18个）
包含6大领域的Evaluator（评估者）和Responder（响应者）：

**Tech Expert**（技术专家）
- Tech Expert Evaluator
- Tech Expert Responder

**Creative Expert**（创意专家）
- Creative Expert Evaluator
- Creative Expert Responder

**Marketing Expert**（营销专家）
- Marketing Expert Evaluator
- Marketing Expert Responder

**Operation Expert**（运营专家）
- Operation Expert Evaluator
- Operation Expert Responder

**Management Expert**（管理专家）
- Management Expert Evaluator
- Management Expert Responder

**CP Expert**（CP专家）
- CP Expert Evaluator
- CP Expert Responder

**Executive Expert**（执行专家）
- Executive Expert Evaluator
- Executive Expert Responder

**CS Expert**（客服专家）
- CS Expert Evaluator
- CS Expert Responder

**i18n Expert**（国际化专家）
- i18n Expert Evaluator
- i18n Expert Responder

---

### 3️⃣ 角色分组折叠功能

每个角色组都可以**折叠/展开**，方便管理：

```
🔽 基础角色 (8)     ← 点击折叠
🔽 CP角色 (5)       ← 点击折叠
🔽 IP角色 (1)       ← 点击折叠
🔽 Expert角色 (18)  ← 点击折叠
```

折叠后隐藏该组所有列，展开后显示所有列。

---

### 4️⃣ 搜索和筛选

**多维度筛选**：
- 🔍 姓名搜索
- 📋 员工类型
- 💼 职位筛选
- 🏢 部门筛选
- 📊 项目筛选
- 🎭 角色搜索

---

### 5️⃣ 权限开关

每个角色权限都使用**Switch开关**控制：
- ✅ **蓝色**：已启用
- ⚪ **灰色**：未启用
- 点击即可切换状态
- 自动保存并提示

---

### 6️⃣ 统计仪表盘

顶部显示3个关键指标：

| 指标 | 说明 |
|------|------|
| **总员工数** | 系统中的员工总数 |
| **已分配角色** | 已激活的角色权限总数 |
| **角色类型** | 可分配的角色类型总数（32个）|

---

## 🎨 界面特点

### ✅ **完全基于Ant Design**
- 使用Ant Design组件库
- 专业的企业级UI设计
- 响应式布局

### ✅ **左侧导航菜单**
- 员工管理
- 薪酬管理
  - 候选人
  - 合作方
- 设置
  - 团队和项目
  - AOT设置
  - 模版管理
  - **权限管理** ⭐（当前页面）
  - 角色管理

### ✅ **表格功能**
- 固定左侧列（Employee + Information）
- 水平滚动查看所有角色
- 分组列头（可折叠）
- 分页显示
- 排序功能
- 快速编辑

### ✅ **交互体验**
- 实时更新
- 操作提示
- 悬停效果
- 流畅动画

---

## 🔧 技术栈

| 技术 | 版本 | 说明 |
|------|------|------|
| React | 18.2.0 | 前端框架 |
| Ant Design | 5.12.0 | UI组件库 |
| Ant Design Icons | 5.2.6 | 图标库 |
| Babel Standalone | 7.23.0 | JSX转换 |

**架构**：纯前端实现，使用CDN加载所有依赖

---

## 📊 数据结构

### 员工对象示例

```javascript
{
  key: '1',
  name: '佐々木龍一',
  nameEn: 'Sasaki Ryuichi',
  avatar: '佐',
  tag: 'ctw',
  department: 'tech',      // 可编辑
  position: 'be',          // 可编辑
  project: '-',
  group: '-',
  team: '-',
  
  // 基础角色 (8个)
  ceo: false,
  executive: false,
  deptManager: true,
  groupManager: true,
  teamLeader: false,
  interviewer: true,
  globalHR: false,
  hr: false,
  
  // CP角色 (5个)
  cpManager: false,
  cpDev: false,
  cpOperation: false,
  cpMonitor: false,
  aManager: false,
  
  // IP角色 (1个)
  ipManager: false,
  
  // Expert角色 (18个)
  techExpertEvaluator: false,
  techExpertResponder: false,
  // ... 更多expert角色
}
```

---

## 🎯 使用说明

### 启动服务
```bash
cd /Users/ctw/Desktop/permission-management-system
python3 -m http.server 8006
```

### 访问页面
在浏览器打开：`http://localhost:8006/`

### 操作指南

#### 1. **查看员工权限**
- 左右滚动表格查看所有角色
- 蓝色开关表示已启用权限

#### 2. **编辑员工信息**
- 点击Information列中的部门或职位标签
- 在弹窗中输入新值
- 按Enter键保存

#### 3. **修改权限**
- 点击任意Switch开关
- 自动保存并显示成功提示

#### 4. **折叠角色组**
- 点击角色组标题（如"基础角色 (8)"）
- 该组所有列将被隐藏/显示

#### 5. **搜索筛选**
- 在顶部搜索栏输入条件
- 表格自动过滤显示结果

#### 6. **菜单导航**
- 点击左侧菜单可切换页面
- 当前在"权限管理"页面

---

## 📊 角色统计

| 分组 | 角色数量 |
|------|---------|
| 基础角色 | 8 |
| CP角色 | 5 |
| IP角色 | 1 |
| Expert角色 | 18 |
| **总计** | **32** |

---

## 🎨 设计亮点

### ✨ **简洁操作**
- Switch开关一键切换
- 点击即可编辑信息
- 分组折叠减少视觉负担

### ✨ **信息密度适中**
- 每列内容清晰可读
- 合理的列宽分配
- 舒适的行高间距

### ✨ **响应式设计**
- 固定列保持可见
- 横向滚动查看更多
- 自适应不同屏幕

### ✨ **专业美观**
- 渐变色统计卡片
- 统一的配色方案
- Ant Design设计语言

---

## 💡 后续扩展

实际生产环境可对接：
- 后端API持久化权限数据
- 批量权限分配
- 权限模板管理
- 操作日志记录
- 权限审计报告
- 角色继承机制
- 权限有效期管理

---

## 📂 项目位置

```
/Users/ctw/Desktop/permission-management-system/
```

---

## 🚀 特色功能

✅ **32种角色类型**  
✅ **分组折叠管理**  
✅ **实时编辑保存**  
✅ **多维度筛选**  
✅ **统计仪表盘**  
✅ **Ant Design UI**  
✅ **响应式表格**  
✅ **固定列滚动**  

---

**创建时间**：2025.10.24  
**版本**：v1.0  
**技术栈**：React + Ant Design  
**语言**：简体中文

