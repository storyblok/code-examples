```
import http.client

conn = http.client.HTTPSConnection("api.storyblok.com")

headers = {
    'cache-control': "no-cache"
    }

conn.request("GET", "/v1/cdn/stories/home?token=xs8KfuZGvQVOM824AFUQDQtt", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```
