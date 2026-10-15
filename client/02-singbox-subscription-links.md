# 02 · 机场订阅链接怎么导入

> 网站版（更长、含繁体与英文）：https://www.leotun.com/zh-CN/guides/singbox-subscription?utm_source=github&utm_content=client-02

机场给的"订阅链接"就是一个 HTTPS 地址，客户端从那里下载一份完整配置——服务器、端口、凭据都在里面，不用手填。雷腾的流量伪装（Hiddify）给的是同一种东西，而且三种格式都直接给，Hiddify、Clash、Shadowrocket 各拿各的，不用转换。

## 弹窗里的三个按钮

登录网站 → 流量伪装页面 → 点地区国旗，弹出二维码，二维码下面是三个按钮。按钮**按订阅类型分**，不按操作系统分，手机和电脑看到的是同一组：

| 按钮上写的客户端 | 副标题 | 点了复制到什么 |
|---|---|---|
| Hiddify / sing-box / GUI.for.SingBox / Karing | sing-box 订阅 | 手机上是 `sing-box://import-remote-profile?url=…` 导入链接，能唤起 App；电脑上是 `https://…` 配置地址，粘贴用。配置里已含分流规则和拒绝 IPv6 的规则，不需要再套"订阅模板" |
| Clash Meta / Clash Verge / FlClash / Stash / Mihomo Party / Clash Nyanpasu / ClashX Meta / OpenClash | Clash 订阅 | Clash 格式（YAML）的订阅地址，粘贴到客户端的订阅 / 配置列表里 |
| NekoBox / Shadowrocket / v2rayN / v2rayNG / Streisand / V2Box / Loon / Egern / Husi / NekoRay / Pharos Pro / Bedlam / Furious / daed / Lumen KVN / Kitty Pro | 分享链接 | 一行 `hysteria2://…`，只带节点，不带分流规则 |

- 按钮上的名字一行放不下时会循环滚动，这是正常的。
- **点哪个按钮，上面的二维码就切换成哪种类型**，对应的客户端可以直接扫。弹窗刚打开时二维码是 Hiddify / sing-box 的，别的客户端直接扫会提示"无效的二维码"——先点自己客户端所在的按钮，再扫码或粘贴。
- 页面上方的"导入所有自动选择"弹窗只有前两个按钮，没有分享链接。

**订阅转换**：把一种格式转成另一种的第三方网站。雷腾三种格式都直接给，**不需要转换**；把带凭据的链接交给转换站等于把账号交给第三方，别这么做。

## Hiddify / sing-box 系：第一个按钮

1. 装 Hiddify（安卓：网站下载页或 Google Play；iOS：App Store；桌面版有 Windows / macOS / Linux）。自带 sing-box 内核。
2. 点地区国旗，弹出二维码。
3. 手机：点第一个按钮，切到 Hiddify 它会提示从剪贴板添加；或者用另一台设备上 Hiddify 的"扫描二维码"。电脑：点同一个按钮，复制到的是 https:// 地址，在 Hiddify 里"+" → "从剪贴板添加"，保存。
4. 点连接，首次允许 VPN 权限。要加地区就再点一个国旗，每个地区是一份独立配置。

## Clash 系：第二个按钮

Clash Meta（mihomo）、Clash Verge、FlClash、Stash 等点"Clash 订阅"按钮，把复制到的地址粘贴进客户端的订阅 / 配置列表，不需要订阅转换。

**Clash 系不要用分享链接**：它们没法把单独一行 `hysteria2://` 当成配置导入。

## 其他客户端：第三个按钮

点"分享链接"按钮，在 NekoBox / Shadowrocket / v2rayN / v2rayNG 等客户端里"从剪贴板导入"，或者点完按钮后扫上面的二维码。分享链接不带规则，分流和 IPv6 要自己设：海外看国内内容的，把国内域名设成走节点、关闭 IPv6。

按钮上 v2rayN 之后的那些客户端都支持 hysteria2，但分享链接用了 hysteria2 的扩展写法，少数客户端解析不了；导入失败或连不上，就换 Hiddify。

## 用不了的客户端

| 客户端 | 原因 |
|---|---|
| Surge | 支持 hysteria2，但只读它自己的配置格式，三种类型都对不上 |
| Quantumult X | 不支持这种线路 |
| 原版 Clash、Clash for Windows | 内核没有 hysteria2，换用 mihomo 内核的客户端 |

## 订阅会过期吗

- **不会因时间过期。** 订阅地址里的令牌跟账号绑定，账号在有效期内就一直能用；续费、切档都不用重导。
- **改密码会让旧地址立刻失效**——用来在手机丢失或链接外泄时收回访问权，改完重新扫码。
- **到期后**返回 401，续费后原配置不用换。
- **2026 年 9 月以前导入的**缺拒绝 IPv6 的规则，删掉重导。

导入了连不上，见[排障 04](../troubleshooting/04-singbox-import-not-connecting.md)。

## 常见问题

**Hiddify 订阅和 Clash 订阅有什么区别？** 格式不同（JSON vs YAML），客户端互不认对方的订阅，但节点本身通用。两种雷腾都直接给：Clash 系客户端点"Clash 订阅"按钮，不要用分享链接。

**一份配置能包含所有地区吗？** 点国旗导入的是每个地区一份，在客户端配置列表里切换，这样某个地区换地址只影响它自己。想一次导入境外全部地区、由客户端自动选，点页面上方的"导入所有自动选择"（只有 sing-box 订阅和 Clash 订阅两个按钮）。

**二维码能发给家人吗？** 二维码含你的账号凭据，发给谁就是把账号给谁。家人共用允许（按档位个人 2 台、家庭 4 台、企业 8 台同时在线），别发到公开的地方；泄露了改密码即失效。

---
由 [雷腾](https://www.leotun.com/zh-CN?utm_source=github&utm_content=client-02) 团队整理 · 问题来 [联系页面](https://www.leotun.com/zh-CN/contact?utm_source=github&utm_content=client-02)（群、邮件、客服都在上面） · 注册领 24 小时免费试用，邀请朋友付费，双方各得 20 天个人档有效期，长期有效
