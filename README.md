[中文](./README.cn.md)
# Elite Robots CS SDK

The SDK for Elite CS series robots.

## Requirements
 * **RT ROBOT & RT SERVER** (the control software for robots) version >= **2.13.x** (for CS-Series). If the version of the robot's control software is lower than this, it is recommended to upgrade it.
 * The socket in the SDK uses **boost::asio**. Therefore, the **boost** library needs to be installed.
 * This SDK requires a compiler that supports C++17 or C++14. Note that if the C++14 standard is used, **boost::variant** will be used.
 * cmake version >= 3.22.1

## Build
On the Windows platform, you can use the following steps to compile this project:
```bash
cd <clone of this repository>
mkdir build && cd build
cmake..
cmake --build./
```
After compilation, two library files, `libelite_robot_client_static.lib` and `libelite_robot_client.dll`, and an `include` folder containing header files will be obtained.

For the Linux platform, you can use the following steps to compile and install:
```bash
cd <clone of this repository>
mkdir build && cd build
cmake..
make -j
sudo make install
```

## User guide
[English guide](./doc/UserGuide/en/UserGuide.en.md)

## Document
To compile the documentation, you need to install dependencies first:
```bash
sudo apt-get update
sudo apt-get install doxygen
sudo apt-get install doxygen-gui
```

You can compile the documentation using the following steps:
```bash
cd <clone of this repository>
mkdir build && cd build
cmake -DELITE_COMPLIE_DOC=TRUE..
make -j
```
After compilation, in the `./build` directory, you can see the `./docs` directory, which contains the usage documentation.

## Example
In the folder `./example/`, there are examples of how to use this SDK. If you need to compile the examples, please refer to the following steps:
```bash
cd <clone of this repository>
mkdir build && cd build
cmake -DELITE_COMPLIE_EXAMPLES=TRUE..
make -j
sudo make install
```

## Compatible Operating Systems
Tested on the following system platforms:

 * Ubuntu 22.04 (Jammy Jellyfish)
 * Ubuntu 16.04 (Xenial Xerus)
 * Windows 11

## Compiler
Currently compiled with the following compilers:

 * gcc 11.4.0
 * gcc 5.5.0
 * msvc 19.40.33808