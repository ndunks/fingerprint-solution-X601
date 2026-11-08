
## Change Admin PW

```
curl --url 'http://192.168.18.176/form/Device?act=8' \
  -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/jxl,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7' \
  -H 'Accept-Language: en,id;q=0.9' \
  -H 'Cache-Control: max-age=0' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -b 'SessionID=949372089' \
  -H 'Origin: http://192.168.18.176' \
  -H 'Referer: http://192.168.18.176/csl/changepwd' \
  -H 'Upgrade-Insecure-Requests: 1' \
  -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/157.0.0.0 Safari/537.36' \
  --data-raw 'adminpwd=99&readminpwd=99' \
  --insecure
  ```