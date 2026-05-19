# Accommodation Search Framework (住)

## Search Query Templates

| Query | Purpose |
|-------|---------|
| `"{dest} 住宿 推荐 区域"` | Best areas to stay |
| `"{dest} 住在哪里 方便"` | Convenience comparison |
| `"{dest} 民宿 推荐 价格"` | Guesthouse options |
| `"{dest} 酒店 推荐"` | Hotel options |
| `"{dest} 住宿 避雷 差评"` | Negative experiences |

### Verification Rules
1. **Safety:** Search for "{dest} 住宿 安全 女生" for solo female travelers. Flag areas with safety concerns.
2. **Location:** Map-check proximity to main attractions. "In old town" doesn't always mean convenient.
3. **Rating threshold:** Ctrip/Meituan rating ≥4.0. Read the 10 most recent reviews, not just the rating.
4. **Red flags:** "不干净", "吵", "与照片不符", "安全有问题" — any repeated → exclude.

### Output Format
For each recommended area:
- **Area** | Vibe | Price range/night | Pros | Cons | Confidence
- Include: specific hotel/guesthouse example in each area with source

### Key Rules
1. For Chinese destinations: homestay (民宿) in old town areas is often the best experience, but verify plumbing/heating/quietness
2. For families: prioritize space, safety, kitchen access
3. For budget: note youth hostels, capsule hotels, or rural guesthouses
4. Always note if the best area requires advance booking (peak season)
