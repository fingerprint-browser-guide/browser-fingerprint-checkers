# 工具字段速查

| 字段组 | BrowserLeaks | CreepJS | Cover Your Tracks | AmIUnique | FingerprintJS | BrowserScan | Pixelscan | IPhey |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| IP / ASN / 地理位置 | ● | ○ | ○ | ○ | — | ● | ● | ● |
| DNS / WebRTC 泄漏 | ● | ○ | — | — | — | ● | ● | ● |
| HTTP / Client Hints | ● | ○ | ● | ● | ○ | ● | ● | ○ |
| HTTP/2 / TLS | ● | — | — | — | — | ● | ○ | ○ |
| Canvas / WebGL | ● | ● | ● | ● | ● | ● | ● | ● |
| Audio / 字体 | ● | ● | ○ | ● | ● | ● | ● | ● |
| 原型篡改 / lies | ○ | ● | — | ○ | — | ○ | ○ | ○ |
| WebDriver / CDP / Bot | ○ | ● | — | ○ | — | ● | ● | ● |
| 样本唯一性 | ○ | ○ | ● | ● | — | ○ | ○ | ○ |
| 时间线 / visitor ID 稳定 | — | ○ | ○ | ● | ● | — | ○ | ○ |
| 跟踪器阻断 | — | — | ● | — | — | — | — | — |

说明：● 为主要或明确公开能力，○ 为相关字段或辅助能力，— 表示不建议把该工具作为该维度的主要依据。表格根据 2026-07-22 的官方公开资料整理，不代表完整实现清单。

## 使用建议

- 排查泄漏：BrowserLeaks 为主，综合面板为交叉检查。
- 排查浏览器修改副作用：CreepJS 为主，检查具体 API 而不是总分。
- 研究唯一性：Cover Your Tracks 与 AmIUnique，先读数据采集说明。
- 研究客户端 ID：FingerprintJS Demo，只比较同一库、同一版本。
- 排查自动化暴露：至少两个综合面板，加具体 WebDriver/CDP 字段。

