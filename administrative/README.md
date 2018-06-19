## Administrative divisions

This directory contains files with data regarding administrative divisions of Poland. Only official internal territorial units are presented here, which are (from biggest to smallest):

* Voivodeships (pl: _województwa_)
* Powiats (pl: _powiaty_, something like counties)
* Gminas (pl: _gminy_, municipalities or comunes)

### Voivodeships

_to be done_

### Powiats

Includes following data:

* id – comes from TERYT database and is always four-digits; first two digits match voivodeship code
* name
* population, divided by men vs women and urban vs rural population
* city – a boolean value indication if it's a city with status of powiat
* area - in square kilometers

Example:

```
  {
    "id": "3263",
    "name": "Świnoujście",
    "population": {
      "total": 41027,
      "men": 19751,
      "women": 21276,
      "urban": 41027,
      "rural": 0
    },
    "city": true,
    "area": 197.23
  }
```

### Gminas

Includes following data

* id – comes from TERYT database and is always six-digits; first four digits match powiat code
* name
* population broken down by gender and rural/urban
* type – can be `rural`, `urban` or `urban-rural`
* area – in square kilometers

Example:

```
  {
    "id": "321705",
    "name": "Wałcz",
    "population": {
      "total": 12688,
      "men": 6345,
      "women": 6343,
      "urban": 0,
      "rural": 12688
    },
    "type": "rural",
    "area": 574.91
  }
```

## Sources

* Area: [Powierzchnia i ludność w przekroju terytorialnym w 2016 r.](https://stat.gov.pl/obszary-tematyczne/ludnosc/ludnosc/powierzchnia-i-ludnosc-w-przekroju-terytorialnym-w-2016-r-,7,13.html)
* Population: [Ludność. Stan i struktura w przekroju terytorialnym. Stan w dniu 30.06.2017 r.](http://stat.gov.pl/obszary-tematyczne/ludnosc/ludnosc/ludnosc-stan-i-struktura-w-przekroju-terytorialnym-stan-w-dniu-30-06-2017-r-,6,22.html) (30.06.2017)
