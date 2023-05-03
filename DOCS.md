# API Reference
###### Base URL

```
https://site.com/api
```

## Args
| Field                        | Type    |
| ---------------------------- | ------- |
| from                         | integer |
| to                           | integer |

## Python GET Request Example(without args)
```py
import requests

r = requests.get("https://site.com/api/scale")
print(r.json())
>>> {"len_of_all_rows":92438,"ok":true}
```

## Python GET Request Example(with args)
```py
import requests


base_url = "https://site.com/api"

r = requests.get(f"{base_url}/scale?from=0&to=10")
print(r.json())

>>> {'data': {'len_of_all_rows': 92438,
          'lp_contract': '0:dc9b4e9196b7ae32eae6fb28a4f566cbea423ad7b07becead2445fd98e809816',
          'rates': {'0': {'close': '0.051168150',
                          'date': '2023-02-16 15:27:22.752302',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '1': {'close': '0.051168150',
                          'date': '2023-02-16 15:28:19.020826',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '2': {'close': '0.051168150',
                          'date': '2023-02-16 15:29:16.349622',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '3': {'close': '0.051168150',
                          'date': '2023-02-16 15:30:12.567172',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '4': {'close': '0.051168150',
                          'date': '2023-02-16 15:31:08.682641',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '5': {'close': '0.051168150',
                          'date': '2023-02-16 15:33:03.106352',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '6': {'close': '0.051168150',
                          'date': '2023-02-16 15:33:59.231472',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '7': {'close': '0.051168150',
                          'date': '2023-02-16 15:34:55.213754',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '8': {'close': '0.051168150',
                          'date': '2023-02-16 15:35:51.474348',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0},
                    '9': {'close': '0.051168150',
                          'date': '2023-02-16 15:36:47.451102',
                          'high': '0.051168150',
                          'low': '0.051168150',
                          'open': '0.051168150',
                          'volume': 0}}},
 'ok': True}
```
