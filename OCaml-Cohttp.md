```
open Cohttp_lwt_unix
open Cohttp
open Lwt

let uri = Uri.of_string "https://api.storyblok.com/v1/cdn/stories/home?token=xs8KfuZGvQVOM824AFUQDQtt" in
let headers = Header.init ()
  |> fun h -> Header.add h "cache-control" "no-cache"
in

Client.call ~headers `GET uri
>>= fun (res, body_stream) ->
  (* Do stuff with the result *)
```
