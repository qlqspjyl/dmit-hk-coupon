# DMIT 香港优惠码：Pro/T1/EB 三条线路的折扣逻辑，附全套餐价格与验证步骤

搜“DMIT 香港优惠码”的人，多数最后都卡在同一个地方：码找到了，粘进结算页点 Validate Code，提示无效。

这事通常不是码过期了，而是码不对口。DMIT 的优惠码是按产品线和付款周期切开的——香港机房里 Pro、T1、EB 是三条独立产品线，季付和年付能用到的折扣也不一样，拿 T1 的码去买 Pro，系统照样拒。

下面把目前还在流传的香港优惠码、它们各自能用在哪个系列、以及三个系列当前的全部套餐价格整理一遍。

## DMIT 的优惠码为什么这么难对上

DMIT 没有一张“长期通用码”。它的做法是把折扣塞进活动码里，活动结束码就失效，只在社区贴子里继续流传。所以你会看到同一个页面里同时躺着好几年前的码。

命名规律其实挺直白，以这条为例：


202510_HKG_TYO_PRO_20OFF_RECURRING


拆开看就是：`202510` 活动时间（2025 年 10 月）、`HKG_TYO` 适用机房（香港和东京）、`PRO` 适用产品线（Premium）、`20OFF` 折扣力度（八折）、`RECURRING` 循环折扣，也就是续费同价，不是只便宜第一期。

只要记住“机房 + 产品线 + 付款周期 + 折扣”这套结构，拿到一条没见过的码，你基本能猜出它能不能用在你的单子上。名字里带 `RECURRING` 的才是长期省钱的，不带的那部分通常只作用于首单。

## 目前可查的香港优惠码及适用范围

下面这几条是中文主机圈里反复出现、且有多个来源提到的。需要说明的是，DMIT 的活动码收放比较频繁，任何一条都可能随时失效，最终能不能用以下单页 Validate Code 的结果为准。

| 优惠码 | 适用产品线 | 折扣 | 付款周期要求 |
| --- | --- | --- | --- |
| `202510_HKG_TYO_PRO_20OFF_RECURRING` | 香港 / 东京 Premium（Pro） | 八折，循环 | 季付及以上 |
| `202510_HKG_TYO_T1_30OFF_RECURRING` | 香港 / 东京 Tier 1 | 七折，循环 | 季付及以上，WEE 不参与 |
| `HKG-EB-V2-ANNUALLY-15OFF-RECUR` | 香港 Eyeball（EB） | 八五折，循环 | 年付，TINY 及以上 |
| `HKG-T1-ANNUALLY-45OFF-RECUR` | 香港 Tier 1 | 最高 45% 折扣 + 配置翻倍 | 年付，限量供应 |
| `2025-EXISTING-CUSTOMER-10OFF` | 全系 | 九折 | 老客户专属，月消费需超过 $3.33 |
| `HKG-EB-UPGRADE-TO-V2-15OFF-RECUR` | 香港 EB 老用户置换 | 八五折 | 需提交工单申请 |

最后两条要单独说一下。`2025-EXISTING-CUSTOMER-10OFF` 不是公开码，是给已有客户用的，新注册账号套不上；`HKG-EB-UPGRADE-TO-V2-15OFF-RECUR` 也只对从旧套餐迁移过来的用户开放，且必须由工作人员手工建单，自己下单是享受不到的。

早前还流传过 `Lite-Annually-Recur-30OFF`（年付七折）和 `Lite-Semi-Annually-Recur-20OFF`（半年付八折）这两条，主要针对香港和日本的大带宽 Lite 系列。不过该系列后来更名为 Standard，套餐结构也调整过，这两条码现在是否仍然生效，需要自己在结算页验证。

👉 [去 DMIT 香港产品页试一下手里的码](https://www.dmit.io/aff.php?aff=12046)

## Pro、T1、EB：香港三条线路差在哪

选错线路，比用错优惠码更亏。三个系列的区别主要在路由，不在 CPU。

香港 Premium（HKG.Pro）是旗舰，电信去程 CN2 GIA 直连香港 CTG，回程同样走 CN2 GIA；联通走 AS4837 + AS10099；移动接香港 CMI。三网都顾到了，到国内主要城市的延迟通常在 50ms 以内。代价是价格，最小配置月付就要 $39.9。

香港 Tier 1（HKG.AS3.T1）走国际线路，接入了 RETN、NTT 这类国际骨干，香港到欧洲的延迟表现不错，但没有针对中国大陆做任何优化。如果你的用户在国内，别买这条——电信联通可能出现延迟比美国机器还高的情况。它的优势是带宽和流量给得足，最低 4Gbps 端口，最高到 10Gbps。

香港 Eyeball（HKG.EB）夹在中间。回程走联通 CUG + CMI 动态负载、移动 CMI、电信 163，去程电信走 CN2，联通和移动未做优化。价格比 Pro 低一档，流量额度比同价位 Pro 高出不少。

有一点必须提醒：DMIT 官方至今仍把香港 Eyeball Network 标记为 Beta，路由和性能处于持续调整中，官方自己也不建议用在稳定性要求高的生产环境。拿一次测速结果当成长期线路状态，是不靠谱的。

| 对比项 | HKG.Pro | HKG.T1 | HKG.EB |
| --- | --- | --- | --- |
| 中国大陆优化 | 三网 CN2 GIA 直连 | 无 | 部分（回程 CMI 为主） |
| 端口带宽 | 1Gbps | 4–10Gbps | 500Mbps–1Gbps |
| 起步价 | $39.9/月 | $6.9/月 | $24.9/月 |
| 超量后 | 规则以结算页为准 | 降速不停机 | 规则以结算页为准 |
| 稳定性说明 | 生产环境可用 | 生产环境可用 | 官方标注 Beta |

Tier 1 的“降速不停机”值得单独讲：WEE 套餐流量用完后降到 50Mbps 继续跑，TINY 降到 100Mbps，更高配置降到 1Gbps，不会直接断服务。月底不用盯着流量报警。

## DMIT 香港全套餐价格表

价格采集自 DMIT 官方结算与产品页面，不同时期可能有平台迁移和调价，下单时以结算页显示为准。

### 香港 Premium（Pro，AN5 平台，AMD EPYC 9005）

| 套餐 | vCPU | 内存 | SSD | 月流量 / 带宽 | 月付价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| TINY | 1 核 | 1GB | 20GB | 500GB @ 1Gbps | $39.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.tiny&aff=12046) |
| STARTER | 1 核 | 2GB | 40GB | 1TB @ 1Gbps | $79.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.starter&aff=12046) |
| MINI | 2 核 | 2GB | 80GB | 1.5TB @ 1Gbps | $149.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.mini&aff=12046) |
| MICRO | 2 核 | 4GB | 160GB | 2TB @ 1Gbps | $199.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.micro&aff=12046) |
| MEDIUM | 4 核 | 4GB | 160GB | 2.5TB @ 1Gbps | $279.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.medium&aff=12046) |
| LARGE | 4 核 | 8GB | 320GB | 3TB @ 1Gbps | $359.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.large&aff=12046) |
| GIANT | 8 核 | 16GB | 640GB | 6TB @ 1Gbps | $759.90 | [查看 Premium 套餐](https://www.dmit.io/cart.php?region=hong-kong&generation=an5&network=premium&product=hkg.an5.pro.giant&aff=12046) |

这组套餐原本跑在 AS3（AMD EPYC 7003）平台上，后来陆续升级到 AN5 平台，价格没跟着涨。如果你在别的页面看到 $119.9、$126.9 这类数字，那是升级前的旧价，已经不作数了。

### 香港 Tier 1（HKG.AS3.T1，国际线路）

| 套餐 | vCPU | 内存 | SSD | 月流量 / 带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| WEE | 1 核 | 1GB | 20GB | 1TB @ 4Gbps | $36.90/年 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| TINY | 1 核 | 1GB | 20GB | 2TB @ 4Gbps | $6.90/月，$76.90/年 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| STARTER | 1 核 | 2GB | 40GB | 4TB @ 10Gbps | $12.90/月，$154.80/年 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| MINI | 2 核 | 2GB | 60GB | 8TB @ 10Gbps | $21.90/月，$262.80/年 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| MICRO | 4 核 | 4GB | 80GB | 16TB @ 10Gbps | $32.90/月 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| MEDIUM | 4 核 | 8GB | 160GB | 32TB @ 10Gbps | $49.90/月 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| LARGE | 8 核 | 16GB | 320GB | 64TB @ 10Gbps | $99.90/月 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| GIANT | 8 核 | 24GB | 640GB | 128TB @ 10Gbps | $199.90/月 | [查看 Tier 1 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |

WEE 只提供年付，也是整个香港机房最便宜的一档。注意七折码的适用范围明确排除了 WEE，买这一档就别指望再叠折扣了。

### 香港 Eyeball（HKG.AS3.EB，Beta）

| 套餐 | vCPU | 内存 | SSD | 月流量 / 端口 | 月付价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| WEE | 1 核 | 1GB | 20GB | 500GB @ 500Mbps | $24.90 | [查看 Eyeball 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| TINY | 1 核 | 1GB | 20GB | 800GB @ 1Gbps | $39.90 | [查看 Eyeball 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| STARTER | 1 核 | 2GB | 40GB | 1.5TB @ 1Gbps | $79.90 | [查看 Eyeball 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| MINI | 2 核 | 4GB | 60GB | 2.2TB @ 1Gbps | $126.90 | [查看 Eyeball 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| MICRO | 4 核 | 4GB | 80GB | 3TB @ 1Gbps | $179.90 | [查看 Eyeball 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |
| MEDIUM | 4 核 | 8GB | 160GB | 4TB @ 1Gbps | $239.90 | [查看 Eyeball 套餐](https://www.dmit.io/cart.php?region=hong-kong&aff=12046) |

EB 系列同时提供 AS3 和 AN5 两个平台，AN5 版本配置更高、起步价也更高（4 核 4GB 档位约 $149.9/月），且库存波动比较大，经常出现某一档缺货的情况。香港 Pro 的常规型号也一样，尤其是低配，补货节奏不好预测，看到有货再犹豫往往就没了。

## 优惠码具体怎么用

流程本身没难度，DMIT 用的是 WHMCS 那套结算系统：

1. 从产品页选好机房、线路系列和具体配置。
2. 选付款周期。这一步决定了哪些码能用——季付和年付能用的码不一样，月付基本都享受不到循环折扣。
3. 点 Continue 进入结算页。
4. 在右侧的 Apply Promo Code 输入框填码，点 Validate Code。
5. 价格立刻刷新，确认无误再付款。

支付方式支持支付宝、PayPal 和信用卡，对国内用户来说支付宝这一步省事不少。

👉 [带着优惠码去 DMIT 结算页验证](https://www.dmit.io/aff.php?aff=12046)

## 几个容易踩的坑

**码不对产品线。** 这是最常见的问题。T1 的七折码套不到 Pro 上，Pro 的八折码也套不到 T1 上，名字里就写着呢。

**忽略季付门槛。** 好几条码都要求季付及以上，月付下单再填码必然报错。如果你本来就打算长期用，季付或年付的门槛反而不是问题。

**把限量特价和优惠码混着算。** DMIT 每次上新品会放一批首发限量套餐，这类特价通常明确写着“无优惠码”，价格本身就是折后价，别再试图叠码。

**以为循环折扣会一直自动续。** `RECURRING` 的意思是续费同价，但这建立在优惠码政策不变的前提下。DMIT 保留调整活动条件的权利，长期账单还是建议定期回看一次。

**拿 T1 的测速当 Pro 的参考。** 这两条线路的国内表现差距很大，测速 IP 也不一样。香港 Premium 可以用 103.117.100.199，Tier 1 可以用 154.12.176.28，Eyeball 是 154.12.188.3。买之前先自己 ping 一下，比看任何测评都准。

## 常见问题

**新用户能拿到折扣吗？**
能，但只能靠公开活动码。`2025-EXISTING-CUSTOMER-10OFF` 这类客户专属码需要历史消费记录，新账号验证不通过。

**年付一定比月付划算吗？**
不绝对，但通常是的。以 T1.STARTER 为例，月付 $12.9，年付 $154.8 折合每月 $12.9 左右，本身没有价格差；真正拉开差距的是年付可叠加的循环折扣码，像七折、45% 这类力度基本只对年付开放。要不要为了折扣锁定一年，取决于你对这条线路的确定性。

**值得为香港 Pro 多花钱吗？**
看你用户在哪。用户主要在国内、对延迟和丢包敏感，Pro 的三网 CN2 GIA 是实打实的差距，钱花得值。业务面向海外，或者你手上已经有中转方案，T1 用更低的钱拿到 4–10Gbps 端口和几 TB 流量，没必要硬上 Pro。

**客服是中文吗？**
有资料提到 DMIT 已经取消了独立中文支持团队，统一走英文工单。技术沟通没障碍的话问题不大，需要中文实时沟通的要有心理准备。

**机器缺货怎么办？**
香港 Pro 的低配档和 EB 系列缺货比较频繁。想等的话可以定期看一下产品页补货状态，急用就选当时有货的那一档，配置差一档通常比等一周更划算。

最后提醒一句：上面所有价格和优惠码都来自公开的产品页与活动信息，DMIT 调整得比较勤——平台从 AS3 换到 AN5、系列更名、活动码上下线都发生过。下单那一刻结算页上显示的价格，才是唯一算数的价格。
