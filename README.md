# kindle-weather-dashboard

Simple webpage with weahter informations.
* for **Kindle 4/5 only** (for now) *Paperwhite support (or universal) in progress*
* only **portrait mode** (for now)
* api source: openweathermap.org
* configurable place, units, language

## Configuration
### with config.js
* create config.js file from config.js.sample and set variables
 * `api_locParams` - query parameters to set location (e.g. `lat=50&lon=14`, or `q=Paris`)
 * `api_appId` - set your `API KEY (appId)` from http://openweathermap.org/appid
 * `api_lang` - output language (e.g. `en`)
 * `api_units` - units (e.g. `metric`, `imperial`)
 * or you can set all parameters with `api_params` varialble (e.g. `q=Prague&appid=YOUR_API_KEY&lang=sk&units=metric`
 
See more: http://openweathermap.org/current and http://openweathermap.org/forecast5

### with url query parameters
* `appId` sets the appId
* `city` sets city, (e.g. `city=Paris`)
* `lat`, `lon` sets location (e.g. `lat=50&lon=14`)
* `lang` and `units` for lang and units :)

Examples:
* Dashboard for Prague, metrics slovak language: `http://YOUR_URL/?city=Prague&lang=sk&units=metric&appId=YOUR_API_KEY`
* Dashboard for given gps, metric, default language: `https://YOUR_URL/?lat=50&lon=14&units=metric&appId=YOUR_API_KEY`

## Screenshots

![alt sc1.png](https://raw.githubusercontent.com/matopeto/kindle-weather-dashboard/master/screen_shot_kindle4.gif)
