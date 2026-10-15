# 04 · 流量伪装（Hiddify）导入了却连不上

> 网站版（更长、含繁体与英文）：https://www.leotun.com/zh-CN/guides/singbox-subscription?utm_source=github&utm_content=troubleshooting-04

按报错对号入座。导入方法本身见 [机场订阅链接怎么导入](../client/02-singbox-subscription-links.md)。

| 表现 | 原因 | 做法 |
|---|---|---|
| "无法获取订阅"、401 | 账号到期，或者改过密码（改密码会让旧配置立刻失效，这是设计） | 登录网站看有效期；续费或改完密码后重新扫码 |
| 导入成功，连接超时 | 该地区的地址刚更换，或该入口被运营商干扰 | 客户端里点"更新订阅"拉最新配置；换一个地区，每个地区是独立配置，互不影响 |
| 连上了但没有网 | 客户端自己的分流规则把流量放到"直连" | 默认出站改成该节点，或删掉自加的规则 |
| 扫码提示"无效的二维码" | 弹窗刚打开时二维码是 Hiddify / sing-box 的，别的客户端直接扫会报这个；或从别人截图扫的 | 先点自己客户端所在的按钮，二维码会切换成对应类型，再扫码或粘贴：Clash 系点"Clash 订阅"，Shadowrocket / NekoBox / v2rayN 等点"分享链接"；二维码含你自己的凭据，别人的不能用 |
| 速度慢 | 所选地区负载高，或本地宽带与地区不搭配 | 看网站地区列表的红黄绿灯，换绿灯的地区；还是慢就按运营商换地区 |
| Clash 系客户端导入分享链接失败 | Clash Meta、Clash Verge、FlClash、Stash 等没法把单独一行 hysteria2:// 当成配置导入 | 点"Clash 订阅"按钮，把地址粘贴进客户端的订阅列表；原版 Clash 和 Clash for Windows 内核没有 hysteria2，换用 mihomo 内核的客户端 |
| 分享链接导入失败或连不上 | 分享链接用了扩展写法，少数客户端解析不了 | 换 Hiddify |

## 续费、切档、改密码后要不要重新导入

- **续费、切换档位（个人/家庭/企业）**：不用，原配置继续用。
- **改密码**：旧配置立刻失效，重新扫码。手机丢了、链接外泄就用这个办法收回。
- **账号到期**：配置返回 401；续费后不用换配置，重新连接即可。
- **2026 年 9 月以前导入的**：缺拒绝 IPv6 的规则，海外看国内视频会提示版权限制，删掉重导，见 [03](03-ipv6-and-dns-leak.md)。

## 什么时候找客服

把三样告诉客服：客户端名字和版本、地区、报错原文或截图。

---
由 [雷腾](https://www.leotun.com/zh-CN?utm_source=github&utm_content=troubleshooting-04) 团队整理 · 问题来 [联系页面](https://www.leotun.com/zh-CN/contact?utm_source=github&utm_content=troubleshooting-04)（群、邮件、客服都在上面） · 注册领 24 小时免费试用，邀请朋友付费，双方各得 20 天个人档有效期，长期有效
