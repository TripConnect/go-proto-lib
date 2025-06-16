# Introduce
The proto definition for golang language.

# Build
Clone proto definition files
```sh
cd go-proto-lib
git clone git@github.com:TripConnect/proto-storage.git
```
Build golang proto
```sh
protoc --go_out=proto-storage/protos/defs --go_opt=paths=source_relative --go-grpc_out=proto-storage/protos/defs --go-grpc_opt=paths=source_relative --proto_path=proto-storage/protos ./proto-storage/protos/*.proto
```
