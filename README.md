Zainstalowałem Git Bash na Windowsie


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


$ curl --fail \
    -X DELETE \
    -H "Content-Type: application/json" https://httpbin.org/delete
 
reakcja:
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   362  100   362    0     0    105      0  0:00:03  0:00:03 --:--:--   105{
  "args": {},
  "data": "",
  "files": {},
  "form": {},
  "headers": {
    "Accept": "*/*",
    "Content-Type": "application/json",
    "Host": "httpbin.org",
    "User-Agent": "curl/7.88.1",
    "X-Amzn-Trace-Id": "Root=1-64665061-3b7d02436fd715c81e0469f8"
  },
  "json": null,
  "origin": "83.30.133.158",
  "url": "https://httpbin.org/delete"
}


Metoda PUT zwraca pełną zawartość tego, do czego została wywołana, zaś metoda PATCH zwraca zmodyfikowaną zawartość.

CRUD opiera się na metodach POST, GET, PUT lub PATCH oraz DELETE

Circuit Breakers działa w ten sposób, że jeśli jakaś funkcjonalność nie działa, to pozostali klienci próbujący jej zażądać od razu dostają informację, że nie działa.

Programiści próbują unikać Cascading Failures, ponieważ drobne błędy powodujące inne błędy mogą zablokować całą stronę.


