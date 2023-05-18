$ curl --fail -X POST \
 -H "Content-Type: application/json" \
 -d '{"name":"natalia"}' https://httpbin.org/post

reakcja:

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    18    0     0    0    18      0      0 --:--:--  0:00:30 --:--:--     0



$ curl --fail -X POST \
  -H "Content-Type: application/json" \
  -d '{"name":"natalia"}' https://httpbin.org/get

reakcja:

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  9   196    0     0  100    18      0      5  0:00:03  0:00:03 --:--:--     8
curl: (22) The requested URL returned error: 405



$ curl --fail -X GET \
    -H "Content-Type: application/json" \
    https://httpbin.org/get

reakcja:

% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   296  100   296    0     0    211      0  0:00:01  0:00:01 --:--:--   213{
  "args": {},
  "headers": {
    "Accept": "*/*",
    "Content-Type": "application/json",
    "Host": "httpbin.org",
    "User-Agent": "curl/7.88.1",
    "X-Amzn-Trace-Id": "Root=1-64664fc1-5874cef271f471246718405a"
  },
  "origin": "83.30.133.158",
  "url": "https://httpbin.org/get"
}







