# Readme

## Install

```bash
pip3 install requests
```

## Example

```jsx
import requests
import json

limit = 500
days = 365

url = f"https://eonet.gsfc.nasa.gov/api/v2.1/events?limit={limit}&days={days}"
req = requests.get(url)
events_data = req.json()

with open('data.json', 'w') as f:
    f.write(json.dumps(events_data, indent=4))

event_list = events_data['events']

for event in event_list:
    print(event['title'])
```
