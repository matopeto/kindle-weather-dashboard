# kindle-weather-dashboard

Simple webpage with weahter informations.
* tested on **Kindle 3/4/5 only** and **Paperwhite 3**, *maybe works on other kindles*,
* only **portrait mode** (for now)
* api source: openweathermap.org
* configurable place, units, language

# How to install
1. clone or download repository
2. set your location and others in `config.js`
3. upload to your server, or simply create local (e.g with php: `php -S 192.168.0.1:80 -t .`)
4. disable screensaver on your cindle
 * press search button on homescreen and type: `;debugOn` and press enter on keyboard
 * press search button again and type: `~disableScreensaver` and press enter on keyboard. (On kindle Paperwhite type: `~ds`
5. launch your browser and go to url of your server
6. Dashboard don't need connection to your server (you can shutdown local server now) Dashboard calls api directly.

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

## Try it (on my server):

http://kindle.hrincar.eu/weather/

http://kindle.hrincar.eu/weather/?city=Brno

http://kindle.hrincar.eu/weather/?lat=50&lon=14&lang=en


## Screenshots

### Kindle 4
<img src="screenshot_kindle4.gif" width="300" alt="Kindle 4 screenshot" />

### Kindle Paperwhite 3
<img src="screenshot_paperwhite3.png" width="300" alt="Kindle Paperwhite 3 screenshot" />

### Real devices
<img src="real_devices.jpg" width="300" alt="Dashboard on real devices" />

