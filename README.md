# Buf Tour

This repository is used in the Buf Tour described [here](https://dev.docs.buf.build/tour/introduction).

The tour introduces you to the `buf` CLI and the Buf Schema Registry ([BSR](https://dev.docs.buf.build/bsr/overview)).
Along the way, you will enforce lint standards, detect breaking changes, generate code, create a
[module](https://dev.docs.buf.build/bsr/overview#module), manage a non-trivial dependency graph, and publish the module
to the BSR so that it can be consumed by others. The tour takes approximately 20 minutes to complete.

##Commands To Run to Generate gRPC Interface
```shell
cd petapis
```
Run commands:

+ buf config init
+ buf build
  + buf build --exclude-source-info -o -#format=json | jq '.file[] | .package'
+ buf ls-files
  + buf ls-files git://github.com/bufbuild/buf-tour.git#branch=main,subdir=start/petapis
+ buf lint
