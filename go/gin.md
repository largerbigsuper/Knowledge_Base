# gin web framework



## govendor

```shell

go get -u github.com/kardianos/govendor
```


## start project

```
mkdir -p $GOPATH/src/github.com/largerbigsuper/ReservationApp && cd "$_"

govendor init

govendor fetch github.com/gin-gonic/gin@v1.4

curl https://raw.githubusercontent.com/gin-gonic/examples/master/basic/main.go > main.go

go run main.go

```