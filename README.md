# 2026年30款浏览器指纹检测与分析工具汇总（最新整理）
> **更新日期：2026-08-09**  
> GitHub 版本用于持续维护工具目录、功能变化与来源。WordPress 原文发布后，可在这里补充原文地址。
![2026年30款浏览器指纹检测与分析工具汇总封面](assets/browser-fingerprint-checkers-2026-cover.png)
浏览器在访问网站时，会向网站暴露大量与设备、操作系统、浏览器和网络环境有关的信息，例如 User-Agent、Client Hints、屏幕分辨率、语言、时区、字体、Canvas、WebGL、WebGPU、AudioContext 和 WebRTC，以及 IP、DNS、TLS、HTTP 等网络与协议特征。这些信号既可以单独使用，也可以被组合起来构成浏览器指纹以及更广义的客户端和网络身份，用于设备识别、访问分析、反欺诈、Bot 检测、风险控制和用户识别。

浏览器指纹检测与分析工具可以帮助用户了解当前浏览器和网络环境究竟向网站暴露了哪些信息，并进一步检查不同信号之间是否保持合理一致。例如浏览器声明的操作系统是否与硬件特征匹配，HTTP Header 与 JavaScript 获取到的身份信息是否一致，IP 所在地区与时区、语言和 DNS 是否协调，以及浏览器是否存在 Canvas/WebGL 修改、WebRTC 或 DNS 泄漏、自动化特征、运行时修改痕迹等异常。

不同工具关注的检测层并不相同。有些工具主要分析 Canvas、WebGL、WebGPU、Fonts、AudioContext 等浏览器指纹；有些更关注环境一致性、Fingerprint Spoofing 和 Modification Traces；还有一些进一步检测 Proxy、VPN、IP Reputation、TLS、JA3/JA4、HTTP/2、Bot/Automation、Visitor Identification、浏览器隐私防护以及数字身份暴露等信息。

本文整理了 30 款浏览器指纹、环境一致性、网络身份和数字身份检测工具，包括 BrowserLeaks、Pixelscan、BrowserScan、CreepJS、TraceScope 等浏览器环境分析网站，也涵盖 TLS/HTTP 指纹、Bot Detection、IP Reputation、Visitor Identification、网络泄漏、浏览器隐私防护和数字身份暴露等不同方向。这些工具可用于浏览器隐私检查、浏览器环境测试、Proxy/VPN 网络排查、WebRTC 和 DNS 泄漏检测、自动化浏览器调试、浏览器环境一致性验证，以及浏览器指纹和设备识别技术研究。后文除了介绍每个网站的基本用途，也会重点说明它与其他同类工具相比值得单独关注的特点。
## 30款浏览器指纹检测与分析工具快速对比
这 30 款工具并不是功能完全相同的 Browser Fingerprint Checker。有些更适合快速判断完整浏览器环境，有些专门查看 Canvas、WebGL、TLS 等底层信号，还有一些重点检测 Bot、自动化、网络泄漏、浏览器隐私防护或数字身份暴露。
| 工具 | 类型 | 主要检测方向 | 结果形式 | 最突出的特点 | 更适合用于 |
|---|---|---|---|---|---|
| [BrowserScan](https://www.browserscan.net/) | 综合环境检测 | 浏览器、硬件、IP、DNS、WebRTC、TLS | 判断 + 原始数据 | 环境一致性 + JA3/JA4/HTTP2 | 快速检查完整浏览器环境 |
| [Pixelscan](https://pixelscan.net/) | 综合环境检测 | Fingerprint、IP、Proxy、VPN、DNS、Bot | 综合判断 | 多维环境检测 + Android Checker | 判断环境是否存在明显异常 |
| [Iphey](https://iphey.com/) | 环境可信度检测 | Fingerprint、IP、VPN、Bot、DNS | Trust Score | 强调不同信号之间的一致性 | 快速判断环境可信度 |
| [Fingerprint-Scan](https://fingerprint-scan.com/) | Fingerprint/Bot | 浏览器指纹、IP Reputation、Proxy | Bot Risk Score | 将指纹异常直接用于 Bot 风险判断 | 检查指纹是否具有自动化特征 |
| [Whoer](https://whoer.net/) | 匿名环境检测 | IP、DNS、WebRTC、Proxy、Timezone、UA | 匿名度/异常判断 | 将多种环境不一致直接转化为风险项 | VPN/Proxy 环境检查 |
| [DeviceInfo.me](https://www.deviceinfo.me/) | 设备信息分析 | 浏览器、OS、硬件、GPU、Fonts、TLS | 原始数据 + 部分判断 | True Browser/OS 与 Fingerprinting Resistance | 深入查看设备暴露信息 |
| [BrowserLeaks](https://browserleaks.com/) | 深度技术检测 | Canvas、WebGL、WebGPU、TLS、HTTP、TCP | 原始数据 | JA4T、HTTP/2、QUIC/HTTP3 等协议层检测 | 深入分析具体指纹参数 |
| [CreepJS](https://abrahamjuliot.github.io/creepjs/) | 高级指纹分析 | Browser API、Worker、Canvas、WebGL、Audio | 异常分析 | Lies、Resistance、Headless、Stealth | 检查指纹伪装和异常 |
| [Device & Browser Info](https://deviceandbrowserinfo.com/are_you_a_bot) | Fingerprint/Bot | WebDriver、CDP、Headers、WebGL、Behavior | Bot/异常判断 | 同时检查静态指纹和用户行为 | 自动化浏览器调试 |
| [WebBrowserTools](https://webbrowsertools.com/) | 指纹修改检测 | Canvas、WebGL、WebGPU、ClientRects | Spoof 判断 | Fixed/Random Noise Detection | 检查指纹是否被修改 |
| [Browserize / PrivacyCheck](https://privacycheck.sec.lrz.de/) | 指纹研究 | Active/Passive Fingerprinting | 原始实验数据 | ETag、JSEcho、Header Signature、HTTP2 | 研究高级指纹技术 |
| [AmIUnique](https://amiunique.org/) | 指纹唯一性 | Browser Fingerprint | 唯一性/统计 | Global Statistics + Fingerprint History | 判断指纹是否罕见 |
| [EFF Cover Your Tracks](https://coveryourtracks.eff.org/) | 隐私/追踪检测 | Tracking、Fingerprintability | 隐私判断 | 同时分析 Tracker Protection | 判断浏览器被追踪难度 |
| [FingerprintJS OSS Demo](https://fingerprintjs.github.io/fingerprintjs/) | Visitor Identification | 客户端 Browser Signals | Visitor ID | 可实际部署的开源指纹算法 | 理解网站如何生成 Visitor ID |
| [Fingerprint Pro Playground](https://demo.fingerprint.com/playground) | Device Intelligence | 浏览器、网络、设备、Smart Signals | Visitor ID + 风险信号 | 客户端 + 服务端持续设备识别 | 研究商业设备识别 |
| [Incolumitas Bot Detector](https://bot.incolumitas.com/) | Bot Detection | Browser、TCP/IP、TLS、Behavior | Behavioral Score | 行为分类 + 多层指纹 | 综合 Bot/自动化检测 |
| [Rebrowser Bot Detector](https://bot-detector.rebrowser.net/) | Automation Detection | Chromium、CDP、Puppeteer、Playwright | 异常判断 | 专攻现代 CDP/Automation Leak | 调试 Playwright/Puppeteer |
| [Sannysoft](https://bot.sannysoft.com/) | 经典 Bot Benchmark | WebDriver、Headless、Plugins、WebGL | Pass/Fail | 行业常用经典自动化基准 | 基础 Automation 检查 |
| [AntCpt reCAPTCHA v3 Score](https://antcpt.com/eng/information/demo-form/recaptcha-3-test-score.html) | 外部风控检测 | reCAPTCHA v3 | 0.1–0.9 Score | 直接观察 Google 风控评分 | 判断当前访问的人机风险 |
| [TLS.Peet.ws / TrackMe](https://tls.peet.ws/) | 协议指纹 | TLS、HTTP/2、JA3、JA4 | 原始协议数据 | JA3 + JA4 + Akamai + PeetPrint | 检查 TLS/HTTP 客户端身份 |
| [IPLeak](https://ipleak.net/) | 网络泄漏检测 | IP、DNS、WebRTC、Torrent | 原始数据 | Torrent Client IP + 端口路由测试 | VPN/Proxy 泄漏排查 |
| [IPQualityScore](https://www.ipqualityscore.com/ip-reputation-check) | IP Reputation | Proxy、VPN、Tor、Fraud、Abuse | Fraud Score | 自有网络信誉和欺诈数据 | 判断 IP 风险质量 |
| [LeaksCheck](https://leakscheck.com/) | 数字身份暴露 | Credential、Infostealer、OSINT | 查询结果 | 浏览器之外的身份关联和数字足迹 | 检查历史身份暴露 |
| [Webkay](https://webkay.robinlinus.com/) | 浏览器信息暴露 | Browser、Hardware、WebRTC、Autofill | 可视化演示 | Autofill、登录状态、局域网等攻击面 | 理解网站能知道什么 |
| [PrivacyTests.org](https://privacytests.org/) | 浏览器隐私比较 | 浏览器默认隐私防护 | Pass/Fail | 统一方法横向比较不同浏览器 | 比较浏览器抗追踪能力 |
| [BrowserAudit](https://browseraudit.com/) | 浏览器安全检测 | SOP、CSP、CORS、Cookies 等 | 400+测试结果 | 检查浏览器安全标准实现 | 浏览器安全能力分析 |
| [Ethical Red](https://www.ethicalred.io/) | 网络路径检测 | WebRTC、STUN、DNS、IPv6、VPN | 泄漏/路径判断 | STUN + VPN Tunnel Integrity | 检查 VPN 是否真正完整接管流量 |
| [PrivacyTestLab](https://privacytestlab.com/) | Fingerprint/隐私 | Fingerprint、IP、DNS、WebRTC | Fingerprint Score | 公开 Shannon Entropy 与 Signal Weight | 理解评分和指纹唯一性 |
| [Privacy.net Analyzer](https://privacy.net/analyzer/) | 身份信息暴露 | Fingerprint、Autofill、登录状态 | 测试结果 | Autofill Leak + User Account Tests | 检查浏览器身份泄漏 |
| [TraceScope](https://tracescope.org/) | 指纹一致性/环境诊断 | Fingerprint、IP、WebRTC、DNS、Automation | 一致性评分 + 证据报告 | 修改痕迹、Server/JS 交叉验证、品牌痕迹 | 检查浏览器环境是否存在伪装或异常 |

## 浏览器指纹检测工具（定期保持更新）

### 1. BrowserScan

**官方网站：** https://www.browserscan.net/

**网站介绍：** BrowserScan 是一个综合型浏览器指纹和网络环境检测平台。打开检测页面后，可以查看当前浏览器、操作系统、IP、地理位置、ISP、Proxy、DNS、Bot Detection，以及 Canvas、WebGL、Audio、ClientRects、WebGPU、屏幕、媒体设备、字体、语言和时区等信息。它比较适合用于快速了解一个完整浏览器环境在网站看来呈现出的设备和网络身份。

**主要特点：** BrowserScan 不只是展示传统 JavaScript 浏览器指纹，还提供 Kernel 与 User-Agent 一致性、时区一致性、Client Hints、WebGPU，以及独立的 HTTP/2、SSL/TLS 指纹检测工具。它因此既可以查看单个浏览器参数，也可以进一步观察浏览器、操作系统、硬件和网络之间是否存在不合理组合。

### 2. Pixelscan

**官方网站：** https://pixelscan.net/

**网站介绍：** Pixelscan 是一个 All-in-One 类型的浏览器环境检测网站，将 Fingerprint Check、IP、Proxy、VPN、IP Blacklist、DNS Leak、Bot Verification、Location 和 WebRTC Leak 等多种检测集中在一个平台中。用户可以通过一次扫描快速查看当前浏览器与网络环境是否暴露明显异常。

**主要特点：** Pixelscan 更强调“整个环境是否协调”，而不只是显示某一个 Canvas 或 WebGL Hash。例如它会检查 IP、时区和语言之间的关系，同时结合 Proxy、IP 黑名单、DNS Leak 和 Bot 痕迹进行判断。此外，Pixelscan 还提供独立的 Android Checker，使它的检测范围不只局限于桌面浏览器。

### 3. Iphey

**官方网站：** https://iphey.com/

**网站介绍：** Iphey 是一个用于分析浏览器数字身份的综合检测工具，可以查看 Browser、Location、IP Address、Hardware 和 Software 等信息，并提供 Fingerprint Check、IP Check、VPN Checker、Bot Check、DNS Leak Test 和 IP Blacklist Test 等功能。其浏览器指纹检测涉及 User-Agent、Canvas、WebRTC、AudioContext、Fonts 和 Plugins 等常见信号。

**主要特点：** Iphey 的重点并不是单纯列出浏览器参数，而是进一步形成 Trust Score。低 Trust Score 可能来自低质量 Proxy、IP 与时区不匹配或明显的自动化痕迹，因此它更适合用于判断多个参数组合起来以后，这个浏览器环境是否自然和可信。

### 4. Fingerprint-Scan

**官方网站：** https://fingerprint-scan.com/

**网站介绍：** Fingerprint-Scan 是一个将浏览器 Fingerprinting 与 Bot Detection 结合起来的在线检测工具。网站可以生成当前浏览器的 Fingerprint ID，并提供 Browser Fingerprint、IP Address、Canvas Fingerprint、HTTP Headers 和 Browser Extensions 等独立检测页面。

**主要特点：** Fingerprint-Scan 会进一步利用收集到的指纹计算 Bot Risk Score。该评分综合浏览器指纹、IP Reputation 和 Proxy Detection，同时还会寻找 User-Agent 与实际浏览器环境之间的矛盾，例如修改成 Firefox User-Agent，但底层仍然留下 Chrome 特征。

### 5. Whoer

**官方网站：** https://whoer.net/

**网站介绍：** Whoer 是一个以网络匿名性和环境泄漏检查为核心的综合检测平台，可以查看 IP、ISP、地理位置、DNS、WebRTC、Proxy、VPN、Tor、Blacklist、浏览器和系统信息，并根据检测结果评估当前环境的匿名状态。

**主要特点：** Whoer 会把多个环境不一致问题直接转化成具体风险项，例如 DNS 所在国家与 IP 国家不同、系统时间与 IP 时区不同、HTTP User-Agent 与 JavaScript 检测到的浏览器信息不同，以及浏览器语言与 IP 所在地区明显不匹配。相比只显示指纹 Hash 的工具，它更像一个环境一致性检查器。

### 6. DeviceInfo.me

**官方网站：** https://www.deviceinfo.me/

**网站介绍：** DeviceInfo.me 是一个非常详细的浏览器安全、隐私和设备信息检测网站。它可以显示操作系统、浏览器、IP、Proxy、VPN、Tor、HTTP Headers、TLS/SSL、CPU、RAM、GPU、Fonts、Canvas、AudioContext、WebGL、WebRTC、媒体设备、存储、Plugins、Screen 和 Private Browsing Mode 等大量信息。

**主要特点：** DeviceInfo.me 的价值在于原始信息非常丰富，而且还尝试识别 True Browser Core、True Operating System Core 和 Fingerprinting Resistance。Canvas 与 AudioContext 等项目也不只是简单显示是否支持，还会判断 Fingerprinting 是 Allowed、Blocked 还是 Spoofed，因此比较适合深入检查浏览器究竟修改了哪些底层信号。

### 7. BrowserLeaks

**官方网站：** https://browserleaks.com/

**网站介绍：** BrowserLeaks 是一个将浏览器、设备和网络暴露信息拆分成大量独立技术测试的在线分析平台。用户可以分别查看 IP、JavaScript、WebRTC、Canvas、WebGL、WebGPU、Fonts、Geolocation、Feature Detection、Client Hints、DNS 和 TLS 等信息，适合逐项了解网站能够获取到哪些原始浏览器和网络数据。

**主要特点：** BrowserLeaks 的检测深度已经超出了普通 Canvas/WebGL Fingerprint。它可以生成 JA3/JA4 TLS 指纹，查看 TCP/IP 与 JA4T、HTTP/2 指纹，并提供 QUIC/HTTP/3 和 WebGPU 等测试。因此它特别适合观察浏览器 JavaScript 指纹之外的协议层和网络层身份。

### 8. CreepJS

**官方网站：** https://abrahamjuliot.github.io/creepjs/

**网站介绍：** CreepJS 是一个偏研究型的高级浏览器指纹分析项目，可以收集和展示 WebRTC、Canvas、WebGL、Fonts、DOMRect、SVGRect、Audio、Speech、Media、Screen、Timezone、Navigator、CSS、Math 和 Worker 等大量浏览器信号。

**主要特点：** CreepJS 的价值不只是检测项目多，还会特别关注 Fingerprint Resistance、Lies Detection、Headless、Stealth、Worker 与主线程差异、JS Proxy 等异常。它不仅想知道浏览器返回了什么，还试图判断这些返回值是否可能经过修改、伪装或反指纹处理。

### 9. Device & Browser Info

**官方网站：** https://deviceandbrowserinfo.com/are_you_a_bot

**网站介绍：** Device & Browser Info 是一个结合设备信息、浏览器指纹和 Bot Detection 的研究型网站。其检测体系同时包含客户端 Browser Fingerprinting、服务器端 HTTP Headers、IP/Proxy 数据，以及独立的 Fingerprinting Bot Test 和 Behavioral Bot Test。

**主要特点：** 它把 Bot Detection 拆得比较细，例如可以检测 navigator.webdriver、iframe 中的 WebDriver、Playwright 特定变量、Selenium 特征、Headless Chrome 和 WebGL 不一致等。同时还提供独立的行为测试，观察鼠标移动、输入速度、表单提交以及 CDP Mouse Leak，因此可以同时研究静态指纹和自动化行为。

### 10. WebBrowserTools

**官方网站：** https://webbrowsertools.com/

**网站介绍：** WebBrowserTools 提供多种浏览器隐私和安全测试，其中包括 Canvas Fingerprint、WebGL Fingerprint、WebGPU Fingerprint、ClientRects Fingerprint、AudioContext 和其他浏览器环境检测工具。它比较适合需要单独检查某一个具体 Fingerprinting Surface 的用户。

**主要特点：** WebBrowserTools 的重点不是只生成 Hash，而是尝试判断浏览器扩展是否对 Canvas、WebGL、WebGPU 或 ClientRects 加入了固定或随机 Noise。网站还区分 Normal 与 Aggressive 两种读取方式，用来观察普通 JavaScript 方法与更强检测方法得到的结果是否不同。

### 11. Browserize / PrivacyCheck

**官方网站：** https://privacycheck.sec.lrz.de/

**网站介绍：** Browserize 是一个专门展示 Browser Fingerprinting 技术的研究型平台。它不是简单给出一个安全或不安全结果，而是为不同 Fingerprinting Technique 建立独立页面，并说明每种方法的原理、分类和实际演示。常见检测包括 Canvas、WebGL、WebRTC、Fonts、AudioContext、Math、Feature Detection 和 getClientRects 等。

**主要特点：** Browserize 明确把浏览器指纹分成 Active Fingerprinting 与 Passive Fingerprinting。除了常见客户端检测，它还提供 ETag Fingerprinting、HTTP Header Signature、HTTP/2 Fingerprinting、CSS Font 和 JSEcho 等较少见的实验；其中 HTTP/2 Fingerprint 可以主要在服务器端生成。

### 12. AmIUnique

**官方网站：** https://amiunique.org/

**网站介绍：** AmIUnique 是一个以研究浏览器指纹唯一性为核心的网站。它通过收集浏览器和设备参数生成 Fingerprint，并让用户了解自己的浏览器在其他真实样本中到底有多容易被区分。检测数据包括浏览器、操作系统、屏幕、架构、字体、Plugins、摄像头和麦克风等。

**主要特点：** 它最大的区别是拥有 Global Statistics、Fingerprint History 和 Timeline。因此用户不仅可以看到当前指纹，还可以将自己的结果与全球样本进行比较，并观察同一个设备或浏览器的指纹随着配置、版本和时间变化发生了什么改变。

### 13. EFF Cover Your Tracks

**官方网站：** https://coveryourtracks.eff.org/

**网站介绍：** Cover Your Tracks 是 Electronic Frontier Foundation（EFF）推出的浏览器隐私测试项目，用于检查当前浏览器面对 Tracking 和 Fingerprinting 时的保护能力，并向用户展示 Tracker 实际能够看到哪些独特浏览器特征。

**主要特点：** 它与普通 Fingerprint Checker 的区别是关注重点更接近这个浏览器有多容易被追踪，而不是简单展示所有底层参数。测试结果会把浏览器的 Tracker Protection 和 Fingerprintability 放在隐私追踪场景中解释，因此适合普通用户理解浏览器指纹为什么能够被用来持续识别访问者。

### 14. FingerprintJS OSS Demo

**官方网站：** https://fingerprintjs.github.io/fingerprintjs/

**网站介绍：** FingerprintJS 是一个开源、客户端运行的 Browser Fingerprinting Library。它通过读取浏览器属性并对这些数据进行处理，最终计算出一个 Visitor Identifier。官方 Demo 可以直接运行算法并查看当前浏览器生成的 Visitor ID。

**主要特点：** FingerprintJS 与普通检测网站最大的区别，是它本身就是可以集成到网站中的开源指纹识别库，而不只是给用户看的测试页面。它非常适合用来理解网站如何把多个浏览器信号组合成可以持续使用的 Visitor ID。

### 15. Fingerprint Pro Playground

**官方网站：** https://demo.fingerprint.com/playground

**网站介绍：** Fingerprint Pro Playground 是 Fingerprint 商业 Device Intelligence 平台的在线演示，可以分析当前设备和浏览器信号并生成 Visitor ID。与开源 FingerprintJS 相比，商业版本会将客户端采集到的信息发送至服务器端进一步处理。

**主要特点：** Fingerprint Pro 将 Browser Fingerprint 扩展到了更完整的设备识别体系。除了持续 Visitor Identification，还能够提供 Bot、VPN、Incognito、Browser Tampering 等 Smart Signals，因此代表的是商业反欺诈系统如何从大量浏览器和网络信号中持续识别同一访问设备。

### 16. Incolumitas Bot Detector

**官方网站：** https://bot.incolumitas.com/

**网站介绍：** Incolumitas Bot Detector 是一个综合型 Bot 和 Headless Browser Detection 测试页面，可以检查 Browser Fingerprint、Canvas、WebGL、HTTP Headers、TCP/IP Fingerprint、TLS Fingerprint、Proxy/VPN、Web Worker 和 Service Worker 等大量信号。

**主要特点：** 除了静态指纹，它还有 Behavioral Bot Classification Score。评分会随着访问行为持续更新，并综合多个行为分类器，因此可以把技术环境与真实访问行为一起观察。它也保留旧式 Bot Detection Tests，方便对比经典和现代检测方法。

### 17. Rebrowser Bot Detector

**官方网站：** https://bot-detector.rebrowser.net/

**网站介绍：** Rebrowser Bot Detector 是一个专门针对现代 Chromium 自动化浏览器的检测项目，主要用于测试 Puppeteer、Playwright 以及 Chrome DevTools Protocol 等自动化方式是否留下能够被网站识别的异常。

**主要特点：** 它不像传统 Bot Checker 只关注 navigator.webdriver，而是测试更具体的自动化泄漏，例如 exposeFunctionLeak、sourceUrlLeak、runtimeEnableLeak 和 mainWorldExecution 等，因此更适合现代 Playwright/Puppeteer 自动化环境调试。

### 18. Sannysoft

**官方网站：** https://bot.sannysoft.com/

**网站介绍：** Sannysoft 是一个非常经典的自动化和 Headless Browser 检测页面，整合 Intoli Tests 与 Fingerprint Scanner Tests。它会检查 User-Agent、WebDriver、Chrome Object、Permissions、Plugins、Languages、WebGL、Canvas、Screen 和其他 Navigator 属性。

**主要特点：** Sannysoft 今天的价值更多在于 Legacy Benchmark（经典基准）。很多 Selenium、Puppeteer、Playwright 和反检测浏览器环境仍会用是否通过 Sannysoft 作为基础检查。不过它主要代表较早一代 Automation Detection，因此更适合作为基础基准，而不能替代现代 CDP 或行为检测工具。

### 19. AntCpt reCAPTCHA v3 Score

**官方网站：** https://antcpt.com/eng/information/demo-form/recaptcha-3-test-score.html

**网站介绍：** AntCpt 的测试页面用于查看当前访问在 Google reCAPTCHA v3 中获得的风险评分。它不是传统意义上的 Browser Fingerprint Checker，而是通过真实 reCAPTCHA v3 结果观察当前浏览器和访问环境被外部风控系统判断得有多接近真人或 Bot。

**主要特点：** 页面直接显示 reCAPTCHA v3 Score。较高分值通常代表当前访问更接近正常真人行为，较低分值则意味着访问更可疑。因此它提供的是比较特别的外部风控结果视角：不是告诉用户 Canvas 是什么，而是观察成熟风控系统最终如何评价这次访问。

### 20. TLS.Peet.ws / TrackMe

**官方网站：** https://tls.peet.ws/

**网站介绍：** TLS.Peet.ws 是一个专门用于分析 TLS、HTTP 和客户端协议指纹的检测网站。它会展示当前连接使用的 TLS、HTTP、Cipher Suites、TLS Extensions、TLS Curves、HTTP/2 Frames 和其他请求信息。

**主要特点：** 它可以在同一个页面直接输出 JA3、JA4、Akamai HTTP Fingerprint 和 PeetPrint。网站同时提供 API，因此不仅适合人工查看，也适合开发人员通过程序获取客户端协议层 Fingerprint。

### 21. IPLeak

**官方网站：** https://ipleak.net/

**网站介绍：** IPLeak 是一个专门检查 IP 和网络隐私泄漏的工具。它可以查看公网 IP、WebRTC 暴露的 IP、DNS Resolver、地理位置、ISP、User-Agent、HTTP Headers、系统信息、Screen 和 Plugins 等数据，尤其适合 VPN 和 Proxy 环境的泄漏排查。

**主要特点：** 除了常见 WebRTC 与 DNS Leak，IPLeak 还提供 Torrent Address Detection。它可以通过 Torrent Tracker 观察 Torrent Client 实际暴露的 IP，并通过不同端口检查网络是否存在基于 Destination Port 的不同路由行为。

### 22. IPQualityScore

**官方网站：** https://www.ipqualityscore.com/ip-reputation-check

**网站介绍：** IPQualityScore（IPQS）的 IP Reputation Check 主要用于分析一个 IP 地址的信誉和风险，包括 Proxy、VPN、Tor、Hosting Provider、Blacklist、Abuse 和 Fraud Risk 等信息。它不是传统 Canvas/WebGL 浏览器指纹检测器，而是从网络身份信誉的角度补充环境判断。

**主要特点：** IPQS 的判断不仅依赖普通静态黑名单，还综合 Network Reputation、ASN 与 Hosting、Proxy/VPN Detection、Behavioral Risk、Honeypot Telemetry、Abuse Reports 和 Fraud Signals。因此它更适合回答这个 IP 在反欺诈系统看来是否具有风险。

### 23. LeaksCheck

**官方网站：** https://leakscheck.com/

**网站介绍：** LeaksCheck 是一个 Data Breach、Credential Intelligence 和 OSINT 查询平台。它本身不检测 Canvas、WebGL 或 Browser Fingerprint，而是可以通过邮箱、Domain、Username、Phone Number 等身份标识搜索 Infostealer Logs、泄露数据库和其他外部情报来源。

**主要特点：** LeaksCheck 从浏览器指纹之外提供了另外一个身份关联角度。即使浏览器和网络环境本身没有明显异常，历史邮箱、用户名、社交账号或泄露凭据仍然可能构成能够关联同一个人的 Digital Footprint。因此它可以补充浏览器技术指纹没有覆盖的身份暴露层。

### 24. Webkay

**官方网站：** https://webkay.robinlinus.com/

**网站介绍：** Webkay 是一个用来展示网站能够从浏览器知道什么的隐私演示项目。页面会展示浏览器能够暴露的位置、操作系统、Browser、Plugins、Hardware、Connection 和 WebRTC 等信息，让普通用户更直观地理解网页访问过程中可能泄露的数据。

**主要特点：** Webkay 的内容不只局限于 Fingerprint 参数，还演示 Social Media 登录状态、Clickjacking、Auto-Fill Phishing 和 Local Network 等身份与网络暴露场景，因此更强调技术信息最终如何连接到真实用户身份。

### 25. PrivacyTests.org

**官方网站：** https://privacytests.org/

**网站介绍：** PrivacyTests.org 是一个开源浏览器隐私测试项目。与前面的工具不同，它主要不是检查某一个具体 Browser Profile，而是使用统一测试方法比较 Brave、Chrome、Edge、Firefox、Safari、Tor、Mullvad 等不同浏览器在默认设置下的隐私保护能力。

**主要特点：** 它重点测试不同浏览器是否真正隔离可用于跨站追踪的状态，包括 State Partitioning 等机制。因此它提供的是浏览器产品本身抗追踪和数据泄漏能力的横向比较，而不是单个设备的 Fingerprint 检查。

### 26. BrowserAudit

**官方网站：** https://browseraudit.com/

**网站介绍：** BrowserAudit 是一个专门测试浏览器安全标准和安全功能实现情况的平台。它关注浏览器是否正确实现 Web Security Mechanisms，而不是传统意义上的 Canvas、WebGL 或 IP Fingerprinting。

**主要特点：** BrowserAudit 包含 400 多项自动化测试，运行完成后会生成针对当前浏览器的安全报告。其检测范围涉及 Same-Origin Policy、CSP、CORS、Cookies 和其他 Web Security Mechanisms，因此对于研究浏览器自身安全实现差异具有独立价值。

### 27. Ethical Red

**官方网站：** https://www.ethicalred.io/

**网站介绍：** Ethical Red 是一个专门检查 Browser、VPN 和网络路径泄漏的隐私诊断工具，检测覆盖 WebRTC、DNS、IPv6、Fingerprint Surface、STUN 和 VPN Tunnel 等多个网络暴露面。

**主要特点：** Ethical Red 将 STUN Exposure 与普通 WebRTC Leak 分开报告，同时分析 DNS 路径、IPv6 Path 和 VPN Tunnel Integrity，并进一步关注 UDP 流量是否正确通过 VPN，以及是否存在 Split Tunneling。

### 28. PrivacyTestLab

**官方网站：** https://privacytestlab.com/

**网站介绍：** PrivacyTestLab 是一个综合型浏览器与网络隐私检测平台，提供 Browser Fingerprint、Canvas Fingerprint、IP Leak、DNS Leak、WebRTC Leak 和 Proxy/VPN Detection 等测试，可以查看当前浏览器和网络实际暴露的信息。

**主要特点：** PrivacyTestLab 比较特别的一点是主动公开 Browser Fingerprint Score 的计算方法，包括 Shannon Entropy、不同 Signal 的权重以及评分逻辑。因此用户不仅可以看到一个 Fingerprint Score，还可以理解这个分数为什么这样产生。

### 29. Privacy.net Analyzer

**官方网站：** https://privacy.net/analyzer/

**网站介绍：** Privacy.net Analyzer 用于演示普通网站在用户访问页面时能够获得哪些浏览器和身份相关信息。测试被分成 Basic Info、Autofill Leak Test、User Account Tests、Browser Capability Test 和 Fingerprint Analysis 等多个部分。

**主要特点：** 它提供两个普通 Fingerprint Checker 很少涉及的方向。Autofill Leak Test 可以展示浏览器自动填充可能泄露 Email、地址、Phone、Postal Code 和 City；User Account Tests 则用于检查浏览器中是否存在能够暴露用户登录状态的痕迹。

### 30. TraceScope

**官方网站：** https://tracescope.org/

**网站介绍：** TraceScope 是一个浏览器指纹与网络环境诊断平台，用于检查当前浏览器在网站看来呈现出的设备、网络和身份信息。检测内容包括公网 IP、ISP/ASN、Proxy、WebRTC、DNS、User-Agent、Client Hints、操作系统、Canvas、WebGL、WebGPU、Audio、ClientRects、Fonts、屏幕、时区、语言和自动化特征等，并通过 Browser Fingerprint Consistency 帮助判断不同信号之间是否形成合理一致的浏览器环境。

**主要特点：** TraceScope 比较特别的地方是强调检测结论的证据链。它会分别比较服务器实际收到的 HTTP User-Agent 与 JavaScript 读取到的浏览器身份，并列出 Automation、Runtime 和其他 Modification Traces，解释为什么当前环境被判断为正常或疑似修改。网站还设置了独立的 Fingerprint Browser Brand Detection：只有检测到可验证的产品标记时才尝试识别具体指纹浏览器品牌，而不会仅凭普通 Chromium 特征进行品牌归因。

## 总结

浏览器指纹并不是单一的 Canvas、WebGL 或某一个 Fingerprint Hash，而是浏览器、操作系统、硬件、网络协议、访问环境和行为信号共同形成的一套可识别特征。不同检测网站观察的是这个身份体系中的不同层级，因此一个工具即使显示“正常”，也不代表浏览器、网络和数字身份在其他检测层面同样没有异常。

如果只是希望快速检查一个浏览器环境是否存在明显问题，可以优先使用 **BrowserScan、Pixelscan、Iphey 或 Whoer**，从浏览器、IP、DNS、WebRTC、时区、语言和 Proxy 等多个维度快速判断整体环境。如果进一步需要检查不同信号之间是否存在冲突、浏览器是否留下修改痕迹，或者 HTTP 与 JavaScript 获取到的身份信息是否一致，可以结合 **TraceScope、Fingerprint-Scan、CreepJS 和 WebBrowserTools** 进行更深入的环境一致性、Fingerprint Spoofing 和 Modification Traces 分析。

如果需要查看更加底层的技术数据，**BrowserLeaks、TLS.Peet.ws 和 Browserize / PrivacyCheck** 可以进一步分析 TLS、JA3/JA4、HTTP/2、TCP/IP、WebGPU 以及主动和被动 Fingerprinting 等协议与浏览器信号；如果重点是自动化和 Bot Detection，则可以使用 **Incolumitas、Rebrowser Bot Detector、Sannysoft、Device & Browser Info 和 reCAPTCHA v3 Score**，分别从浏览器指纹、CDP/Playwright/Puppeteer 痕迹、经典 WebDriver 特征、用户行为以及外部风控评分等角度进行检查。

网络环境同样是整个识别体系的重要组成部分。**IPLeak、IPQualityScore 和 Ethical Red** 分别适合检查 IP/DNS/WebRTC 泄漏、IP Reputation 与 Fraud Risk，以及 STUN、IPv6 和 VPN Tunnel 等网络路径问题。与此同时，**AmIUnique、EFF Cover Your Tracks、FingerprintJS 和 Fingerprint Pro** 又分别从指纹唯一性、Tracking Resistance、Visitor ID 和持续设备识别等方向说明，一个访问者如何被区分、关联和长期识别。

浏览器之外还存在另一层数字身份风险。**LeaksCheck、Webkay 和 Privacy.net Analyzer** 展示了 Credential、Infostealer Logs、Autofill、登录状态、社交账号和其他身份痕迹如何与浏览器和网络信号共同形成可关联的 Digital Footprint。也就是说，即使浏览器技术指纹本身没有明显异常，外部身份数据仍然可能成为识别和关联访问者的另一条路径。

因此，这 30 款工具并不是 30 个功能相同的 Browser Fingerprint Checker，而是分别覆盖 **浏览器指纹、环境一致性、修改痕迹、网络与协议指纹、Bot/Automation、IP Reputation、Visitor Identification、隐私防护和数字身份暴露** 等不同检测层。将这些结果结合起来看，才能更完整地理解网站能够获得哪些身份信号、这些信号之间是否一致，以及一个浏览器、设备或数字身份为什么可能被识别、关联、追踪或判定为异常。

---

## 原文与维护说明

- WordPress 原文地址：**发布后补充**
- GitHub 版本用于持续维护工具状态、来源和更新记录。
- 本文不是“通过率”或“绕过率”排名；不同工具的评分不能直接横向换算。
- 发现工具失效、改版或新增重要检测维度，欢迎通过 Issue 提交更新建议。
