gRPC - iOS & Android support with Unity
===================================

# Official

[Official Repository](https://github.com/grpc/grpc)

[Official README](https://github.com/grpc/grpc/blob/master/README.md)

# Pre-requisites

## macOS

On a Mac, you will first need to
install Xcode or
[Command Line Tools for Xcode](https://developer.apple.com/download/more/)
and then run the following command from a terminal:

```sh
 $ [sudo] xcode-select --install
```

To build gRPC from source, you may also need to install the following
packages, which you can get from [Homebrew](https://brew.sh):

```sh
 $ brew install autoconf automake libtool shtool
```

If you plan to build from source and run tests, install the following as well:
```sh
 $ brew install gflags
```

## Protoc

By default gRPC uses [protocol buffers](https://github.com/google/protobuf),
you will need the `protoc` compiler to generate stub server and client code.

If you compile gRPC from source, as described below, the Makefile will
automatically try and compile the `protoc` in third_party if you cloned the
repository recursively and it detects that you don't already have it
installed.

If it hasn't been installed, you can run the following commands to install it.

```sh
 $ git submodule update --init --recursive
 $ make third_party/protobuf/configure
 $ cd third_party/protobuf
 $ ./configure
 $ sudo make install
```

# Install

```sh
 $ git submodule update --init --recursive    # if you didn't run before
 $ make
 $ sudo make install
 $ sudo make grpc_csharp_ext
```
