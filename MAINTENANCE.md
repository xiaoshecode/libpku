# libpku 维护说明

北京大学课程资料索引和历史静态目录生成脚本。

- 上游：https://github.com/lib-pku/libpku
- 在线文档：https://xiaoshecode.github.io/xiaoshecode/repos/libpku/
- 检查日期：2026-10-30

## 环境与使用

- 推荐在线浏览；如需克隆可使用 git clone --depth 1 --filter=blob:none --sparse。

使用/检查入口（需先满足依赖条件）：

- `按课程目录阅读资料；index.js 是历史站点生成器。`

## 目录职责

- README.md — 使用和贡献约定
- 专业课/ / 通选课/ / 英语课/ — 分类资料
- index.js — 旧版 Node 目录生成器

## 本次整理

- 新增维护文档和在线文档入口，补全用途、目录、使用路径及验证边界。

## 检查记录

- **仓库目录与入口盘点**（passed）：检查 Git 索引中的 960 个路径、README 和项目配置；不等于功能验收。
- **JavaScript syntax**（passed）：1 个文件通过解析；不导入依赖、不执行应用。
- **完整构建与端到端运行**（not_run）：为避免下载大量附件仅稀疏检出根目录；附件未逐一读取。index.js 依赖 directory-tree/remark 等但缺 package.json，不声称站点可重复构建。

## 验证边界与待办

- 为避免下载大量附件仅稀疏检出根目录；附件未逐一读取。index.js 依赖 directory-tree/remark 等但缺 package.json，不声称站点可重复构建。

## 后续维护约定

保留上游许可证与作者信息。沿用现有模块边界和格式配置；修复功能时同步最小回归验证。依赖或接口变更需写明迁移步骤，避免仅为目录美观搬动公开入口。
