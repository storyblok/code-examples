```
var data = null;

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.storyblok.com/v1/cdn/stories/home?token=xs8KfuZGvQVOM824AFUQDQtt");
xhr.setRequestHeader("cache-control", "no-cache");

xhr.send(data);
```
