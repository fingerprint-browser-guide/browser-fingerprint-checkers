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

README 顶部和底部预留了原文位置。WordPress 正式 URL 确定后，再补上原文链接即可。
