# Attractions Search Framework (游)

## Search Query Templates

| Query | Purpose |
|-------|---------|
| `"{dest} 景点 攻略 必去"` | Core attraction list |
| `"{dest} 值得去吗 真实评价"` | Authenticity check |
| `"{dest} 冷门 小众 景点"` | Off-the-beaten-path options |
| `"{dest} 网红打卡 拍照"` | Instagram-worthy spots |
| `"{dest} [季节/月份] 最佳时间"` | Season-specific advice |
| `"{dest} 门票 价格 开放时间"` | Practical details |

### Commercialization Filter
| Query | Purpose |
|-------|---------|
| `"{dest} 商业化 严重吗"` | Commercialization level |
| `"{dest} 坑 不值得 去"` | Overrated attractions |
| `"{dest} 真正值得去的景点"` | Genuinely worthwhile |

### Verification Rules
1. **Price/hours:** Minimum 2 matching sources. Official site/government tourism page preferred.
2. **"Must-see" claims:** Cross-check with negative reviews ("不值得" "坑").
3. **Photos:** Image search to verify current state (not 10-year-old photos).
4. **Commercialization:** Flag if multiple sources mention "商业化严重" or "全是卖东西的".

### Output Format
For each attraction:
- **Name** | Type (nature/culture/entertainment/shopping) | Time needed | Ticket price | Hours | Confidence
- **Rating:** ⭐ Genuinely worth visiting / ⚠️ Worth it with caveats / ❌ Overrated — explain why
