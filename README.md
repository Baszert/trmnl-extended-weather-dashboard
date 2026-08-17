# Extended Weather Dashboard

A comprehensive weather dashboard plugin for [TRMNL](https://trmnl.com/) that displays current conditions, 8-day forecast, and detailed meteorological data on your e-ink display.

<a href="https://usetrmnl.com/recipes/214872">
  <img src="https://usetrmnl.com/images/brand/badges/dark/show-it-on-trmnl/trmnl-badge-show-it-on-dark.svg" alt="TRMNL Badge" width="120">
</a>

## Features

### Current Weather
- **Temperature** with "feels like" apparent temperature
- **Weather conditions** with descriptive icons (sunny, cloudy, rainy, snowy, thunderstorm, etc.)
- **Today's high/low** temperatures
- **Cloud cover** percentage
- **Humidity** percentage

### 8-Day Forecast
- Daily weather icons
- High and low temperatures for each day
- Day-of-week labels

### Detailed Meteorological Data
- **Wind Speed** with customizable units (km/h, m/s, mph, knots)
- **Wind Direction** in degrees
- **UV Index** for the current hour
- **Precipitation Probability** (or snowfall when applicable)
- **Visibility** with distance unit preference
- **Air Quality Index** (US AQI or European AQI)
- **Atmospheric Pressure** in hPa
- **Total Daylight** duration
- **Sunrise & Sunset** times
- **PM2.5 and PM10** particulate matter measurements

### Customization Options
- **Location name** display
- **Temperature units**: Celsius or Fahrenheit
- **Wind speed units**: km/h, m/s, mph, or knots
- **Distance units**: kilometers or miles
- **Time format**: 24-hour or 12-hour
- **Air Quality Index type**: US AQI or European AQI

## Installation

1. **Add the plugin to your TRMNL device**
   - Copy all files to your TRMNL plugins directory
   - Or install via the TRMNL plugin marketplace (if available)

2. **Configure your settings**
   - Enter your **Location name** (e.g., "Amsterdam", "New York")
   - Enter your **Latitude** (use [GPS Coordinates](https://www.gps-coordinates.net/) to find yours)
   - Enter your **Longitude**
   - Select your preferred units and formats

3. **Deploy to your device**
   - The plugin will automatically fetch weather data every 60 minutes

## Data Sources

This plugin uses two free, open-source APIs:

- **[Open-Meteo Weather API](https://open-meteo.com/)** - Current weather, forecasts, and meteorological data
- **[Open-Meteo Air Quality API](https://air-quality-api.open-meteo.com/)** - Air quality measurements (AQI, PM2.5, PM10)

No API key required! 🎉

## Layout Support

The plugin includes four layout sizes to fit your TRMNL screen configuration:

- **Full** (800x480px) - Complete dashboard with all data points
- **Half Horizontal** (800x240px) - Condensed horizontal layout
- **Half Vertical** (400x480px) - Vertical layout with key metrics
- **Quadrant** (400x240px) - Compact view with essential information

## Weather Codes & Icons

The plugin supports all WMO weather interpretation codes:

| Code | Condition | Icon |
|------|-----------|------|
| 0 | Clear sky | ☀️ wb_sunny |
| 1-2 | Mainly clear / Partly cloudy | ⛅ wb_cloudy |
| 3 | Overcast | ☁️ cloud |
| 45, 48 | Fog | 🌫️ foggy |
| 51-67 | Drizzle & Rain (various intensities) | 🌧️ rainy |
| 71-86 | Snow (various intensities) | ❄️ ac_unit |
| 95-99 | Thunderstorm | ⛈️ thunderstorm |

## Technical Details

- **Strategy**: Polling (fetches data via GET request)
- **Refresh Interval**: 60 minutes
- **Font**: Google Sans Flex
- **Icons**: Material Symbols Outlined
- **Timezone**: Automatically detected based on coordinates

## Files

- `shared.liquid` - Core data processing and variable assignments
- `full.liquid` - Full-screen layout (800x480px)
- `half_horizontal.liquid` - Half-width horizontal layout (800x240px)
- `half_vertical.liquid` - Half-height vertical layout (400x480px)
- `quadrant.liquid` - Quadrant layout (400x240px)
- `settings.yml` - Plugin configuration and custom fields

## Configuration Example

```yaml
Location: Amsterdam
Latitude: 52.3676
Longitude: 4.9041
Temperature Unit: Celsius (°C)
Wind Speed Unit: km/h
Distance Unit: Kilometers (km)
Time Format: 24-hour (13:45)
Air Quality Index Type: European AQI
Bar Color: WWhite
```

## Credits

Created by **achtnegen** ([trmnl@achtnegen.nl](mailto:trmnl@achtnegen.nl))

Weather data provided by [Open-Meteo.com](https://open-meteo.com/) - Free Open-Source Weather API

## License

This plugin is provided as-is for use with TRMNL devices.

## Support

Questions or feature requests? Email [trmnl@achtnegen.nl](mailto:trmnl@achtnegen.nl)
