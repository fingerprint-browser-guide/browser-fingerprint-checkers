# 2026年30款浏览器指纹检测与分析工具

> **最后核查：2026-08-09**  
> **完整原文：** [https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)  
> GitHub Edition 用于维护工具目录、状态、检测方向、结构化数据和更新记录；完整网站介绍、截图与详细说明请查看 Web4 Browser 原文。

![2026年30款浏览器指纹检测与分析工具汇总封面](assets/browser-fingerprint-checkers-2026-cover.png)

## 这个仓库收录什么

这里整理的 30 款工具并不都是传统 Canvas/WebGL Fingerprint Checker。它们分别覆盖浏览器指纹、环境一致性、网络泄漏、TLS/HTTP 协议指纹、Bot/Automation、IP Reputation、Visitor Identification、浏览器隐私/安全以及数字身份暴露等不同层级。

本仓库的目标不是给工具做“最好/最强”排名，而是快速回答三个问题：**这个工具主要检测什么、它与其他工具相比有什么独特点、目前是否仍值得继续维护。**

## 30款工具快速目录

| # | 工具 | 类型 | 主要检测方向 | 独特点 | 状态 | 最后核查 |
|---:|---|---|---|---|---|---|
| 1 | [BrowserScan](https://www.browserscan.net/) | 综合环境检测 | 浏览器、硬件、IP、DNS、WebRTC、TLS | 环境一致性 + JA3/JA4/HTTP2 | Active | 2026-08-09 |
| 2 | [Pixelscan](https://pixelscan.net/) | 综合环境检测 | Fingerprint、IP、Proxy、VPN、DNS、Bot | 多维环境检测 + Android Checker | Active | 2026-08-09 |
| 3 | [Iphey](https://iphey.com/) | 环境可信度检测 | Fingerprint、IP、VPN、Bot、DNS | 强调不同信号之间的一致性 | Active | 2026-08-09 |
| 4 | [Fingerprint-Scan](https://fingerprint-scan.com/) | Fingerprint/Bot | 浏览器指纹、IP Reputation、Proxy | 将指纹异常直接用于 Bot 风险判断 | Active | 2026-08-09 |
| 5 | [Whoer](https://whoer.net/) | 匿名环境检测 | IP、DNS、WebRTC、Proxy、Timezone、UA | 将多种环境不一致直接转化为风险项 | Active | 2026-08-09 |
| 6 | [DeviceInfo.me](https://www.deviceinfo.me/) | 设备信息分析 | 浏览器、OS、硬件、GPU、Fonts、TLS | True Browser/OS 与 Fingerprinting Resistance | Active（访问兼容性可能因环境不同） | 2026-08-09 |
| 7 | [BrowserLeaks](https://browserleaks.com/) | 深度技术检测 | Canvas、WebGL、WebGPU、TLS、HTTP、TCP | JA4T、HTTP/2、QUIC/HTTP3 等协议层检测 | Active | 2026-08-09 |
| 8 | [CreepJS](https://abrahamjuliot.github.io/creepjs/) | 高级指纹分析 | Browser API、Worker、Canvas、WebGL、Audio | Lies、Resistance、Headless、Stealth | Active | 2026-08-09 |
| 9 | [Device & Browser Info](https://deviceandbrowserinfo.com/are_you_a_bot) | Fingerprint/Bot | WebDriver、CDP、Headers、WebGL、Behavior | 同时检查静态指纹和用户行为 | Active | 2026-08-09 |
| 10 | [WebBrowserTools](https://webbrowsertools.com/) | 指纹修改检测 | Canvas、WebGL、WebGPU、ClientRects | Fixed/Random Noise Detection | Active | 2026-08-09 |
| 11 | [Browserize / PrivacyCheck](https://privacycheck.sec.lrz.de/) | 指纹研究 | Active/Passive Fingerprinting | ETag、JSEcho、Header Signature、HTTP2 | Active | 2026-08-09 |
| 12 | [AmIUnique](https://amiunique.org/) | 指纹唯一性 | Browser Fingerprint | Global Statistics + Fingerprint History | Active | 2026-08-09 |
| 13 | [EFF Cover Your Tracks](https://coveryourtracks.eff.org/) | 隐私/追踪检测 | Tracking、Fingerprintability | 同时分析 Tracker Protection | Active | 2026-08-09 |
| 14 | [FingerprintJS OSS Demo](https://fingerprintjs.github.io/fingerprintjs/) | Visitor Identification | 客户端 Browser Signals | 可实际部署的开源指纹算法 | Active | 2026-08-09 |
| 15 | [Fingerprint Pro Playground](https://demo.fingerprint.com/playground) | Device Intelligence | 浏览器、网络、设备、Smart Signals | 客户端 + 服务端持续设备识别 | Active | 2026-08-09 |
| 16 | [Incolumitas Bot Detector](https://bot.incolumitas.com/) | Bot Detection | Browser、TCP/IP、TLS、Behavior | 行为分类 + 多层指纹 | Active | 2026-08-09 |
| 17 | [Rebrowser Bot Detector](https://bot-detector.rebrowser.net/) | Automation Detection | Chromium、CDP、Puppeteer、Playwright | 专攻现代 CDP/Automation Leak | Active | 2026-08-09 |
| 18 | [Sannysoft](https://bot.sannysoft.com/) | 经典 Bot Benchmark | WebDriver、Headless、Plugins、WebGL | 行业常用经典自动化基准 | Active | 2026-08-09 |
| 19 | [AntCpt reCAPTCHA v3 Score](https://antcpt.com/eng/information/demo-form/recaptcha-3-test-score.html) | 外部风控检测 | reCAPTCHA v3 | 直接观察 Google 风控评分 | Active | 2026-08-09 |
| 20 | [TLS.Peet.ws / TrackMe](https://tls.peet.ws/) | 协议指纹 | TLS、HTTP/2、JA3、JA4 | JA3 + JA4 + Akamai + PeetPrint | Active | 2026-08-09 |
| 21 | [IPLeak](https://ipleak.net/) | 网络泄漏检测 | IP、DNS、WebRTC、Torrent | Torrent Client IP + 端口路由测试 | Active | 2026-08-09 |
| 22 | [IPQualityScore](https://www.ipqualityscore.com/ip-reputation-check) | IP Reputation | Proxy、VPN、Tor、Fraud、Abuse | 自有网络信誉和欺诈数据 | Active | 2026-08-09 |
| 23 | [LeaksCheck](https://leakscheck.com/) | 数字身份暴露 | Credential、Infostealer、OSINT | 浏览器之外的身份关联和数字足迹 | Active | 2026-08-09 |
| 24 | [Webkay](https://webkay.robinlinus.com/) | 浏览器信息暴露 | Browser、Hardware、WebRTC、Autofill | Autofill、登录状态、局域网等攻击面 | Active | 2026-08-09 |
| 25 | [PrivacyTests.org](https://privacytests.org/) | 浏览器隐私比较 | 浏览器默认隐私防护 | 统一方法横向比较不同浏览器 | Active | 2026-08-09 |
| 26 | [BrowserAudit](https://browseraudit.com/) | 浏览器安全检测 | SOP、CSP、CORS、Cookies 等 | 检查浏览器安全标准实现 | Active | 2026-08-09 |
| 27 | [Ethical Red](https://www.ethicalred.io/) | 网络路径检测 | WebRTC、STUN、DNS、IPv6、VPN | STUN + VPN Tunnel Integrity | Active | 2026-08-09 |
| 28 | [PrivacyTestLab](https://privacytestlab.com/) | Fingerprint/隐私 | Fingerprint、IP、DNS、WebRTC | 公开 Shannon Entropy 与 Signal Weight | Active | 2026-08-09 |
| 29 | [Privacy.net Analyzer](https://privacy.net/analyzer/) | 身份信息暴露 | Fingerprint、Autofill、登录状态 | Autofill Leak + User Account Tests | Active | 2026-08-09 |
| 30 | [TraceScope](https://tracescope.org/) | 指纹一致性/环境诊断 | Fingerprint、IP、WebRTC、DNS、Automation | 修改痕迹、Server/JS 交叉验证、品牌痕迹 | Active | 2026-08-09 |

## 工具简表

### 1. BrowserScan

**BrowserScan** 主要用于 **浏览器、硬件、IP、DNS、WebRTC、TLS**；它值得单独保留的原因是 **环境一致性 + JA3/JA4/HTTP2**。更适合：**快速检查完整浏览器环境**。  
[官网](https://www.browserscan.net/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 2. Pixelscan

**Pixelscan** 主要用于 **Fingerprint、IP、Proxy、VPN、DNS、Bot**；它值得单独保留的原因是 **多维环境检测 + Android Checker**。更适合：**判断环境是否存在明显异常**。  
[官网](https://pixelscan.net/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 3. Iphey

**Iphey** 主要用于 **Fingerprint、IP、VPN、Bot、DNS**；它值得单独保留的原因是 **强调不同信号之间的一致性**。更适合：**快速判断环境可信度**。  
[官网](https://iphey.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 4. Fingerprint-Scan

**Fingerprint-Scan** 主要用于 **浏览器指纹、IP Reputation、Proxy**；它值得单独保留的原因是 **将指纹异常直接用于 Bot 风险判断**。更适合：**检查指纹是否具有自动化特征**。  
[官网](https://fingerprint-scan.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 5. Whoer

**Whoer** 主要用于 **IP、DNS、WebRTC、Proxy、Timezone、UA**；它值得单独保留的原因是 **将多种环境不一致直接转化为风险项**。更适合：**VPN/Proxy 环境检查**。  
[官网](https://whoer.net/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 6. DeviceInfo.me

**DeviceInfo.me** 主要用于 **浏览器、OS、硬件、GPU、Fonts、TLS**；它值得单独保留的原因是 **True Browser/OS 与 Fingerprinting Resistance**。更适合：**深入查看设备暴露信息**。  
[官网](https://www.deviceinfo.me/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 7. BrowserLeaks

**BrowserLeaks** 主要用于 **Canvas、WebGL、WebGPU、TLS、HTTP、TCP**；它值得单独保留的原因是 **JA4T、HTTP/2、QUIC/HTTP3 等协议层检测**。更适合：**深入分析具体指纹参数**。  
[官网](https://browserleaks.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 8. CreepJS

**CreepJS** 主要用于 **Browser API、Worker、Canvas、WebGL、Audio**；它值得单独保留的原因是 **Lies、Resistance、Headless、Stealth**。更适合：**检查指纹伪装和异常**。  
[官网](https://abrahamjuliot.github.io/creepjs/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 9. Device & Browser Info

**Device & Browser Info** 主要用于 **WebDriver、CDP、Headers、WebGL、Behavior**；它值得单独保留的原因是 **同时检查静态指纹和用户行为**。更适合：**自动化浏览器调试**。  
[官网](https://deviceandbrowserinfo.com/are_you_a_bot) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 10. WebBrowserTools

**WebBrowserTools** 主要用于 **Canvas、WebGL、WebGPU、ClientRects**；它值得单独保留的原因是 **Fixed/Random Noise Detection**。更适合：**检查指纹是否被修改**。  
[官网](https://webbrowsertools.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 11. Browserize / PrivacyCheck

**Browserize / PrivacyCheck** 主要用于 **Active/Passive Fingerprinting**；它值得单独保留的原因是 **ETag、JSEcho、Header Signature、HTTP2**。更适合：**研究高级指纹技术**。  
[官网](https://privacycheck.sec.lrz.de/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 12. AmIUnique

**AmIUnique** 主要用于 **Browser Fingerprint**；它值得单独保留的原因是 **Global Statistics + Fingerprint History**。更适合：**判断指纹是否罕见**。  
[官网](https://amiunique.org/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 13. EFF Cover Your Tracks

**EFF Cover Your Tracks** 主要用于 **Tracking、Fingerprintability**；它值得单独保留的原因是 **同时分析 Tracker Protection**。更适合：**判断浏览器被追踪难度**。  
[官网](https://coveryourtracks.eff.org/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 14. FingerprintJS OSS Demo

**FingerprintJS OSS Demo** 主要用于 **客户端 Browser Signals**；它值得单独保留的原因是 **可实际部署的开源指纹算法**。更适合：**理解网站如何生成 Visitor ID**。  
[官网](https://fingerprintjs.github.io/fingerprintjs/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 15. Fingerprint Pro Playground

**Fingerprint Pro Playground** 主要用于 **浏览器、网络、设备、Smart Signals**；它值得单独保留的原因是 **客户端 + 服务端持续设备识别**。更适合：**研究商业设备识别**。  
[官网](https://demo.fingerprint.com/playground) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 16. Incolumitas Bot Detector

**Incolumitas Bot Detector** 主要用于 **Browser、TCP/IP、TLS、Behavior**；它值得单独保留的原因是 **行为分类 + 多层指纹**。更适合：**综合 Bot/自动化检测**。  
[官网](https://bot.incolumitas.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 17. Rebrowser Bot Detector

**Rebrowser Bot Detector** 主要用于 **Chromium、CDP、Puppeteer、Playwright**；它值得单独保留的原因是 **专攻现代 CDP/Automation Leak**。更适合：**调试 Playwright/Puppeteer**。  
[官网](https://bot-detector.rebrowser.net/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 18. Sannysoft

**Sannysoft** 主要用于 **WebDriver、Headless、Plugins、WebGL**；它值得单独保留的原因是 **行业常用经典自动化基准**。更适合：**基础 Automation 检查**。  
[官网](https://bot.sannysoft.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 19. AntCpt reCAPTCHA v3 Score

**AntCpt reCAPTCHA v3 Score** 主要用于 **reCAPTCHA v3**；它值得单独保留的原因是 **直接观察 Google 风控评分**。更适合：**判断当前访问的人机风险**。  
[官网](https://antcpt.com/eng/information/demo-form/recaptcha-3-test-score.html) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 20. TLS.Peet.ws / TrackMe

**TLS.Peet.ws / TrackMe** 主要用于 **TLS、HTTP/2、JA3、JA4**；它值得单独保留的原因是 **JA3 + JA4 + Akamai + PeetPrint**。更适合：**检查 TLS/HTTP 客户端身份**。  
[官网](https://tls.peet.ws/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 21. IPLeak

**IPLeak** 主要用于 **IP、DNS、WebRTC、Torrent**；它值得单独保留的原因是 **Torrent Client IP + 端口路由测试**。更适合：**VPN/Proxy 泄漏排查**。  
[官网](https://ipleak.net/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 22. IPQualityScore

**IPQualityScore** 主要用于 **Proxy、VPN、Tor、Fraud、Abuse**；它值得单独保留的原因是 **自有网络信誉和欺诈数据**。更适合：**判断 IP 风险质量**。  
[官网](https://www.ipqualityscore.com/ip-reputation-check) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 23. LeaksCheck

**LeaksCheck** 主要用于 **Credential、Infostealer、OSINT**；它值得单独保留的原因是 **浏览器之外的身份关联和数字足迹**。更适合：**检查历史身份暴露**。  
[官网](https://leakscheck.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 24. Webkay

**Webkay** 主要用于 **Browser、Hardware、WebRTC、Autofill**；它值得单独保留的原因是 **Autofill、登录状态、局域网等攻击面**。更适合：**理解网站能知道什么**。  
[官网](https://webkay.robinlinus.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 25. PrivacyTests.org

**PrivacyTests.org** 主要用于 **浏览器默认隐私防护**；它值得单独保留的原因是 **统一方法横向比较不同浏览器**。更适合：**比较浏览器抗追踪能力**。  
[官网](https://privacytests.org/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 26. BrowserAudit

**BrowserAudit** 主要用于 **SOP、CSP、CORS、Cookies 等**；它值得单独保留的原因是 **检查浏览器安全标准实现**。更适合：**浏览器安全能力分析**。  
[官网](https://browseraudit.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 27. Ethical Red

**Ethical Red** 主要用于 **WebRTC、STUN、DNS、IPv6、VPN**；它值得单独保留的原因是 **STUN + VPN Tunnel Integrity**。更适合：**检查 VPN 是否真正完整接管流量**。  
[官网](https://www.ethicalred.io/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 28. PrivacyTestLab

**PrivacyTestLab** 主要用于 **Fingerprint、IP、DNS、WebRTC**；它值得单独保留的原因是 **公开 Shannon Entropy 与 Signal Weight**。更适合：**理解评分和指纹唯一性**。  
[官网](https://privacytestlab.com/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 29. Privacy.net Analyzer

**Privacy.net Analyzer** 主要用于 **Fingerprint、Autofill、登录状态**；它值得单独保留的原因是 **Autofill Leak + User Account Tests**。更适合：**检查浏览器身份泄漏**。  
[官网](https://privacy.net/analyzer/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

### 30. TraceScope

**TraceScope** 主要用于 **Fingerprint、IP、WebRTC、DNS、Automation**；它值得单独保留的原因是 **修改痕迹、Server/JS 交叉验证、品牌痕迹**。更适合：**检查浏览器环境是否存在伪装或异常**。  
[官网](https://tracescope.org/) · [完整介绍 → Web4 Browser](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)

## 结构化数据

- [`data/tools.csv`](data/tools.csv)：30 款工具的类型、检测方向、结果形式、独特点、适用场景、状态与核查日期。
- [`data/test-dimensions.csv`](data/test-dimensions.csv)：浏览器指纹、环境一致性、网络泄漏、协议指纹、Bot/Automation、唯一性/识别、网络信誉、浏览器隐私/安全、数字身份暴露等检测层。
- [`METHODOLOGY.md`](METHODOLOGY.md)：纳入标准、内容边界和维护规则。
- [`SOURCES.md`](SOURCES.md)：30 款工具官方入口和后续来源账本。
- [`CHANGELOG.md`](CHANGELOG.md)：项目更新历史。
- [`IMAGE-MAP.md`](IMAGE-MAP.md)：30 张官网截图的文件名、Alt 与 Caption 建议。

## 状态说明

- `active`：本轮核查时仍作为现役候选工具保留。
- `active_access_may_vary`：仍有现役页面证据，但不同网络/抓取环境下访问可能不稳定。
- `tested=false`：表示本项目尚未在统一硬件、浏览器版本、网络和代理条件下执行完整横向实测。

## 使用边界

不同工具的 `Trust Score`、`Bot Risk Score`、`Fraud Score`、`Pass/Fail` 或其他总分不能直接横向换算。公共检测器显示“正常”也不代表某个具体目标网站一定会给出相同判断。

## 原文与维护

- 完整原文：[https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86](https://web4browser.io/cn/blog/2026%E5%B9%B430%E6%AC%BE%E6%B5%8F%E8%A7%88%E5%99%A8%E6%8C%87%E7%BA%B9%E6%A3%80%E6%B5%8B%E4%B8%8E%E5%88%86%E6%9E%90%E5%B7%A5%E5%85%B7%E6%B1%87%E6%80%BB%E6%9C%80%E6%96%B0%E6%95%B4%E7%90%86)
- GitHub 版本：工具目录、状态、来源、结构化数据与更新日志。
- 发现工具失效、改版或新增重要检测维度，可通过 Issue 提交更新建议。
