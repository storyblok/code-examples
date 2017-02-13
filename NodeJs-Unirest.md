```
var unirest = require("unirest");

var req = unirest("GET", "https://api.storyblok.com/v1/cdn/stories/home");

req.query({
  "token": "xs8KfuZGvQVOM824AFUQDQtt"
});

req.headers({
  "cache-control": "no-cache"
});


req.end(function (res) {
  if (res.error) throw new Error(res.error);

  console.log(res.body);
});
```
