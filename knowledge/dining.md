# Dining Search Framework (食)

## Search Query Templates

Execute these WebSearch queries for the destination. Replace `{dest}` with actual value.

### Local Cuisine Discovery
| Query | Purpose |
|-------|---------|
| `"{dest} 特色美食 必吃"` | Signature dishes |
| `"{dest} 本地人 推荐 餐厅"` | Local-favored restaurants |
| `"{dest} 小吃 一条街 夜市"` | Street food concentration |
| `"{dest} 早餐 吃什么"` | Breakfast specialties |

### Restaurant Verification
| Query | Purpose |
|-------|---------|
| `"{restaurant_name} 大众点评 评分"` | Dianping rating check |
| `"{restaurant_name} 怎么样 好吃吗"` | General sentiment |
| `"{dest} 餐厅 避雷 踩坑"` | Negative experiences warning |
| `"{restaurant_name} 小红书 探店"` | Xiaohongshu reviews |

### Verification Rules
1. **Rating threshold:** Dianping ≥3.5 (weighted more heavily for Chinese destinations)
2. **Volume check:** Xiaohongshu ≥3 independent posts mentioning the same restaurant positively
3. **Recency:** Preference for reviews within the last 12 months
4. **Local vs tourist split:** Explicitly search for "本地人去的" vs "游客去的" and flag the difference
5. **Red flags:** "宰客", "贵得离谱", "不好吃还贵", "专坑外地人" — any of these → ⚡ or ❓

### Output Format
For each recommended dish/restaurant:
- **Name** | Type (local staple/tourist spot) | Price range/person | Rating (if available) | Confidence
- Sort by: local staples first, tourist spots with caveats last

### Key Rules
1. Always distinguish "local eats" from "tourist restaurants"
2. Always mention peak hours if known
3. For Chinese destinations: prioritize Dianping reviews > Xiaohongshu > Douyin
4. If a place is famous but overrated, say so explicitly with source citations
