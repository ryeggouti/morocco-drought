# Is Morocco Running Out of Rain?

**Live site:** https://ryeggouti.github.io/morocco-drought/

Not exactly. It's getting hotter.

I analysed 34 rainy seasons (1991/92–2024/25) across a grid of 62 points covering all of Morocco, then tested which changes are statistically real and which could be chance.

## Key findings
1. **The wet years stopped.** The last very wet season (25%+ above average) was 2014/15. The 10 seasons since are the second-longest gap since 1991; the longest was 12 seasons (1996/97–2007/08). Recent seasons aren't record-dry: the five driest were all in 2007/08 or earlier.
2. **The centre lost the most.** Comparing 2015–2025 with 1991–2015, weighted by how much rain each area normally gets: Centre −14.0% (about −33 mm per season), North −4.7% (about −19 mm), South +13.5% (only about +5 mm).
3. **The thirsty air.** Rainfall shows no clear trend, but evaporation demand rose significantly. Since 2015 the average season brought 13 mm less rain, while the air demanded 59 mm more water, so about 80% of the worsening water balance comes from heat.
4. **Rain decides the harvest.** National rainfall vs the next cereal harvest (World Bank yields, 33 seasons): r = 0.61, p = 0.0001. The worst harvests all followed dry seasons.

## What the data can and can't prove
| Trend per decade | Change | p-value | Verdict |
|---|---|---|---|
| Rain | −0.4 mm | 0.960 | Could be chance |
| Evaporation demand | +31.2 mm | 0.001 | Strong, real trend |
| Rain minus evaporation | −31.6 mm | 0.047 | Just significant |

The centre's rainfall drop (p = 0.098) is suggestive but not statistically significant.

## How I built it
- **Data:** daily rain and FAO reference evapotranspiration from Open-Meteo's historical archive, on a 1° grid (about 100 km); Morocco's border from Natural Earth; cereal yields from the World Bank
- **Analysis:** Python (pandas, SciPy, GeoPandas) in Google Colab
- **Website:** HTML, CSS, JavaScript and Chart.js, hosted on GitHub Pages
- I used AI tools to help write some of the code. I chose the questions, checked the results and wrote the findings.

## Data notes
- Open-Meteo data is reanalysis (observations combined with a model), not readings from one weather station per city.
- The grid covers Morocco including its southern provinces. National figures are the average of all 62 points.
- A rainy season runs September to August, so "2022/23" is matched to the 2023 harvest.
- Evaporation demand is what the air could take, not water actually lost; when soil is dry, real evaporation is lower.

## License
Code: MIT. Data: [Open-Meteo](https://open-meteo.com/) (CC BY 4.0), [World Bank](https://data.worldbank.org/) (CC BY 4.0) and [Natural Earth](https://www.naturalearthdata.com/) (public domain).

Part of **[Morocco in Data](https://ryeggouti.github.io/)**. See also:
[How Did Morocco Reach the Semi-Final?](https://ryeggouti.github.io/morocco-world-cup-2022/) · [Stork Flight](https://ryeggouti.github.io/stork-flight/)
