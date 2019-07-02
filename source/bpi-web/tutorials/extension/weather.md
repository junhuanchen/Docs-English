#气象资讯

Meteorological information blocks can instantly obtain open data from the Central Meteorological Administration, including common meteorological information such as weather, air quality, weather forecast, earthquake information, reservoir water conditions and radar echo maps. Implementation can better implement the effective application of meteorological information.

## Weather Information Building Block List

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-01.jpg)

## Obtaining meteorological data

Meteorological Information has a "Get Meteorological Information" building block. It can obtain six common types of information: "Air Quality", "Instant Observation", "Weather Forecast", "Earthquake Information", "Reservoir Water" and "Radar Echo". Figure".

> The building block for obtaining meteorological information belongs to the type of "* will continue to execute the rear program* after obtaining the information". When there is this building block in the editing screen, * when the program encounters this building block, it will pause until the weather information is obtained. Will continue to *.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-03.jpg)

## Air quality

The "air quality" building blocks can display information about air quality, including AQI, PM2.5, PM10... and other related values ​​as well as textual descriptions of comprehensive indicators. The location of the detection is the observation station of the Central Meteorological Administration in Taiwan. The location closest to the home is used as the basis for observation.

> Air quality building blocks are required to obtain "air quality" information in conjunction with "Get Meteorological Data" blocks.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-02.jpg)

In the example below, the air quality data of the former town area is obtained, and the air quality comprehensive indicators and individual detection values ​​are spoken through the small monsters.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-04.jpg)

## Instant observation

"Instantaneous observation" building blocks can display relevant information about the current weather, including temperature, humidity, wind power, accumulated rainfall, etc. The detection location is the observation station of the Central Meteorological Administration in Taiwan, and the location closest to the home can be selected. As the basis for observation.

> Instant observation of building blocks is required to obtain "instant observation" information with the "Get Meteorological Data" building blocks.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-05.jpg)

In the example below, the weather information of Kaohsiung and Taipei is reported through the little monsters.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-06.jpg)

## Weather forecast

The "weather forecast" building blocks can display weather forecasts for the next six hours, eighteen hours and thirty-six hours. The forecast locations are the major counties and cities in Taiwan, and the counties and cities where the homes are located can be used as the basis for observation.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-07.jpg)

In the example below, the weather forecast for Kaohsiung's eight hours and the weather forecast for Hsinchu's eighteen hours are reported through the little monsters.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-08.jpg)

## Reservoir water situation

The "Reservoir Water" building blocks can obtain the water conditions of all reservoirs in Taiwan, including the percentage of water storage, effective water storage and rainfall...etc.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-09.jpg)

In the example below, the water information of the Shimen Reservoir and the Zengwen Reservoir are told through the little monsters.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-10.jpg)


## Earthquake Information

The "Earth Information" building blocks can obtain the latest 1-3 earthquake information.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-11.jpg)

In the example below, the last earthquake information is reported by the little monster (example date is 5/17).

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-12.jpg)

## Radar echo

The "radar echo" building block can obtain a radar echo map in the form of jpg.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-13.jpg)

The example below shows a radar echo map through a small monster.

![Weather Information](../images/zh-tw/docs/webbit/extension/weather-14.jpg)