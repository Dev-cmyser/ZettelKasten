# type hinting - большая статья

Created at: 2022:06:01 09:19

Tags: #python 
__ 

# тут максимально понятно что вернет функция type hinting - на максимум!
``` python 
from typing import NamedTuple

class Coordinates(NamedTuple):
	longituge: float
	latituge: float
	
def coordinates() -> Coordinates:
	return Coordinates(longituge=some_float, latituge=some_float)



```

__


# если где то есть пречисление то это про enum - тип данных (перечисление)

```python 

from datetime import datetime
from dataclasses import dataclass
from enum import Enum

from coordinates import Coordinate

Celsius = int

class WeatherType(str, Enum):
    THUNDERSTORM = "Гроза"
    DRIZZLE = "Изморось"
    RAIN = "Дождь"
    SNOW = "Снег"
    CLEAR = "Ясно"
    FOG = "Туман"
    CLOUDS = "Облачно"

@dataclass(slots=True, frozen=True)
class Weather:
    temperature: Celsius
    weather_type: WeatherType
    sunrise: datetime
    sunset: datetime
    city: str

def get_weather(coordinates: Coordinate) -> Weather:
    """Requests weather in OpenWeather API and returns it"""
    return Weather(
       temperature=20,
       weather_type=WeatherType.CLEAR,
       sunrise=datetime.fromisoformat("2022-05-04 04:00:00"),
       sunset=datetime.fromisoformat("2022-05-04 20:25:00"),
       city="Moscow"
   )



```

### Links
-[[00-Python]]
-