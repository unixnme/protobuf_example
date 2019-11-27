## Install
```shell script
git submodule update --init 
cd protobuf
./configure
make -j4
make install
cd ..
```

## Compile
```shell script
protoc --cpp_out=. addressbook.proto
```

## Build
```shell script
mkdir build && cd build
cmake ..
make 
cd ..
```

## Run
```shell script
build/write address.bin
build/read address.bin
```