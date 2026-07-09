# Chicago Lakefront Sailing Weather

Live wind, waves, water temp, and a race-day outfit recommendation for sailing on Lake Michigan off Chicago. No login, no install — just open the page.

**Live site:** https://lakefrontlogic-commits.github.io/chicago-lakefront-sailing-weather/

## What it does

- Pick a harbor and any date (or click a race card) to see wind, gusts, wave height/period, water temp, sunrise/sunset, and active NWS marine advisories.
- Get a specific "what to wear" recommendation tiered by on-water feels-like temperature, with call-outs for cold-water immersion risk, gusty/small-craft-advisory wind, and rain.
- Dates within ~16 days use live forecast data; older or far-future dates fall back to historical or seasonal-average data (clearly labeled).

## Updating the race list

The races shown on the page live in the `RACES` array near the top of the `<script>` block in `index.html`. Each entry looks like:

```js
{ name: 'NHYC Wednesday Series', date: '2026-07-15', harbor: 'monroe', notes: 'optional' }
```

`harbor` must match one of the `<option value>`s in the harbor dropdown (`monroe`, `dusable`, `belmont`, `diversey`, `montrose`, `31st`, `jackson`).

## Data sources

[NWS Chicago (LOT)](https://www.weather.gov/lot/) marine alerts, [Open-Meteo](https://open-meteo.com/) forecast/marine/historical archive, [NDBC buoy 45198](https://www.ndbc.noaa.gov/station_page.php?station=45198). This is a planning aid, not a safety authority — always check the official NWS marine forecast before heading out.
