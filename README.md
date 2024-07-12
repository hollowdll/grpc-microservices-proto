# grpc-microservices-proto
Proto files for gRPC microservices example project.

This repository contains gRPC API definitions with Protocol Buffers and the generated source code.

The generated source codes are used in the microservices as external dependencies in this example project: https://github.com/hollowdll/go-grpc-microservices

# Tagging versions

The generated source codes can be versioned with Git tags. Golang uses this for dependency management so you can import a specific version of the generated source code as an external dependency in another Go project.

For example
```sh
git tag -a gen/golang/paymentpb/v1.0.0 -m "gen/golang/paymentpb/v1.0.0"
git push --tags
```
This tags the generated source code of payment service as v1.0.0 and pushes it to the remote repository. Now you can import the generated code of payment gRPC API definition v1.0.0 in your microservices.

For example
```sh
go get -u github.com/<YOUR GITHUB USERNAME>/<YOUR REPO>/gen/golang/paymentpb@v1.0.0
```
