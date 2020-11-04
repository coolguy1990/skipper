## Running geoip

1. make sure `$GOROOT` and `$GOPATH` are set correctly.
2. clone this repo
3. `make deps`
4. `make install`
5. Use the below command while editing the geoip.go file 
```go run ./cmd/skipper -insecure -geo-ip-db ./geoip.mmdb -routes-file ./routes.eskip```
6. run a server in another terminal `python3 -m http.server`
7. do curl from another terminal `curl -vL -I -H"X-Forwarded-For: 46.114.39.242" localhost:9090/`