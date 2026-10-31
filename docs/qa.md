# Jury Q&A: 2 minutes

Each question has an owner. The owner answers in **2–3 sentences (under 20 seconds)**, then stops. Others add only if the owner looks at them.

| Area | Owner |
|---|---|
| Data, tech, costs of running | Shohjahon |
| Mini App, UX, "would a shop owner use it" | Jahongir |
| Bot, voice, invoice AI | Muhammadali |
| Market, money, numbers, growth | Otabek |
| Risks, data quality, testing | Abdulboriy |

Golden rule: if we don't know, say what we assumed and how we'll check it. The jury scores **realism in metrics**, so "this is an assumption, we verify it in the pilot" is a strong answer.

---

## The five we're sure to get (`product.md` §17)

**1. Where does the data come from? (Shohjahon)**
> Four layers: AI parsing of wholesalers' Telegram channels for the cold start, invoice photos from shops for real deal prices, and suppliers updating their own price lists. On top of that we filter outliers, weight sources and flag prices older than 7 days.

**2. Why would suppliers agree to show their prices? (Shohjahon)**
> We don't need them at the start: their prices are already public in Telegram. Once shops order through us, suppliers want to be listed correctly, because that's where the orders come from.

**3. How will you make money? (Otabek)**
> Search stays free. Suppliers pay 1.5–2% commission on orders, shops pay for Pro alerts and forecasts, and distributors and banks pay for price and demand reports. Commission is the main stream, so we don't depend on subscriptions.

**4. Why is this better than the Telegram price channels? (Jahongir)**
> Channels give you one seller's price, often outdated. We combine all of them, compare them, keep the history and pick the cheapest supplier mix including delivery. And you can just send a voice message.

**5. What if the shop and supplier just make the deal off the platform? (Otabek)**
> Some will. But the group discount, the supplier rating and later deferred payment with a bank only work through the platform, so staying is cheaper than leaving.

## Likely follow-ups

**6. How do you stop fake or low-ball prices? (Abdulboriy)**
> Already working in the prototype: an invoice price only enters the database if it's between half and double the market median, and prices older than 7 days are flagged stale. Next we weight sources: verified suppliers and real invoices count more than Telegram posts.

**7. How accurate is the AI on voice and invoices? (Muhammadali)**
> Voice already works for real: Uzbek, Russian and English, recognized by Gemini or Whisper, and the bot asks "Correct / Fix" before using the list. Reading the invoice photo is still a demo; in the MVP that's OCR. Either way the shop sees the parsed lines and can fix one with a tap.

**8. Where does the 3 million sum average order come from? (Otabek)**
> It's an assumption, and we marked it as one. It's the first thing we check in the pilot with the 50 Chilonzor shops, because over 90% of our revenue depends on it.

**9. Is the data in the demo real? What actually works today? (Shohjahon)**
> The markets are real, the prices are demo seed data, and the slide says so. Live in our API today: min, median and max across suppliers with an 8-week trend, a source tag on every price, a stale flag after 7 days, and the invoice check with an outlier filter. Telegram parsing with an LLM, the supplier dashboard and source weighting come next.

**10. Would a busy shop owner actually use this? (Jahongir)**
> It's inside Telegram, which he already uses, with nothing to install and no sign-up. He can just send a voice message. Prices are large on screen and the main action is one button.

**11. Why start in Chilonzor? (Otabek)**
> One district lets us onboard 50 shops in person and bring in the suppliers they already buy from. Then we expand across Tashkent through Telegram and business associations, and into the regions through field agents.

**12. How will you grow beyond Tashkent? (Otabek)**
> Samarkand, Fergana and other regions from month 10, through field agents. We'll also add new categories like household goods and vegetables, then cross-border suppliers.

**13. Did you test it? Does the flow work end to end? (Abdulboriy)**
> Yes. I tested the bot, the Mini App and the API separately and then ran the full flow [N] times without errors. *(Fill in the real number after the dress rehearsal.)*

**14. What does it cost to run? (Shohjahon)**
> Servers and AI are about 60 million sum in year 1 in our model, and it grows with the number of prices we process. That's an assumption we'll check against real API bills once the prototype runs.

**15. Who are your competitors? (Otabek)**
> Today's alternatives are Telegram channels, calling suppliers, distributors' sales agents and the bazaar itself. None of them compare prices across sellers or keep a price history.
