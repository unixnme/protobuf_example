## Install
```shell script
git submodule update --init --recursive
cd protobuf
./autogen.sh
./configure
make -j4
cd ..
```

## Compile
```shell script
protobuf/src/protoc --cpp_out=. addressbook.proto
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