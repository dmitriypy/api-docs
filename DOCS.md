# API Reference
###### Base URL

```
https://site.com
```

## /api/{symbol}
#### Args
| Field                        | Type    |
| ---------------------------- | ------- |
| from                         | integer |
| to                           | integer |

#### Python GET Request Example(without args)
```py
import requests

r = requests.get("https://site.com/api/scale")
print(r.json())
>>> {"len_of_all_rows":92438,"ok":true}
```

#### Python GET Request Example(with args)
```py
import requests


base_url = "https://site.com"

r = requests.get(f"{base_url}/api/scale?from=0&to=10")
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

## /api/getInfoByContract
#### Args
| Field                        | Type    |
| ---------------------------- | ------- |
| contract(required)           | string  |

#### Python GET Request Example
```py
import requests

contract_address = "0:dc9b4e9196b7ae32eae6fb28a4f566cbea423ad7b07becead2445fd98e809816"

r = requests.get(f"https://site.com/api/getInfoByContract?contract={contract_address}")
print(r.json())
>>> {'ok': True,
     'jetton': 0.06827374,
     'ton': 14.355361555,
     'left_token_root': 179870.547978104,
     'right_token_root': 2608202.991178625}
```


## /api/tokens.json
#### Python GET Request Example
```py
import requests

r = requests.get("https://site.com/api/tokens.json")
print(r.json())
>>> {'ambr': 'EQAv6X80FaAqBSuZDAPs5uia98M14Pw5LW2MwGkj8I9TFrDb',
     'bolt': 'EQABHkxndSnqrBgMIDR73LB0FBDDM0C_Up39EL1Rn3ao_54-',
     'click': 'EQBm9WZCRQFPXMNQ3u8B4N8Qu2PjMtmCePUqWi4CyIaxz5Ra',
     'ddao': 'EQBWYs6w5lpJ15_PMh3bcTupMrGZHKXQe6ZhCOoOXzAHTglh',
     'dhd': 'EQAuoxgiHoLGBxLQ0lkOgpLwneX_CjroB8H8s3h1QMNLWhIW',
     'exc': 'EQD-rHe9UGVhcTF6SIEM72trdffF_pP_okSw3MCfd6Dd9wBq',
     'gaika': 'EQComXbgJOqDpaA7L7IAefID6HA8FG6Qhh-hStGH-ZipYEf_',
     'ggt': 'EQBTQ9OLKaY2L9jsSqyyGZoZuCv6Q0_3dr7PDEBgeWZcNFIA',
     'grbs': 'EQCqH726RKRhR4HG8TtUR8_ebxo0zB3D-pLdYEPHqwnvQy__',
     'hedge': 'EQBqIBQDyv352Rb7pyJGBLVb4xFIyeJssy2ll-LbwZnTTQxz',
     'inc': 'EQCe7i11lU-VDartvgu5QEu5cNHxd9Ev0PZ1OXKn5gvmHdff',
     'ivs': 'EQDLGQMiDYhkNYGcvuG9Vu1haK8twV1s8jsvoUJTzRG9hcYw',
     'jbct': 'EQA3tl3ID_1C69ECyHTDYJEDUWvQwuj4WdOs5lbFGWqtFUHn',
     'kingy': 'EQDsIxN6kTHNTzkW-KDAFoOd7uK8IV_qhw8wR5NkYH1Gh_SQ',
     'kiss': 'EQC1bSn8Xm5m2JNQVADGDkDa9ox8Jv6vMc0jEvapuuScnMsG',
     'lave': 'EQCCPQrYpU85L23q9RaEfzkXn4buefvm9KA2MhpjA8mVgcDX',
     'marga': 'EQCHQo7Y6CP1IF4Q3fWf2k2blMLJodBO8YjeAFybgzTxyvlJ',
     'redx': 'EQBNtHHaL3D4PKSSc1HyTm5aIL8KUbRvIlXc2AGu1vNMC1EF',
     'scale': 'EQDcm06RlreuMurm-yik9WbL6kI617B77OrSRF_ZjoCYFuny',
     'sneg': 'EQDf3AOJ6tTFCF6TMq11uHF2T6Q7MAFCdR-Oh2ymZlc-1-yS',
     'tnr': 'EQCR_4x99hcPWXDsJHGm52IMgTOQd7Mrta1GlEruJZuOjb5u',
     'tnx': 'EQAycFS0Mr1ZsydnS6OmswoJZCDSxIciAHZFVKOrDll3FBpL'}
```
