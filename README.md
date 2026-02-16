# kindle-weather-dashboard

Simple webpage with weather information.

# Try it!

Go to: http://kindle.hrincar.eu/weather/ and that's it!

or you can install it on your own server, customize it, or run it locally on your Kindle.

_Please, if you use this website, generate your free OWM token (see: https://openweathermap.org/api for more info), because the default token can be blocked and changed at any time and the weather forecast can stop working._

## Features

* **current weather and temperature**
* **forecast: hourly every 3 hours (next 12 hours, landscape mode for 15 hours) or daily for 4/5 days**
* **sunrise and sunset**
* **Moon phase**

## Options

* **portrait and landscape mode**
* **landscape mode on Paperwhite!!** see configuration
* configurable place, units, language
* automatic night mode
* tested on **Kindle 3/4/5, Paperwhite 3, iPad Air**, *it may also work on other Kindles and devices*,

Weather and forecast source: https://openweathermap.org/

Icons source: https://github.com/erikflowers/weather-icons

<img src="real_devices.jpg" width="300" alt="Dashboard on real devices" />

# How to run directly on the Kindle (tested on Kindle PW 3)
1. clone or download repository
2. generate your free API key (AppId) at http://openweathermap.org/appid
3. rename `config.js.sample` to `config.js` and set the parameters you need (all parameters are optional and can be set in the HTML webpage `config.html`, but I recommend setting at least the `appId`)
4. copy the folder with all files to the root of Kindle storage
5. disable the screensaver on your Kindle:
  * press the search button (or keyboard button on Kindle 4) on homescreen and type: `;debugOn` and press enter on the keyboard
  * press the search button (or keyboard button on Kindle 4) again and type: `~disableScreensaver` and press enter on the keyboard. (On Kindle Paperwhite, type: `~ds` - with new firmware this may not be possible, but see these [instructions](https://github.com/matopeto/kindle-weather-dashboard/issues/16) for a solution)
6. launch the browser on your Kindle and go to: `file:///mnt/us/kindle-weather-dashboard/index.html` (where `kindle-weather-dashboard` is the folder in the root of your Kindle storage from step 4)

## Configuration
Parameters can be set in `config.js`, URL query parameters, or through `config.html`.

Parameters:
* `city` - city name (e.g. `Paris`), default: not set
* `lat`, `lon` - GPS coordinates (e.g. `lat=50.1243111`, `lon=14.4901953`), default: not set
* `appId` - OpenWeather API key, default: not set
* `lang` - output language (e.g. `en`), default: `en`
* `units` - `metric` (°C), `imperial` (°F), `standard` (K), default: `metric`
* `rotation` - `ll`, `lr`, `up`, or not set (no forced rotation), default: not set
* `nightMode` - `off`, `auto`, `on`, or `HH-HH` (e.g. `22-06`), default: `off`
* `refreshInterval` - refresh interval in minutes, default: `30`
* `utcOffset` - auto by location (not set), `local`, or custom UTC offset (`+08:00`), default: auto by location
* `tempType` - `actual` or `feelsLike`, default: `actual`
* `forecastType` - `hour` or `daily`, default: `hour`

Precedence:
* URL query parameters override values from `config.js`.
* If neither URL nor `config.js` provides a value, built-in defaults are used.
* For location, when both `city` and `lat`/`lon` are set, `lat`/`lon` take priority.

See more: http://openweathermap.org/current, http://openweathermap.org/forecast and http://openweathermap.org/forecast16

Examples:
* Dashboard for Prague, metric units, Slovak language: `http://YOUR_URL/?city=Prague&lang=sk&units=metric&appId=YOUR_API_KEY`
* Dashboard for a given GPS location, metric units, default language: `https://YOUR_URL/?lat=50&lon=14&units=metric&appId=YOUR_API_KEY`

## Screenshots

### Kindle 4
<img src="screenshot_kindle4.gif" width="300" alt="Kindle 4 screenshot" />

### Kindle Paperwhite 3
<img src="screenshot_paperwhite3.png" width="300" alt="Kindle Paperwhite 3 screenshot" />

### Real devices
<img src="real_devices.jpg" width="300" alt="Dashboard on real devices" />
