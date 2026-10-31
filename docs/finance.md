# 3-year financials (case task 7)

Rule of the case: **every number has an assumption next to it.** All inputs below are our assumptions, not facts. Each is labeled with how we plan to check it. Outputs are computed from the inputs by the formulas shown, so changing one input changes everything downstream.

Currency: UZS. M = million, bn = billion.

## Inputs (assumptions)

| Input | Year 1 | Year 2 | Year 3 | Why / how to verify |
|---|---|---|---|---|
| Active shops (yearly average) | 300 | 2,000 | 8,000 | Y1: 50-shop pilot in Chilonzor, then the rest of Tashkent. Y3 is about 9% of the 86,190 retail enterprises (stat.uz, `market.md`). Plan, not data |
| Share of shops ordering through the platform | 20% | 30% | 40% | Assumption. Check in the pilot: how many of the 50 place an order |
| Orders per ordering shop per month | 4 | 4 | 4 | Shops restock weekly (`product.md` §13). **Needs verification** in shop interviews |
| Average order through the platform | 3,000,000 | 3,000,000 | 3,000,000 | **Needs verification**: biggest unknown, ask 2–3 shop owners for a typical weekly purchase |
| Supplier commission | 1.5% | 2% | 2% | Low end of the 1–3% range in `product.md` §11, raised once suppliers see orders |
| Shops paying for Pro | 5% | 8% | 10% | Assumption, typical freemium conversion. **Needs verification** for this segment |
| Pro price per month | 50,000 | 50,000 | 50,000 | Assumption: must be well below the monthly savings. **Needs verification** in the pilot |
| B2B report clients (distributors, banks) | 0 | 3 | 10 | Assumption: nothing to sell until we have a year of price history |
| B2B report price per client per year | 30,000,000 | 30,000,000 | 30,000,000 | Assumption. **Needs verification** with one distributor or bank |

## Revenue

| Metric | Formula | Year 1 | Year 2 | Year 3 |
|---|---|---|---|---|
| Ordering shops | active × ordering share | 60 | 600 | 3,200 |
| GMV of orders | ordering shops × 4 orders × 3,000,000 × 12 | 8.64 bn | 86.4 bn | 460.8 bn |
| Commission revenue | GMV × commission | 129.6 M | 1,728 M | 9,216 M |
| Paying Pro shops | active × Pro share | 15 | 160 | 800 |
| Pro revenue | paying shops × 50,000 × 12 | 9.0 M | 96 M | 480 M |
| B2B report revenue | clients × 30,000,000 | 0 | 90 M | 300 M |
| **Total revenue** | sum | **138.6 M** | **1,914 M** | **9,996 M** |

Group-order commission and bank revenue share are not counted. They start after year 1 (`product.md` §10) and we don't have the inputs to estimate them.

## Costs (assumptions)

| Cost | Formula / assumption | Year 1 | Year 2 | Year 3 |
|---|---|---|---|---|
| Team | people × 8,000,000/month × 12. 5 → 10 → 20 people. Salary: **needs verification** (hh.uz, average IT salary in Tashkent) | 480 M | 960 M | 1,920 M |
| Servers and AI (LLM parsing, OCR) | Assumption, grows with prices processed. **Needs verification** with real API pricing once the prototype runs | 60 M | 180 M | 480 M |
| Field agents | agents × 5,000,000/month × 12. 0 → 3 (Tashkent) → 10 (regions) | 0 | 180 M | 600 M |
| Marketing / onboarding | new shops × 100,000 per shop. Assumption: in-person demo and one free Pro month | 30 M | 170 M | 600 M |
| **Total costs** | sum | **570 M** | **1,490 M** | **3,600 M** |

## Result

| | Year 1 | Year 2 | Year 3 |
|---|---|---|---|
| Revenue | 138.6 M | 1,914 M | 9,996 M |
| Costs | 570 M | 1,490 M | 3,600 M |
| **Profit / loss** | **−431.4 M** | **+424 M** | **+6,396 M** |

### What this depends on

- Over 90% of revenue in every year is supplier commission, so it depends on three numbers we haven't verified:
  - the average order (3M UZS);
  - the share of shops ordering through us (20–40%);
  - the commission rate.
- Halve the average order and year-2 profit turns into a loss: commission becomes 864 M, total revenue about 1,050 M, against 1,490 M of costs.
- **First thing to verify in the pilot:** the average weekly purchase of a Chilonzor shop and how many shops actually order through the app.

## KPIs by year (targets, not forecasts of fact)

| KPI | Year 1 | Year 2 | Year 3 | Assumption |
|---|---|---|---|---|
| Weekly active shops | 180 | 1,200 | 4,800 | 60% of active shops open the app every week |
| Prices collected per day | 500 | 3,000 | 10,000 | Telegram parsing + invoices + supplier dashboard |
| Paying shops (Pro) | 15 | 160 | 800 | From the revenue table |
| Savings per order (UZS) | measure in pilot | — | — | **Needs verification**: compare the optimizer's price with the shop's last invoice |
| Data accuracy (prices within ±5% of a confirmed invoice) | 80% | 90% | 95% | Target, measured with invoice photos |
