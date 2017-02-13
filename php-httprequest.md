```
<?php

$request = new HttpRequest();
$request->setUrl('https://api.storyblok.com/v1/cdn/stories/home');
$request->setMethod(HTTP_METH_GET);

$request->setQueryData(array(
  'token' => 'xs8KfuZGvQVOM824AFUQDQtt'
));

$request->setHeaders(array(
  'cache-control' => 'no-cache'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```
