# Transport Search Framework (行)

## Search Query Templates

Execute these WebSearch queries for the destination. Replace `{dest}` and `{origin}` with actual values.

### Long-Distance Transport (大交通)
| Query | Purpose |
|-------|---------|
| `"{origin} 到 {dest} 怎么去"` | All route options |
| `"{origin} 到 {dest} 高铁 时刻 票价"` | High-speed rail specifics |
| `"{origin} 到 {dest} 飞机 航班"` | Flights (if >500km) |
| `"{dest} 交通攻略 到达"` | How others got there |

### Local Transport (内部交通)
| Query | Purpose |
|-------|---------|
| `"{dest} 市内交通 公交 线路"` | Public transit |
| `"{dest} 打车 方便吗"` | Ride-hailing availability |
| `"{dest} 景区之间 怎么去"` | Inter-attraction transit |
| `"{dest} 租车 自驾 停车"` | Self-drive feasibility |

### Route Comparison Rules
1. **Distance-based defaults:** <200km suggest driving/train, 200-800km suggest HSR, >800km consider flights
2. **Cost comparison:** Always provide cost for each option (ticket + transfers to final destination)
3. **Time comparison:** Door-to-door time, not just travel time
4. **Frequency:** Note how many departures per day — rare buses need backup plans

### Output Format
For each viable route, provide:
- **Transport type** | Duration | Cost | Frequency | Notes
- Label with confidence: ✅ (official schedule) / ⚠️ (user-reported) / ⚡ (one source)
