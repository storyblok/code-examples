```
var http = require("https");

var options = {
  "method": "GET",
  "hostname": "api.storyblok.com",
  "port": null,
  "path": "/v1/cdn/stories/home?token=xs8KfuZGvQVOM824AFUQDQtt",
  "headers": {
    "cache-control": "no-cache"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```
