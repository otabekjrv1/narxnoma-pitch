# Pitch script: 3:00

Problem → live demo → numbers, as the case brief asks. **Slides 1–9 on stage.** Slide 10 is for the jury only.

Each line matches its slide. About 280 spoken words, roughly 2 minutes at a calm pace. The rest of the 3:00 is for taps, clicks and pauses.

| Time | Who | Slide | What |
|---|---|---|---|
| 0:00–0:20 | Abdulboriy | 1 → 2 | Problem |
| 0:20–0:30 | Otabek | 3 | Solution: bot + Mini App |
| 0:30–1:50 | Muhammadali + Jahongir (Shohjahon taps) | 4 + phone | Live killer flow |
| 1:50–2:20 | Shohjahon | 5 → 6 | Where prices come from, money |
| 2:20–3:00 | Otabek | 7 → 8 → 9 | Market, numbers, close |

- **Clicker:** Otabek.
- **Phone:** Shohjahon, mirrored to the screen.
- **Bot:** runs on Muhammadali's laptop (long polling). That laptop must be on and online during the pitch.

---

**Abdulboriy, 0:20** · *slide 1, click to 2 on "Dilshod"*
> This is Dilshod. He runs a grocery shop in Chilonzor.
> Two days a week he goes round the bazaars and calls suppliers.
> The same bag of sugar costs a different price every week,
> and he has no idea if today's price is fair.

**Otabek, 0:10** · *slide 3*
> Narxnoma fixes that, inside Telegram: a bot and a Mini App. Send your list, get the fair price and the cheapest suppliers. Let us show you.

**Muhammadali, 0:15** · *slide 4, screen switches to the phone*
> Dilshod just says his list to our bot: sugar, ten bags. Oil, twenty. Flour, five.
> The bot turns his voice into a clean list.

**Jahongir, 0:45** · *Shohjahon taps through the Mini App as Jahongir speaks*
> Every item shows the fair market price and its trend.
> Sugar: seven suppliers side by side. It's been rising for three weeks, so buy now.
> The best mix: sugar and flour from Abu Saxiy, oil from Qo'yliq, delivery included.
> Four hundred thirty-six thousand sum saved.
> And three shops nearby are buying sugar too. Dilshod joins: four percent off, one delivery tomorrow.

**Muhammadali, 0:20**
> Tomorrow the delivery comes. Dilshod snaps the invoice,
> and sees right away that he overpaid five and a half percent. That real price goes into our index, so the data gets better for everyone.

**Shohjahon, 0:30** · *slide 5, click to 6*
> Where do the prices come from? Wholesalers' Telegram channels, read by AI. Invoice photos like the one you just saw. And suppliers themselves, because orders come through us. Outliers and old prices are filtered out.
> *[click]* Search is free. Suppliers pay a small commission on each order, shops pay for alerts, and banks and distributors buy reports.

**Otabek, 0:40** · *slide 7, click to 8, click to 9*
> Uzbekistan has over eighty-six thousand retail businesses, and Tashkent retail grew thirteen percent last year.
> *[click]* We start with fifty shops in Chilonzor and grow to eight thousand. On these assumptions we're profitable in year two.
> *[click]* Our goal: every shop owner knows today's fair price before leaving home. Thank you.

---

## Plan B

| If… | Then… |
|---|---|
| The phone or demo freezes for 10 seconds | Otabek goes back to slide 4: it has a screen for every step. Keep talking over it |
| Wi-Fi fails or voice isn't recognized | Muhammadali sends `/demo` in the bot: it inserts the ready transcript |
| The bot doesn't answer (laptop asleep or offline) | Shohjahon types the list straight into the Mini App |

## Rules

- Say only numbers that are on the slide or the phone. The invoice shows +5.5% (595,000 sum) in both the bot and the site since #29.
- If you're over time, cut words, never flow steps: all 6 steps must be shown (task 11 is worth 15 points).
- Hand over by looking at the next speaker, not by saying "now X will…".

## Before going on stage

- [ ] Shohjahon redeploys the API and resets the demo data, so the phone shows 436,000 saved and 10,439,000 total
- [ ] The site and API have #26, #29 and #30 deployed: invoice shows +5.5%, 595,000
- [ ] Muhammadali's laptop is on, online, with the bot running; the voice key is set
- [ ] Phone mirroring tested on the venue screen
- [ ] Deck open at slide 1, fullscreen (F)
- [ ] Run 1 ___ · Run 2 ___ · Run 3 ___ (target 2:45–3:00)
