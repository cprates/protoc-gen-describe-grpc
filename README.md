Example of how to write a `protoc` *plugin* based on 
[protoc-gen-go-grpc](https://github.com/grpc/grpc-go/tree/master/cmd/protoc-gen-go-grpc). 

`protoc-gen-describe-grpc` generates one method per each service method describing its input and
return types. Doesn't handle enums nor external types.

## Gen options
(needs `protobuf` and `protoc` installed)
```bash
> protoc --go_out=option/ ./option/option.proto
```

## Gen describer 
(needs `protobuf` and `protoc` installed)
 
```bash
> go install .
> protoc --describe-grpc_out=out/ --go_out=out/ ./server.proto
```
 