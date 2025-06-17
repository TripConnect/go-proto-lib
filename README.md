# Introduction
The proto definition for golang language.

# Installation
Install with latest version
```sh
go get github.com/tripconnect/go-proto-lib@latest
```
Install with specific version corresponding with specific github tag
```sh
go get github.com/tripconnect/go-proto-lib@v1.0.0
```

# Usage
Example
```go
import (
    "fmt"
    pb "github.com/tripconnect/go-proto-lib/protos"
)

func main() {
    pbUserInfo := pb.UserInfo{}
    fmt.Println(pbUserInfo)
}
```

# Build
Clone proto definition files
```sh
cd go-proto-lib
git clone git@github.com:TripConnect/proto-storage.git
```
Build golang proto files
```sh
cd go-proto-lib
protoc --go_out=./protos --go_opt=paths=source_relative --go-grpc_out=./protos --go-grpc_opt=paths=source_relative --proto_path=proto-storage/protos ./proto-storage/protos/*.proto
```
Publish to github registry
```sh
git add .
git commit -m "build: something"
git tag v<version> # ex: git tag v1.0.0
git push origin v<version> # ex: git push origin v1.0.0
```
