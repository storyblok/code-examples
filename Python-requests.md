```
import requests

url = "https://api.storyblok.com/v1/cdn/stories/home"

querystring = {"token":"xs8KfuZGvQVOM824AFUQDQtt"}

headers = {
    'cache-control': "no-cache"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```
