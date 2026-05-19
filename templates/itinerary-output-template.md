# {{DESTINATION}} 旅行计划

*生成日期：{{DATE}} | 信息置信度：见各条目标注*

---

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| 目的地 | {{DESTINATION}} |
| 日期 | {{DATES}} ({{NIGHTS}}晚{{DAYS}}天) |
| 人员 | {{TRAVELERS}} |
| 预算 | {{BUDGET}} |
| 偏好 | {{PREFERENCES}} |
| 天气 | {{WEATHER_FORECAST}} |

---

## 🗺️ 路线逻辑

```
Day 1: {{ORIGIN}} → {{EN_ROUTE_STOP}} → {{DESTINATION}} → {{ACCOMMODATION_AREA}}
Day 2: {{ACCOMMODATION}} → {{LOCAL_CLUSTER}} → {{RETURN_ROUTE_STOP}} → {{ORIGIN}}
```

---

## 🗺 每日行程

### Day 1: {{DAY1_THEME}} ({{DAY1_DATE}})

| 时间 | 项目 | 详情 | 交通 | 费用 | 置信度 |
|------|------|------|------|------|--------|
| 上午 | {{ACTIVITY}} | {{DETAIL}} | {{TRANSIT}} | {{COST}} | {{✅⚠️⚡}} |
| 中午 | {{ACTIVITY}} | {{DETAIL}} | {{TRANSIT}} | {{COST}} | {{✅⚠️⚡}} |
| 下午 | {{ACTIVITY}} | {{DETAIL}} | {{TRANSIT}} | {{COST}} | {{✅⚠️⚡}} |
| 晚上 | {{ACTIVITY}} | {{DETAIL}} | {{TRANSIT}} | {{COST}} | {{✅⚠️⚡}} |

**本日小计：** ¥{{DAY_TOTAL}}
**住宿：** {{HOTEL_NAME}} | ¥{{PRICE}}/晚 | {{CONFIDENCE}}

### Day 2: {{DAY2_THEME}} ({{DAY2_DATE}})
... (repeat for each day)

---

## 💰 预算明细

| 类别 | 预估费用 | 备注 |
|------|---------|------|
| 往返交通 | ¥{{}} | {{}} |
| 住宿 ({{N}}晚) | ¥{{}} | {{}} |
| 餐饮 | ¥{{}} | {{}}/天 × {{}}天 × {{}}人 |
| 门票/体验 | ¥{{}} | |
| 内部交通 | ¥{{}} | |
| 其他 | ¥{{}} | 预留 |
| **总计** | **¥{{TOTAL}}** | 预算：¥{{BUDGET}} ({{STATUS}}) |

---

## ⚠️ 避坑清单

1. 🚫 **{{SCAM_NAME}}** — {{DESCRIPTION}} (来源: {{SOURCE}})
2. ⚠️ **{{PITFALL}}** — {{DESCRIPTION}} (来源: {{SOURCE}})
3. 💸 **{{TRAP}}** — {{DESCRIPTION}} (来源: {{SOURCE}})

---

## 🔄 备选方案

### 如果下雨
- {{RAIN_ALTERNATIVE_1}}
- {{RAIN_ALTERNATIVE_2}}

### 如果某个景点关闭
- {{CLOSURE_ALTERNATIVE}}

### 如果时间不够
- Priority: {{TOP_3_MUST_DOS}}

---

## 📱 实用信息

| 项目 | 内容 |
|------|------|
| 紧急电话 | 报警110 急救120 火警119 |
| 当地旅游投诉 | {{LOCAL_TOURISM_HOTLINE}} |
| 穿搭建议 | {{CLOTHING_ADVICE}} |
| 必备物品 | {{PACKING_LIST}} |
| 当地交通APP | {{LOCAL_TRANSIT_APPS}} |
