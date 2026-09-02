# 选课排课表（国科大专属）

> 基于浏览器本地运行的大学生选课排课工具，自动检测课程时间冲突，彻底告别选课时间撞车。

![License](https://img.shields.io/badge/license-CC%20BY--NC%204.0-orange)
![Language](https://img.shields.io/badge/language-HTML%2FCSS%2FJavaScript-blue)
![Platform](https://img.shields.io/badge/platform-Browser-lightgrey)
![Dependencies](https://img.shields.io/badge/dependencies-0-green)
![Offline](https://img.shields.io/badge/offline-supported-success)
![Data](https://img.shields.io/badge/data-localStorage-yellow)
[![WeChat](https://img.shields.io/badge/微信公众号-程序喵有话说-brightgreen)](Contact%20the%20author.md)
[![Bilibili](https://img.shields.io/badge/B站-程序喵有话说-ff69b4)](https://space.bilibili.com/1029501219)

## 项目简介

选课排课表是一款纯前端、零依赖的排课工具：以学校课表（13 节课/天 × 周一至周日 × 20 周）为底版，核心能力是**自动冲突检测**——同一星期、同一节次、周次重叠即视为时间冲突，冲突课程无法排入课表、只能放入候选区，从根源上避免选课撞车。

- 🗓️ 13 节课 / 天，周一至周日，共 20 周（第 1 周 2026-08-31 起算，各周日期自动计算）
- ⚡ 添加课程时自动校验冲突；编辑已排课程产生冲突时自动打回候选区
- 📋 候选区集中管理未排入课表的课程，冲突角标与原因一目了然
- 🏷️ 8 大课程分类 + 专业学位课金色徽章重点显示
- 🖼️ 课表字号可调（12-24px）；课程名过长自动换行
- 📤 三种导出：JSON 备份 / Excel 总表 / 各周课表图片（所见即所得 PNG）
- 🔒 数据全部保存在浏览器 localStorage，不上传任何服务器

## 使用说明

### 快速开始

1. 下载或克隆本仓库
2. 用浏览器（推荐 Chrome / Edge）直接打开 `index.html`
3. 首次打开内置示例数据（含一门冲突示例），可在右上角「清空」后录入自己的课程

### 操作步骤

1. **添加课程**：点击「＋ 添加课程」，填写课程名、教师、类别、教室，并设置上课时间
   - 节次可多选（表示连堂）；周次支持点选 20 周或快捷输入 `1-8,10,12-16`
2. **自动校验**：保存时自动检查是否与已排课程时间冲突
   - 无冲突 → 直接排入课表
   - 有冲突 → 只能保存到候选区，并明确列出与哪门课、哪个时段冲突
3. **周次浏览**：顶部周次导航条可切换第 1-20 周；勾选「显示全部周的课」查看全量
4. **候选区管理**：候选区课程可「编辑」补全时间后重新排入课表，或「删除」
5. **已排课程**：点击课表条目可编辑；悬停可「打回候选区」或「删除」

### 导出功能

点击右上角「导出」，支持三种方式：

| 方式 | 用途 |
| --- | --- |
| JSON 数据文件 | 完整备份全部课程数据，供「导入」恢复 |
| Excel 总表 | 所有课程排课一览（含类别、教师、教室、状态），便于归档共享 |
| 各周课表图片 | 所见即所得的周课表 PNG（与网页样式完全一致），可选周次，打包 zip |

## 目录结构

| 文件 | 说明 |
| --- | --- |
| `index.html` | 单文件应用（HTML + CSS + JS），零依赖、可离线使用 |
| `LICENSE` | 授权协议（CC BY-NC 4.0 + 作者补充条款） |
| `README.md` | 本说明文件 |
| `author-wx.png` | 作者微信二维码 |
| `Contact the author.md` | 联系方式与授权联系 |

## 技术要点

- 纯原生 HTML / CSS / JavaScript 实现，无任何第三方依赖
- 数据持久化：浏览器 localStorage
- 导出图片：克隆真实课表 DOM + 逐元素内联计算样式 + SVG foreignObject 渲染，所见即所得
- Excel 生成：自研 xlsx（zip + XML）写入器

## 授权

本项目采用 **CC BY-NC 4.0**（知识共享 署名-非商业使用 4.0 国际版）授权，并附有作者补充条款：

- **不可商用**：禁止任何形式的商业用途
- **转发需授权**：取得作者明确授权后方可转发、分享本软件
- **转发须保留**：授权转发时必须完整保留 LICENSE 全文并注明出处

详细条款见 [LICENSE](LICENSE)。如需授权或合作，见 [联系作者](Contact%20the%20author.md)。

## 联系作者

**微信公众号：程序喵有话说**

![author-wx](author-wx.png)

**B站**：程序喵有话说（[点击访问空间](https://space.bilibili.com/1029501219)）

**QQ**：2976377647　**邮箱**：2976377647@qq.com

完整联系方式见 [Contact the author.md](Contact%20the%20author.md)。
