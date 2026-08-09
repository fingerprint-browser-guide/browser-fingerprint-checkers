# 来源与证据账本 / Evidence Ledger

最后核查：**2026-08-09**

本文件不只是列出工具官网，而是记录 README 中“为什么该工具值得单独收录”的主要一手来源。优先使用官网检测页、官方文档和官方代码仓库；若某项只有单一公开入口，则只记录能够直接支持当前描述的页面，不为凑数量添加弱来源。

> `Claims supported` 只说明这些来源能够支持 README 中的功能描述，不代表本项目独立验证了检测准确率、误报率或第三方平台的实际判定。

## 1. BrowserScan

- **Official entry:** https://www.browserscan.net/
- **HTTP/2 / SSL / TLS:** https://www.browserscan.net/tls
- **WebGPU Browser Report:** https://www.browserscan.net/webgpu
- **Tool index:** https://www.browserscan.net/tools
- **Claims supported:** 综合环境检测；HTTP/2/Akamai 指纹；JA3/JA4；WebGPU。
- **Last verified:** 2026-08-09

## 2. Pixelscan

- **Official entry:** https://pixelscan.net/
- **About / Manifest:** https://pixelscan.net/manifest
- **Fingerprint Check:** https://pixelscan.net/fingerprint-check
- **Bot Check:** https://pixelscan.net/bot-check
- **Changelog:** https://pixelscan.net/changelog
- **Claims supported:** 综合 Fingerprint/IP/Proxy/DNS/Bot 检测；Android Checker；Bot 检测；持续更新记录。
- **Last verified:** 2026-08-09

## 3. Iphey

- **Official entry:** https://iphey.com/
- **Browser fingerprint explainer:** https://iphey.com/blog/what-is-a-browser-fingerprint
- **Claims supported:** Fingerprint、IP/VPN/Bot/DNS 检测；Trust Score 与时区/IP/自动化异常说明。
- **Last verified:** 2026-08-09

## 4. Fingerprint-Scan

- **Official entry:** https://fingerprint-scan.com/
- **HTTP Headers:** https://fingerprint-scan.com/http_headers
- **Browser Extensions:** https://fingerprint-scan.com/browser_extensions
- **Canvas fingerprint:** https://fingerprint-scan.com/canvas
- **Claims supported:** Browser Fingerprint 与 Bot Risk Score；User-Agent/真实浏览器差异；扩展与 Canvas 信号。
- **Last verified:** 2026-08-09

## 5. Whoer

- **Official entry:** https://whoer.net/
- **Browser fingerprint check explainer:** https://api.whoer.net/blog/fingerprint-browser-check/
- **Claims supported:** IP、DNS、WebRTC、浏览器指纹与环境不一致提示。
- **Last verified:** 2026-08-09

## 6. DeviceInfo.me

- **Official entry:** https://www.deviceinfo.me/
- **Claims supported:** 设备/浏览器/网络原始信息；True Browser Core、True OS Core、Fingerprinting Resistance、Canvas/AudioContext 状态。
- **Last verified:** 2026-08-09

## 7. BrowserLeaks

- **Official entry:** https://browserleaks.com/
- **TLS / JA3 / JA4:** https://browserleaks.com/tls
- **HTTP/2 fingerprint:** https://browserleaks.com/http2
- **QUIC / HTTP/3:** https://browserleaks.com/quic
- **Chrome Extension Detection:** https://browserleaks.com/chrome
- **Claims supported:** 模块化浏览器指纹；JA3/JA4；JA4T/TCP；HTTP/2；QUIC/HTTP3；扩展检测。
- **Last verified:** 2026-08-09

## 8. CreepJS

- **Official entry:** https://abrahamjuliot.github.io/creepjs/
- **Fingerprint signal index:** https://creepjs.org/fingerprint
- **API Playground:** https://creepjs.org/playground
- **Claims supported:** Headless、Stealth、Resistance、Worker、JS Proxy 与 Lies Detection 等高级信号。
- **Last verified:** 2026-08-09

## 9. Device & Browser Info

- **Official entry:** https://deviceandbrowserinfo.com/are_you_a_bot
- **Behavioral bot test:** https://deviceandbrowserinfo.com/are_you_a_bot_interactions
- **Site / research hub:** https://deviceandbrowserinfo.com/
- **Claims supported:** WebDriver、CDP、iframe/主线程异常、客户端/服务端指纹以及行为检测。
- **Last verified:** 2026-08-09

## 10. WebBrowserTools

- **Official entry:** https://webbrowsertools.com/
- **Canvas spoof detection:** https://webbrowsertools.com/canvas-fingerprint/
- **WebGL spoof detection:** https://webbrowsertools.com/webgl-fingerprint/
- **WebGPU spoof detection:** https://webbrowsertools.com/webgpu-fingerprint/
- **ClientRects spoof detection:** https://webbrowsertools.com/clientrects-fingerprint/
- **Claims supported:** Canvas/WebGL/WebGPU/ClientRects 的固定或随机 Noise / Spoof 检测。
- **Last verified:** 2026-08-09

## 11. Browserize / PrivacyCheck

- **Official entry:** https://privacycheck.sec.lrz.de/
- **HTTP/2 fingerprinting:** https://privacycheck.sec.lrz.de/passive/fp_h2/fp_http2.html
- **ETag fingerprinting:** https://privacycheck.sec.lrz.de/passive/fp_etag/fp_etag.php
- **JSEcho:** https://privacycheck.sec.lrz.de/active/fp_je/fp_js_echo.html
- **Header Signature:** https://privacycheck.sec.lrz.de/passive/fp_hs/fp_header_signature.php
- **Claims supported:** Active/Passive Fingerprinting；HTTP/2、ETag、JSEcho、Header Signature。
- **Last verified:** 2026-08-09

## 12. AmIUnique

- **Official entry:** https://amiunique.org/
- **Global Statistics:** https://amiunique.org/fingerprints-global-statistics
- **Fingerprint History:** https://amiunique.org/fingerprint/history
- **Privacy Policy:** https://www.amiunique.org/privacy-policy
- **Claims supported:** 指纹唯一性、全球样本统计、历史变化与数据收集边界。
- **Last verified:** 2026-08-09

## 13. EFF Cover Your Tracks

- **Official entry:** https://coveryourtracks.eff.org/
- **About:** https://coveryourtracks.eff.org/about
- **Learn:** https://coveryourtracks.eff.org/learn
- **Results explanation:** https://coveryourtracks.eff.org/results-nojs
- **Privacy Policy:** https://coveryourtracks.eff.org/privacy
- **Claims supported:** Tracker Protection、Fingerprintability、样本唯一性解释与隐私政策。
- **Last verified:** 2026-08-09

## 14. FingerprintJS OSS Demo

- **Official entry:** https://fingerprintjs.github.io/fingerprintjs/
- **Official repository:** https://github.com/fingerprintjs/fingerprintjs
- **API reference:** https://github.com/fingerprintjs/fingerprintjs/blob/master/docs/api.md
- **Claims supported:** 开源客户端 Fingerprinting Library；visitorId；API 与开源实现。
- **Last verified:** 2026-08-09

## 15. Fingerprint Pro Playground

- **Official entry:** https://demo.fingerprint.com/playground
- **Product introduction:** https://docs.fingerprint.com/docs/introduction
- **Identify visitors:** https://docs.fingerprint.com/docs/identify-visitors
- **Smart Signals:** https://docs.fingerprint.com/docs/smart-signals-introduction
- **Claims supported:** 服务端 Visitor Identification；Visitor ID；Smart Signals；Bot/VPN/Tampering 等设备智能。
- **Last verified:** 2026-08-09

## 16. Incolumitas Bot Detector

- **Official entry:** https://bot.incolumitas.com/
- **TCP/IP fingerprint:** https://bot.incolumitas.com/tcpip.html
- **Claims supported:** Behavioral Bot Classification；Browser/TCP-IP/TLS/Proxy-VPN 等多层 Bot 检测。
- **Last verified:** 2026-08-09

## 17. Rebrowser Bot Detector

- **Official entry:** https://bot-detector.rebrowser.net/
- **Official repository:** https://github.com/rebrowser/rebrowser-bot-detector
- **Claims supported:** 现代 Puppeteer/Playwright/CDP 自动化泄漏，包括 Runtime.enable、sourceUrl、main-world 等检测。
- **Last verified:** 2026-08-09

## 18. Sannysoft

- **Official entry:** https://bot.sannysoft.com/
- **Claims supported:** WebDriver、Plugins、Languages、WebGL、Canvas 等经典自动化检测基准。
- **Last verified:** 2026-08-09

## 19. AntCpt reCAPTCHA v3 Score

- **Official entry:** https://antcpt.com/eng/information/demo-form/recaptcha-3-test-score.html
- **Score detector:** https://antcpt.com/score_detector/
- **Claims supported:** reCAPTCHA v3 当前站点评分；0.9→更偏人类、0.1→更偏 Bot 的页面说明。
- **Last verified:** 2026-08-09

## 20. TLS.Peet.ws / TrackMe

- **Official entry:** https://tls.peet.ws/
- **API - all data:** https://tls.peet.ws/api/all
- **API - fingerprints:** https://tls.peet.ws/api/clean
- **API - TLS data:** https://tls.peet.ws/api/tls
- **Claims supported:** JA3、JA4、Akamai HTTP Fingerprint、PeetPrint、TLS/HTTP2 原始信息与 API。
- **Last verified:** 2026-08-09

## 21. IPLeak

- **Official entry:** https://ipleak.net/
- **Claims supported:** IP/DNS/WebRTC；Torrent Address Detection；IPv4/IPv6 替代端口与 destination-port routing 检测。
- **Last verified:** 2026-08-09

## 22. IPQualityScore

- **Official entry:** https://www.ipqualityscore.com/ip-reputation-check
- **Proxy/VPN API response fields:** https://www.ipqualityscore.com/documentation/proxy-detection-api/response-parameters
- **Claims supported:** IP Reputation、Proxy/VPN/Tor、Fraud Score、bot_status、recent_abuse 等风险字段。
- **Last verified:** 2026-08-09

## 23. LeaksCheck

- **Official entry:** https://leakscheck.com/
- **API Documentation:** https://leakscheck.com/api/docs
- **Claims supported:** Credential Intelligence、Infostealer Logs、Telegram/OSINT、关联社交账号与 Digital Footprint。
- **Last verified:** 2026-08-09

## 24. Webkay

- **Official entry:** https://webkay.robinlinus.com/
- **Claims supported:** 浏览器可暴露信息；Social Media、Clickjacking、Auto-Fill Phishing、Local Network Scan。
- **Last verified:** 2026-08-09

## 25. PrivacyTests.org

- **Official entry:** https://privacytests.org/
- **About / methodology overview:** https://privacytests.org/about
- **Claims supported:** 统一自动化测试比较不同浏览器默认隐私防护；State Partitioning 与数据泄漏防护。
- **Last verified:** 2026-08-09

## 26. BrowserAudit

- **Official entry:** https://browseraudit.com/
- **Claims supported:** 400+ 浏览器安全实现测试；SOP、CSP、CORS、Cookies、Headers 与历史数据。
- **Last verified:** 2026-08-09

## 27. Ethical Red

- **Official entry:** https://www.ethicalred.io/
- **Claims supported:** WebRTC、STUN、DNS、IPv6、VPN Tunnel Integrity、UDP/Split Tunneling。
- **Last verified:** 2026-08-09

## 28. PrivacyTestLab

- **Official entry:** https://privacytestlab.com/
- **Fingerprint scoring methodology:** https://privacytestlab.com/methodology/
- **IP Leak Test:** https://privacytestlab.com/tools/leak-tests/ip-leak-test
- **Claims supported:** Browser Fingerprint / Leak 测试；Shannon Entropy、Signal Weight、开源评分代码与已公开局限。
- **Last verified:** 2026-08-09

## 29. Privacy.net Analyzer

- **Official entry:** https://privacy.net/analyzer/
- **Privacy Policy:** https://privacy.net/privacy-policy/
- **Claims supported:** Basic Info、Autofill Leak、User Account Tests、Browser Capabilities 与 Fingerprint Analysis。
- **Last verified:** 2026-08-09

## 30. TraceScope

- **Official entry:** https://tracescope.org/
- **WebRTC Leak Check:** https://tracescope.org/tools/webrtc-leak/
- **Claims supported:** Browser Fingerprint Consistency；Server/JavaScript 交叉验证；Modification Traces；Automation；品牌痕迹归因边界。
- **Last verified:** 2026-08-09

