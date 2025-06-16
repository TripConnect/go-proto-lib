# Introduction
The proto definition for golang language.

# Installation
```sh
go get github.com/tripconnect/go-proto-lib@latest
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
