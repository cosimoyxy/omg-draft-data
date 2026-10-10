# OMG Draft 数据库

这是 OMG Draft Helper 的公开离线数据库发布仓库。仓库本身只保存更新清单和维护说明；数据库文件通过 [GitHub Releases](https://github.com/cosimoyxy/omg-draft-data/releases) 发布，避免二进制文件的历史版本持续增大 Git 仓库。

## 给软件用户

请在 OMG Draft Helper 的“数据更新”页面点击“检查并下载更新”。软件只会在用户主动点击时访问本仓库，不会在后台轮询，也不会直接访问 Windrun。

下载完成后，软件会检查文件大小、SHA-256、SQLite 完整性、数据格式和逐抓位覆盖率。校验通过的数据库会在下次启动软件时安装；更新失败不会破坏当前可用数据库。

## 当前数据

- Dota 2 版本：7.41f
- 数据库版本：7.41f-20261009.1
- 数据库能力格式：2
- 普通段与高分段基础统计：各640条
- 组合胜率：10,000条
- 近战／远程统计：1,280条
- 六个时间段统计：3,840条
- 英雄统计：127条
- 完整逐抓位技能：513个
- 逐抓位记录：25,650条（每个技能覆盖1～50手）
- 数据源更新时间：2026-10-09 18:15:52（Asia/Shanghai）

机器可读的当前版本信息位于 [`manifest.json`](./manifest.json)。数据库本体和SHA-256校验文件见
[本次Release](https://github.com/cosimoyxy/omg-draft-data/releases/tag/data-7.41f-20261009.1)。

概览与技能详情是限频抓取的不同时间快照。338项详情与概览存在快照差异，保留来源标识和
Beta处理，不宣称严格同快照统计。实际抓取时间与发布时间分别记录，不以上传时间冒充数据更新时间。

## 数据来源与使用说明

统计数据整理自 [Windrun](https://windrun.io/)。本仓库不是 Windrun 官方仓库，也不会由普通客户端请求 Windrun API。数据仅用于 Dota 2 Ability Draft 辅助分析；Dota、Dota 2 及相关素材商标归 Valve Corporation 所有。

本仓库不为数据库内容授予额外许可。转载、镜像或其他用途应同时遵守原始数据来源的条款。
