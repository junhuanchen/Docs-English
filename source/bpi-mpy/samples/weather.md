## How to climb the city weather

### I. Prerequisites

- 1. First make sure the current firmware dependency package is complete
```python
Help("modules")
```

- The effect is as shown below. If there are no two dependent packages on the map, please burn the latest firmware.

- ![Evaluate](weather/check.png)

- 2. Make sure you are connected to the network
See: https://github.com/BPI-STEAM/BPI-BIT-MicroPython/wiki/how_to_wifi



### Second, prepare weather api

- 1. Here I used the API of the National Weather Service.
`http://www.weather.com.cn/data/cityinfo/101200801.html # 101200801 for Jingzhou City`
See the city ID for details: http://mobile.weather.com.cn/js/citylist.xml
- 2. Request to return Json data sample column
```python
{
  "weatherinfo":
  {
     "city": "Jingzhou",
     "cityid": "101200801",
     "img1": "n7.gif",
     "img2": "d2.gif",
     "ptime": "18:00",
     "temp1": "16°C",
     "temp2": "23°C",
     "weather": "Little rain turns negative"
  }
}
```


- We can analyze these json files and write the following example
### III. Example Analysis
```python

Import urequests
From microbit import *

Def get_weather():
Url = "http://www.weather.com.cn/data/cityinfo/101200801.html"
Rsp = urequests.get(url)
Data = eval(rsp.text) # eval function is used to convert string type json data -> to python dictionary type
Weather = data["weatherinfo"]
L = weather["temp1"] #lowest temperature
H = weather["temp2"] #最高温
Return "L:" + L[:-1] + " H:" + H[:-1] # Data Sample -> L:16 H:23

Display.scroll(get_weather())

# L[:-1] H[:-1] Remove the two special symbols °C and °F, otherwise coding errors will occur
```