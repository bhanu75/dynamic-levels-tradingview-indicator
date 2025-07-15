 📊 Dynamic Levels TradingView Indicator

A customizable Pine Script indicator that dynamically draws horizontal support/resistance levels around three base price points, with individual spacing for each. Designed for price action traders, breakout analysts, and zone-based strategy enthusiasts.

> Created by [Bhanu Tripathi](https://github.com/bhanu75)

---

 🧠 Features

- 🟩 3 customizable base levels
- 📏 User-defined spacing to expand levels up/down
- 🔁 Automatic multi-line plotting around each level
- 🔎 Candle color highlighting for price cross confirmations
- 🧩 Works across any timeframe and asset
- 💬 Simple UI inputs, highly adjustable

---

 📷 Visual Preview

[Chart Screenshot](Dynamic Levels TradingView Indicator.jpeg)

Above: Levels adapting around 3 major base price points with color-coded candle crosses.

---

 ⚙️ How It Works

Each base level (Base 1, Base 2, Base 3) generates 5 key levels:
- Base itself
- 2 levels above (spacing multiples)
- 2 levels below (spacing multiples)

When the candle closes above and crosses the level, it’s marked green.  
When the candle closes below and crosses the level, it’s marked red.

This makes levels highly interactive, not just static lines.

---

 🛠 Inputs

| Input              | Description                          |
|-------------------|--------------------------------------|
| Base Level 1       | Price around which levels are drawn |
| Spacing 1          | Gap size above/below Base 1         |
| Base Level 2       | Second base input                   |
| Spacing 2          | Custom spacing for Base 2           |
| Base Level 3       | Third major level                   |
| Spacing 3          | Custom spacing for Base 3           |

---

 📥 Installation

1. Open [TradingView](https://www.tradingview.com/)
2. Go to Pine Editor
3. Paste the code from `dynamic-levels.pine`
4. Click Add to Chart
5. Adjust the base levels and spacings via inputs

---

 🔔 Optional Enhancements (Future Ideas)

- Add alert conditions on crossovers
- Enable color toggles for each level group
- Export level data to table or external webhook

---

 💻 Code Sample (Extract)

```pinescript
plot(level1_1, title="Base Level 1", color=color.white, linewidth=2, style=plot.style_stepline, trackprice=true)
barcolor(crossUp ? color.green : crossDown ? color.red : na, title="Candle Highlight")

The full code is in dynamic-levels.pine
