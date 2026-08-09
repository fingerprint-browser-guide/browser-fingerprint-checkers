# 图片文件与 Alt/Caption 建议

建议将 30 张官网截图统一放在 `assets/screenshots/`。当前 README 暂不引用这些截图，避免在文件尚未上传时产生坏链。

## 1. BrowserScan

- 建议文件名：`01-browserscan.png`
- Alt：BrowserScan 官网截图，展示综合环境检测相关功能
- Caption：BrowserScan：浏览器、硬件、IP、DNS、WebRTC、TLS；特点是环境一致性 + JA3/JA4/HTTP2。

## 2. Pixelscan

- 建议文件名：`02-pixelscan.png`
- Alt：Pixelscan 官网截图，展示综合环境检测相关功能
- Caption：Pixelscan：Fingerprint、IP、Proxy、VPN、DNS、Bot；特点是多维环境检测 + Android Checker。

## 3. Iphey

- 建议文件名：`03-iphey.png`
- Alt：Iphey 官网截图，展示环境可信度检测相关功能
- Caption：Iphey：Fingerprint、IP、VPN、Bot、DNS；特点是强调不同信号之间的一致性。

## 4. Fingerprint-Scan

- 建议文件名：`04-fingerprint-scan.png`
- Alt：Fingerprint-Scan 官网截图，展示Fingerprint/Bot相关功能
- Caption：Fingerprint-Scan：浏览器指纹、IP Reputation、Proxy；特点是将指纹异常直接用于 Bot 风险判断。

## 5. Whoer

- 建议文件名：`05-whoer.png`
- Alt：Whoer 官网截图，展示匿名环境检测相关功能
- Caption：Whoer：IP、DNS、WebRTC、Proxy、Timezone、UA；特点是将多种环境不一致直接转化为风险项。

## 6. DeviceInfo.me

- 建议文件名：`06-deviceinfo-me.png`
- Alt：DeviceInfo.me 官网截图，展示设备信息分析相关功能
- Caption：DeviceInfo.me：浏览器、OS、硬件、GPU、Fonts、TLS；特点是True Browser/OS 与 Fingerprinting Resistance。

## 7. BrowserLeaks

- 建议文件名：`07-browserleaks.png`
- Alt：BrowserLeaks 官网截图，展示深度技术检测相关功能
- Caption：BrowserLeaks：Canvas、WebGL、WebGPU、TLS、HTTP、TCP；特点是JA4T、HTTP/2、QUIC/HTTP3 等协议层检测。

## 8. CreepJS

- 建议文件名：`08-creepjs.png`
- Alt：CreepJS 官网截图，展示高级指纹分析相关功能
- Caption：CreepJS：Browser API、Worker、Canvas、WebGL、Audio；特点是Lies、Resistance、Headless、Stealth。

## 9. Device & Browser Info

- 建议文件名：`09-device-browser-info.png`
- Alt：Device & Browser Info 官网截图，展示Fingerprint/Bot相关功能
- Caption：Device & Browser Info：WebDriver、CDP、Headers、WebGL、Behavior；特点是同时检查静态指纹和用户行为。

## 10. WebBrowserTools

- 建议文件名：`10-webbrowsertools.png`
- Alt：WebBrowserTools 官网截图，展示指纹修改检测相关功能
- Caption：WebBrowserTools：Canvas、WebGL、WebGPU、ClientRects；特点是Fixed/Random Noise Detection。

## 11. Browserize / PrivacyCheck

- 建议文件名：`11-browserize-privacycheck.png`
- Alt：Browserize / PrivacyCheck 官网截图，展示指纹研究相关功能
- Caption：Browserize / PrivacyCheck：Active/Passive Fingerprinting；特点是ETag、JSEcho、Header Signature、HTTP2。

## 12. AmIUnique

- 建议文件名：`12-amiunique.png`
- Alt：AmIUnique 官网截图，展示指纹唯一性相关功能
- Caption：AmIUnique：Browser Fingerprint；特点是Global Statistics + Fingerprint History。

## 13. EFF Cover Your Tracks

- 建议文件名：`13-eff-cover-your-tracks.png`
- Alt：EFF Cover Your Tracks 官网截图，展示隐私/追踪检测相关功能
- Caption：EFF Cover Your Tracks：Tracking、Fingerprintability；特点是同时分析 Tracker Protection。

## 14. FingerprintJS OSS Demo

- 建议文件名：`14-fingerprintjs-oss.png`
- Alt：FingerprintJS OSS Demo 官网截图，展示Visitor Identification相关功能
- Caption：FingerprintJS OSS Demo：客户端 Browser Signals；特点是可实际部署的开源指纹算法。

## 15. Fingerprint Pro Playground

- 建议文件名：`15-fingerprint-pro.png`
- Alt：Fingerprint Pro Playground 官网截图，展示Device Intelligence相关功能
- Caption：Fingerprint Pro Playground：浏览器、网络、设备、Smart Signals；特点是客户端 + 服务端持续设备识别。

## 16. Incolumitas Bot Detector

- 建议文件名：`16-incolumitas.png`
- Alt：Incolumitas Bot Detector 官网截图，展示Bot Detection相关功能
- Caption：Incolumitas Bot Detector：Browser、TCP/IP、TLS、Behavior；特点是行为分类 + 多层指纹。

## 17. Rebrowser Bot Detector

- 建议文件名：`17-rebrowser-bot-detector.png`
- Alt：Rebrowser Bot Detector 官网截图，展示Automation Detection相关功能
- Caption：Rebrowser Bot Detector：Chromium、CDP、Puppeteer、Playwright；特点是专攻现代 CDP/Automation Leak。

## 18. Sannysoft

- 建议文件名：`18-sannysoft.png`
- Alt：Sannysoft 官网截图，展示经典 Bot Benchmark相关功能
- Caption：Sannysoft：WebDriver、Headless、Plugins、WebGL；特点是行业常用经典自动化基准。

## 19. AntCpt reCAPTCHA v3 Score

- 建议文件名：`19-antcpt-recaptcha.png`
- Alt：AntCpt reCAPTCHA v3 Score 官网截图，展示外部风控检测相关功能
- Caption：AntCpt reCAPTCHA v3 Score：reCAPTCHA v3；特点是直接观察 Google 风控评分。

## 20. TLS.Peet.ws / TrackMe

- 建议文件名：`20-tls-peet-ws.png`
- Alt：TLS.Peet.ws / TrackMe 官网截图，展示协议指纹相关功能
- Caption：TLS.Peet.ws / TrackMe：TLS、HTTP/2、JA3、JA4；特点是JA3 + JA4 + Akamai + PeetPrint。

## 21. IPLeak

- 建议文件名：`21-ipleak.png`
- Alt：IPLeak 官网截图，展示网络泄漏检测相关功能
- Caption：IPLeak：IP、DNS、WebRTC、Torrent；特点是Torrent Client IP + 端口路由测试。

## 22. IPQualityScore

- 建议文件名：`22-ipqualityscore.png`
- Alt：IPQualityScore 官网截图，展示IP Reputation相关功能
- Caption：IPQualityScore：Proxy、VPN、Tor、Fraud、Abuse；特点是自有网络信誉和欺诈数据。

## 23. LeaksCheck

- 建议文件名：`23-leakscheck.png`
- Alt：LeaksCheck 官网截图，展示数字身份暴露相关功能
- Caption：LeaksCheck：Credential、Infostealer、OSINT；特点是浏览器之外的身份关联和数字足迹。

## 24. Webkay

- 建议文件名：`24-webkay.png`
- Alt：Webkay 官网截图，展示浏览器信息暴露相关功能
- Caption：Webkay：Browser、Hardware、WebRTC、Autofill；特点是Autofill、登录状态、局域网等攻击面。

## 25. PrivacyTests.org

- 建议文件名：`25-privacytests.png`
- Alt：PrivacyTests.org 官网截图，展示浏览器隐私比较相关功能
- Caption：PrivacyTests.org：浏览器默认隐私防护；特点是统一方法横向比较不同浏览器。

## 26. BrowserAudit

- 建议文件名：`26-browseraudit.png`
- Alt：BrowserAudit 官网截图，展示浏览器安全检测相关功能
- Caption：BrowserAudit：SOP、CSP、CORS、Cookies 等；特点是检查浏览器安全标准实现。

## 27. Ethical Red

- 建议文件名：`27-ethical-red.png`
- Alt：Ethical Red 官网截图，展示网络路径检测相关功能
- Caption：Ethical Red：WebRTC、STUN、DNS、IPv6、VPN；特点是STUN + VPN Tunnel Integrity。

## 28. PrivacyTestLab

- 建议文件名：`28-privacytestlab.png`
- Alt：PrivacyTestLab 官网截图，展示Fingerprint/隐私相关功能
- Caption：PrivacyTestLab：Fingerprint、IP、DNS、WebRTC；特点是公开 Shannon Entropy 与 Signal Weight。

## 29. Privacy.net Analyzer

- 建议文件名：`29-privacy-net-analyzer.png`
- Alt：Privacy.net Analyzer 官网截图，展示身份信息暴露相关功能
- Caption：Privacy.net Analyzer：Fingerprint、Autofill、登录状态；特点是Autofill Leak + User Account Tests。

## 30. TraceScope

- 建议文件名：`30-tracescope.png`
- Alt：TraceScope 官网浏览器指纹检测页面，展示环境一致性、网络信息和浏览器修改痕迹分析
- Caption：TraceScope 浏览器指纹检测页面，可检查浏览器环境一致性、IP、WebRTC、DNS、自动化特征及浏览器修改痕迹。

