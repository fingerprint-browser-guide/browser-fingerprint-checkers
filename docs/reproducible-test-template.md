# 可复现测试记录模板

复制下方内容，为每个环境建立独立记录。公开前请脱敏。

```yaml
test_id: BF-YYYYMMDD-001
tested_at_utc:
tester:
purpose: privacy | compatibility | regression | authorized-security

environment:
  os_name:
  os_version:
  device_type:
  browser_product:
  browser_version:
  engine_version:
  profile_state: fresh | warmed | reused
  extensions:
  privacy_settings:
  screen_resolution:
  viewport:
  languages:
  timezone:

network:
  connection_type:
  proxy_or_vpn:
  exit_country:
  asn_redacted:
  webrtc_policy:

run:
  tool_name:
  tool_url:
  repetition: 1
  page_version_or_commit:
  raw_evidence_path:

observations:
  ip_dns_webrtc:
  http_tls:
  canvas_webgl_audio_fonts:
  environment_consistency:
  tampering_or_automation:
  uniqueness_or_stability:

interpretation:
  directly_observed:
  possible_explanation:
  not_proven:
  next_control_test:
```

## 最低重复要求

- 同一环境、同一工具连续 3 次；
- 浏览器完整重启后 1 次；
- 浏览器或内核更新后 1 组；
- 每次只改变一个变量；
- 保存原始字段，不只保存首页颜色或总分。

## 隐私检查

- 删除完整 IP、账号、cookie、token、邮箱和客户标识；
- 检查截图中的书签、扩展名、系统用户名和地理位置；
- hash 也可能用于关联同一环境，公开前评估风险；
- 不上传生产环境的完整报告。

