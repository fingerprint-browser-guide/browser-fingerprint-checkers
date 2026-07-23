# 来源账本

最后核查日期：2026-07-22。优先列出官方页面、官方代码仓库和研究项目来源。

## BrowserLeaks

- 官网与工具总览：https://browserleaks.com/
- WebRTC Leak Test：https://browserleaks.com/webrtc
- Canvas Fingerprinting：https://browserleaks.com/canvas
- WebGL Report：https://browserleaks.com/webgl
- TLS Client Test：https://browserleaks.com/tls
- Features Detection：https://browserleaks.com/features

支持的主要结论：模块化检查 IP、WebRTC、Canvas、WebGL、字体、地理位置、TLS/HTTP2 等；Canvas 页面公开固定绘制与签名生成说明；官网声明不存储用户指纹，但某些 API 可能访问第三方。

## CreepJS

- 官方线上部署：https://abrahamjuliot.github.io/creepjs/
- 官方源代码：https://github.com/abrahamjuliot/creepjs

支持的主要结论：研究与教育项目；检查 JavaScript 篡改、原型谎言、渲染、GPU、字体、Audio、DOMRect、时区和其他高熵信号；官方仓库明确它不是通用指纹库。

## Cover Your Tracks

- 测试页：https://coveryourtracks.eff.org/
- Learn：https://coveryourtracks.eff.org/learn
- 结果解释：https://coveryourtracks.eff.org/results-nojs
- 隐私政策：https://coveryourtracks.eff.org/privacy
- 官方源代码：https://github.com/EFForg/cover-your-tracks
- EFF 项目页：https://www.eff.org/pages/cover-your-tracks

支持的主要结论：检查部分跟踪器保护与指纹独特性；结果基于近期数据集；不覆盖所有跟踪方式；3 个月 cookie；对 IP 计算会定期换密钥的 HMAC；AGPL-3.0 源码公开。

## AmIUnique

- 官网：https://amiunique.org/
- 指纹结果页：https://amiunique.org/fingerprint
- 隐私政策：https://amiunique.org/privacy-policy
- 公开源码：https://github.com/DIVERSIFY-project/amiunique
- 研究论文预印本：https://arxiv.org/abs/2006.09511

支持的主要结论：研究浏览器指纹多样性、相似比例与时间变化；公开详细采集字段；使用 4 个月 cookie 并记录 IP 与时间戳；旧版网站源码公开。

## FingerprintJS / Fingerprint

- FingerprintJS 官方仓库：https://github.com/fingerprintjs/fingerprintjs
- 开源 Demo：https://fingerprintjs.github.io/fingerprintjs/
- 开源 API 文档：https://github.com/fingerprintjs/fingerprintjs/blob/master/docs/api.md
- 商业平台介绍：https://docs.fingerprint.com/docs/introduction
- Identify visitors：https://docs.fingerprint.com/docs/identify-visitors

支持的主要结论：开源客户端库从浏览器组件生成 visitor ID 与 confidence；客户端处理存在准确性与被欺骗限制；商业 Identification 平台是闭源服务，并加入服务端与网络信号。两者不可混为一个工具。

## BrowserScan

- 官网：https://www.browserscan.net/
- 官方使用指南：https://blog.browserscan.net/docs/how-to-use-browserscan
- TLS/HTTP2：https://www.browserscan.net/tls
- Bot Detection：https://www.browserscan.net/bot-detection
- 隐私政策：https://www.browserscan.net/privacy-policy

支持的主要结论：检查 IP、WebRTC、地理位置、浏览器、硬件、Canvas、WebGL、TLS/HTTP2、WebDriver、CDP 与 Navigator；隐私政策说明 IP、日志与使用数据处理。综合“真实性”权重和误报率未得到同等程度公开。

## Pixelscan

- 指纹检查：https://pixelscan.net/fingerprint
- Bot Check：https://pixelscan.net/bot-check
- About / Manifest：https://pixelscan.net/manifest
- 隐私政策：https://pixelscan.net/privacy-policy

支持的主要结论：检查浏览器、位置、代理、指纹、Bot、屏幕、字体、UA、Canvas、WebGL、Audio 等；官网有“Zero Data Stored”表述，但隐私政策写明存储浏览器指纹和 IP，并可能分享不含 IP 的匿名结果。算法权重和误报率有限公开。

## IPhey

- 官网与检测页：https://iphey.com/
- 官方浏览器指纹说明：https://iphey.com/blog/what-is-a-browser-fingerprint/

支持的主要结论：提供指纹、IP、VPN/代理、Bot、DNS 泄漏、黑名单与 Trust Score 相关说明；公开列出 UA、Canvas、WebRTC、AudioContext、字体和插件等字段。首版未定位到足以说明检测数据保留规则的完整官方隐私文档。

## 通用研究边界

- EFF 关于单独伪装 User-Agent 可能增加唯一性的说明：https://coveryourtracks.eff.org/learn
- 浏览器指纹用于认证的大规模研究：https://arxiv.org/abs/2006.09511
- 针对指纹系统的定向伪装研究：https://arxiv.org/abs/2110.10129

这些研究用于解释“唯一性、稳定性和可欺骗性是不同问题”，不用于给任何在线检测器背书。

