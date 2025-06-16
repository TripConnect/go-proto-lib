# Introduce
The proto definition for golang language.

# Installation
```sh
go get github.com/tripconnect/go-proto-lib@latest
```

# Build
Clone proto definition files
```sh
cd go-proto-lib
git clone git@github.com:TripConnect/proto-storage.git
```
Build golang proto
```sh
cd go-proto-lib
protoc --go_out=./protos --go_opt=paths=source_relative --go-grpc_out=./protos --go-grpc_opt=paths=source_relative --proto_path=proto-storage/protos ./proto-storage/protos/*.proto
```
