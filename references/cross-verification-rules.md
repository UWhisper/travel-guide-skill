# Cross-Verification Rules (交叉验证规则)

## Confidence Labels

| Label | Criteria | Example |
|-------|----------|---------|
| ✅ High | 3+ independent sources agree, OR official source (government site, official ticket platform, 12306) | "镇远古镇免费进入" confirmed by 文旅局官网, 马蜂窝, 携程 |
| ⚠️ Medium | 2 independent sources agree, OR single highly authoritative source | "XX餐厅是本地人最爱" — 大众点评 + 小红书 ≥3篇 |
| ⚡ Low | Single source, OR user-generated only, OR training data without external confirmation | "这条小巷拍照最好看" — 仅1篇小红书 |
| ❓ Speculative | No direct source found. Inference from general knowledge or old data. | "端午节应该有龙舟活动" — 未搜索到当前年份确认信息 |

## Source Hierarchy

For each type of information, prefer sources in this order:

### Transport
1. 12306.cn (train schedules — highest authority)
2. Airline official websites
3. Official bus station websites/WeChat accounts
4. Baidu Maps / Amap route data
5. Travel forums (Mafengwo, Qyer) — label ⚠️

### Dining
1. Dianping (大众点评) — most reliable for Chinese destinations
2. Xiaohongshu (小红书) — ≥3 independent posts
3. Douyin local food bloggers — lower weight, higher marketing bias
4. Mafengwo restaurant guides — label ⚠️

### Attractions
1. Official attraction website/WeChat account
2. Local government culture & tourism bureau (文旅局)
3. Ctrip / Qunar ticket pages (for prices)
4. Mafengwo / Qyer travelogues — label ⚠️

### Accommodation
1. Ctrip / Meituan verified reviews (rating ≥4.0)
2. Recent reviews (last 6 months preferred)
3. Xiaohongshu accommodation posts
4. Mafengwo accommodation guides — label ⚠️

### Weather & Events
1. China Meteorological Administration (weather.cma.cn)
2. Local government official announcements
3. News reports about local events
4. User posts about past events — label ⚡ for current year

## Contradiction Resolution

When sources disagree:
1. Prefer official sources over user-generated
2. Prefer recent over old (>12 months old = flag as potentially outdated)
3. Prefer specific over vague ("门票50元" beats "门票不贵")
4. When both sides are credible, present both with a note: "来源A说X，来源B说Y，建议到当地确认"
5. When all sources are low quality, be honest: "该信息目前无法充分验证"

## Red Flag Keywords

Treat these keywords in search results as warning signs:
- "宰客" / "坑人" / "专骗外地人" → scam risk
- "商业化严重" / "全是卖东西的" → over-commercialized
- "不值得" / "名不副实" / "网红炒作" → overrated
- "不干净" / "态度差" / "乱收费" → quality issue
- "找不到" / "已关门" / "搬迁" → may no longer exist
