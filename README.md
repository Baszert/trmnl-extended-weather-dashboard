# Extended Weather Dashboard

Too much weather data in one stylish dashboard: current conditions, today's details, air quality and an 8-day forecast.

<a href="https://trmnl.com/recipes/214872"><img width="150" alt="Works with TRMNL" src="https://trmnl.com/images/brand/badges/light/works-with-trmnl/trmnl-badge-works-with-light.svg" /></a>

## Features
- Temperature, feels-like, humidity, rain chance/amount (or snowfall)
- Wind speed, gusts and direction, UV, pressure, cloud cover
- Air quality (US or EU AQI) with PM2.5 and PM10
- Sunrise, sunset, sunshine hours and a sun/moon arc
- 8-day forecast

## Settings
Location name, latitude/longitude, temperature unit, wind speed unit, distance unit, time format, AQI type and panel color (white/black).

Data from [Open-Meteo](https://open-meteo.com/) (weather + air quality). No API key needed.

### Develop locally

Templates and settings live in [`src/`](src/), ready for [trmnlp](https://github.com/usetrmnl/trmnlp):

```sh
gem install trmnl_preview
trmnlp serve
```

Questions or ideas? trmnl@achtnegen.nl or @Bastronautica on Discord.
