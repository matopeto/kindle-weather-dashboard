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

Example: https://matopeto.github.io/kindle-weather-dashboard/?city=Paris&appId=YOUR_APP_ID

## Samples
I created `API KEY` for github (it is free, but it has FUP for requests, so in real use case replace appId with your key.)

#### Dashboard for Prague, metrics, slovak language:
https://matopeto.github.io/kindle-weather-dashboard/?city=Prague&lang=sk&units=metrics&appId=f4c7cce581eb51ad03865fb9fb368167

#### Dashboard for given gps, metrics, default language:
https://matopeto.github.io/kindle-weather-dashboard/?lat=50&lon=14&units=metrics&appId=f4c7cce581eb51ad03865fb9fb368167


## Screenshots

![alt sc1.png](https://raw.githubusercontent.com/matopeto/kindle-weather-dashboard/master/screen_shot_kindle4.gif)
