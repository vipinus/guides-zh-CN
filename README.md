# 雷顿知识库

> 2026-10-05 起中文名由「蓝盾」改为「雷顿」（英文名 LeoTun 不变），同一家、同一个团队，账号与服务都不变。

跨境访问的原理、场景、客户端设置、路由器与排障，一篇讲一件事，不堆术语。由 [雷顿](https://7d24hrs.com/zh-CN?utm_source=github&utm_content=readme) 团队维护。

其他语言：[繁體中文](https://github.com/vipinus/guides-zh-TW) · [English](https://github.com/vipinus/guides-en)

## 长期福利：免费时长，一直有效

| 怎么领 | 得到什么 |
|---|---|
| 注册后领免费试用 | 24 小时全功能试用，不要信用卡 |
| 邀请朋友注册并首次付费 | 你的有效期 +30 天（家庭档 +15 天、企业档 +7.5 天），每位朋友一次，人数不限 |

网站：<https://7d24hrs.com/zh-CN?utm_source=github&utm_content=readme> · 联系我们：<https://7d24hrs.com/zh-CN/contact?utm_source=github&utm_content=readme>

## 目录

### [回国访问指南 · 需要中国 IP 的那些事](china-access/)

人在海外，很多国内服务会因为你的 IP 不在中国大陆而拒绝：视频、音乐、政务、银行、购票、游戏。一篇一个场景，讲清楚**为什么被拦、怎么解决、还有什么坑**。

| 篇 |
|---|
| [01 · 哪些服务需要中国 IP](china-access/01-what-needs-a-china-ip.md) |
| [02 · 在国外看国内视频](china-access/02-watch-chinese-video-abroad.md) |
| [03 · 上国内政府与公共服务网站](china-access/03-government-and-public-services.md) |
| [04 · 网银、手机银行与支付](china-access/04-banking-and-payments.md) |
| [05 · 音乐、播客与有声书](china-access/05-music-and-audio.md) |
| [06 · 国服游戏与直播](china-access/06-gaming-and-streaming.md) |
| [07 · 在国外看国内家里的监控](china-access/07-home-camera-abroad.md) |
| [08 · 回国线路怎么选：国内 IP 从哪来、免费的坑在哪](china-access/08-how-to-choose-a-china-access-line.md) |
| [09 · 验证码收不到与国内手机号](china-access/09-sms-code-and-china-phone-number.md) |
| [10 · 留学生回国 VPN 怎么配](china-access/10-students.md) |
| [11 · 回国 VPN 免费还是付费](china-access/11-free-vs-paid.md) |
| [12 · 出差旅行怎么配](china-access/12-travel.md) |
| [13 · 微信、支付宝与国内小程序](china-access/13-wechat-alipay-miniprograms.md) |
| [14 · 帮国外的长辈设置：装一次，之后不用管](china-access/14-help-parents-abroad.md) |
| [15 · 网课、考试报名与学历认证](china-access/15-online-courses-and-exams.md) |

### [出海访问指南 · 在国内用海外服务](overseas-access/)

人在国内，办公、开发、学术、游戏、影音要用的海外服务打不开或者极慢。一篇一个场景，讲清楚**要什么、怎么选、有什么坑**。

| 篇 |
|---|
| [01 · 哪些服务需要海外 IP，线路是怎么工作的](overseas-access/01-what-needs-an-overseas-ip.md) |
| [02 · 思科 AnyConnect 在中国能用吗](overseas-access/02-anyconnect-in-china.md) |
| [03 · 在国内选哪个地区最快：按运营商](overseas-access/03-which-region-is-fastest.md) |
| [04 · 公司电脑怎么用：没有管理员权限、已连着公司 VPN](overseas-access/04-office-laptop.md) |
| [05 · Linux 服务器和命令行工具怎么走线路](overseas-access/05-linux-server.md) |
| [06 · 群晖、威联通 NAS 怎么走线路](overseas-access/06-nas-openvpn.md) |
| [07 · 访问 AI 工具（ChatGPT、Claude、Gemini 等）](overseas-access/07-ai-tools.md) |
| [08 · 查文献、下论文、投稿](overseas-access/08-academic-research.md) |

### [网络知识笔记 · Network Guides](network/)

讲清楚跨境访问的**原理**、**六种接入方式怎么选**、我们和别家的区别、怎么识别有风险的软件。不堆术语。

| 篇 |
|---|
| [01 · 回国访问是怎么回事](network/01-why-china-services-block-overseas.md) |
| [02 · 各种连接方式适用的场景](network/02-choose-your-connection-method.md) |
| [03 · 私网（Tailscale）和 VPN 的区别，什么时候该用它](network/03-private-network-vs-vpn.md) |
| [04 · 我们和其他 VPN 的区别](network/04-why-us.md) |
| [05 · 如何识别有风险的 VPN 软件](network/05-risky-vpn-apps.md) |
| [06 · 为什么有时候快、有时候慢](network/06-why-sometimes-fast-sometimes-slow.md) |
| [07 · 哪些问题靠线路解决，哪些要另找办法](network/07-when-you-do-not-need-us.md) |
| [08 · 账号三档怎么选、续费与付款](network/08-account-tiers-and-payment.md) |
| [09 · 连接不够设备用怎么办](network/09-not-enough-devices.md) |

### [客户端安装与设置 · Client Guides](client/)

把每种接入方式**装起来、连上**的一步步说明：思科 AnyConnect、Hiddify、网页代理扩展、OpenVPN、私网 Tailscale，以及 iOS 装不了应用、Telegram / Discord 安装、多设备一次配置、Dropbox 等软件要填代理怎么办。选哪种见 [各种连接方式适用的场景](network/02-choose-your-connection-method.md)，装好了连不上见 [排障](troubleshooting/)。

| 篇 |
|---|
| [01 · 思科 AnyConnect：各平台安装、连接与更新](client/01-anyconnect-install.md) |
| [02 · Hiddify 订阅链接、导入链接、分享链接是什么，要不要"订阅转换"](client/02-singbox-subscription-links.md) |
| [03 · 网页代理：ZeroOmega 扩展两步配好](client/03-web-proxy-extension.md) |
| [04 · OpenVPN：下载 .ovpn 配置导入即连，路由器、NAS、Linux 都能用](client/04-openvpn-profile.md) |
| [05 · 私网（Tailscale）：安装、登录本站控制服务器、选出口](client/05-tailscale-private-network.md) |
| [06 · iOS 装不了应用怎么办](client/06-ios-app-store.md) |
| [07 · Telegram 与 Discord 的安装](client/07-install-telegram-discord.md) |
| [08 · 多设备一次配置、换手机不重来](client/08-multi-device.md) |
| [09 · 伪装（Hiddify）各平台安装：Windows、macOS、Linux、安卓、iOS](client/09-hiddify-install-all-platforms.md) |
| [10 · Dropbox 等软件要填 HTTP / SOCKS 代理怎么办](client/10-app-proxy.md) |

### [路由器与家庭网络指南](router/)

整个家的设备一起走线路：预装路由器上手、自己刷固件、分流原理、电视与老人、绑定与换机。

| 篇 |
|---|
| [01 · 预装路由器怎么开始](router/01-plug-and-play-router.md) |
| [02 · 自己刷固件：从官方固件一步步照着做（附视频）](router/02-flash-firmware-yourself.md) |
| [03 · 路由器分流是什么](router/03-router-split-routing.md) |
| [04 · 给家里老人和电视用](router/04-family-tv-and-router.md) |
| [05 · MAC 绑定与换路由器](router/05-mac-binding-and-replacing.md) |
| [06 · 在国外用路由器解锁国内视频网站](router/06-unlock-chinese-video-with-router.md) |
| [07 · 该不该上路由器，四个型号怎么挑](router/07-which-router-to-buy.md) |
| [08 · 固件装好之后：会自己做的事，和你要知道的几个开关](router/08-what-the-firmware-does.md) |
| [09 · 路由器真分流和假分流有什么区别](router/09-real-vs-fake-split.md) |
| [10 · 路由器后面的 NAS、打印机、摄像头会受影响吗](router/10-nas-printer-camera-behind-router.md) |
| [11 · 千兆、2G 宽带配路由器，速度由什么决定](router/11-fast-broadband-and-router-speed.md) |
| [12 · 路由器断电、断网之后会自己恢复吗](router/12-after-power-cut-or-dropout.md) |

### [排障指南](troubleshooting/)

出问题时按顺序查的清单：连不上、慢、断线，开了回国还是不能看，IPv6 与 DNS 漏网，流量伪装导入了连不上，最后是怎么联系我们。安装类内容已归到 [客户端指南](client/)。

| 篇 |
|---|
| [01 · 连不上、慢、断线的排查清单](troubleshooting/01-cannot-connect-slow-drops.md) |
| [02 · 开了回国还是不能看，怎么办](troubleshooting/02-still-blocked-after-connecting.md) |
| [03 · 连上了视频站还提示版权：IPv6 和 DNS 是漏网之鱼](troubleshooting/03-ipv6-and-dns-leak.md) |
| [04 · 流量伪装（Hiddify）导入了却连不上](troubleshooting/04-singbox-import-not-connecting.md) |
| [05 · 怎么联系我们、怎么不失联](troubleshooting/05-how-to-reach-us.md) |
| [06 · Mac 提示「已损坏」怎么办](troubleshooting/06-antivirus-false-positive.md) |
| [07 · 换手机、换电脑、重装系统之后](troubleshooting/07-new-phone-new-computer.md) |
| [08 · 怎么确认真的连上了、现在从哪个地区出去](troubleshooting/08-am-i-connected.md) |
| [09 · 请客服远程帮你看电脑和路由器](troubleshooting/09-remote-assist.md) |
| [10 · 如何有效沟通 AI 客服](troubleshooting/10-ask-ai-support.md) |

有问题可以在本仓库的 [Discussions](https://github.com/vipinus/guides-zh-CN/discussions) 里提问。

> 本库由原来的六个仓库（china-access-guides、overseas-access-guides、network-guides、client-guides、router-guides、troubleshooting-guides）于 2026-10-04 合并而成，文章内容未改。

## 许可

文字内容采用 [CC BY 4.0](LICENSE)，转载请注明来源并保留链接。
