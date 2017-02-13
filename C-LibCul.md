```
CURL *hnd = curl_easy_init();

curl_easy_setopt(hnd, CURLOPT_CUSTOMREQUEST, "GET");
curl_easy_setopt(hnd, CURLOPT_URL, "https://api.storyblok.com/v1/cdn/stories/home?token=xs8KfuZGvQVOM824AFUQDQtt");

struct curl_slist *headers = NULL;
headers = curl_slist_append(headers, "cache-control: no-cache");
curl_easy_setopt(hnd, CURLOPT_HTTPHEADER, headers);

CURLcode ret = curl_easy_perform(hnd);
```
