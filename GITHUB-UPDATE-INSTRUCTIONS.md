# GitHub 更新说明

当前 ChatGPT 连接到 GitHub 的账号没有此仓库的 push 权限，因此本次没有直接修改远程仓库。

## 建议替换/新增

请用本包中的文件覆盖仓库对应文件：

- `README.md`
- `METHODOLOGY.md`
- `SOURCES.md`
- `data/tools.csv`
- `data/test-dimensions.csv`

新增：

- `CHANGELOG.md`
- `IMAGE-MAP.md`
- `assets/browser-fingerprint-checkers-2026-cover.png`

## 旧内容处理

旧 README、METHODOLOGY 和 CSV 都是 8 工具版，不能只更新 README 而保留旧数据。

现有其他资产图片可以先保留；确认不再被 README 或 Pages 引用后再删除，避免误删仍有外链的资源。

## 30 张官网截图

建议统一上传到：

`assets/screenshots/`

命名与 Alt/Caption 见 `IMAGE-MAP.md`。

README 当前没有提前引用这些截图，因此即使暂时不上传也不会出现 404 图片。

## WordPress 原文

已确认原文地址：

https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86

新版 `README.md` 已在顶部和底部加入该原文链接。

## V3 结构调整

README 已改为精简 GitHub Edition，不再复制 WordPress 完整正文。
WordPress 负责完整网站介绍、截图和详细说明；GitHub 负责目录、状态、数据、来源和更新记录。

## V4 README

当前推荐 README 为 Resource Directory 结构：
Quick comparison → Tools by category → Data & methodology → Notes → Full article。

不要恢复 30 次重复的“官网 / 完整介绍”链接；工具标题本身即为官网链接。
