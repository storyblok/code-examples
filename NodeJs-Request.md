```
var request = require("request");

var options = { method: 'GET',
  url: 'https://api.storyblok.com/v1/cdn/stories/home',
  qs: { token: 'xs8KfuZGvQVOM824AFUQDQtt' },
  headers: 
   { 'cache-control': 'no-cache' } };

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});
```
