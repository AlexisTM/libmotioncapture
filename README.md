[![CMake](https://github.com/USC-ACTLab/libmotioncapture/actions/workflows/cmake.yml/badge.svg?branch=master)](https://github.com/USC-ACTLab/libmotioncapture/actions/workflows/cmake.yml)

# libmotioncapture
Interface Abstraction for Motion Capture System APIs such as VICON, OptiTrack, PhaseSpace, or Qualisys.

## Compile options
By default, `libmotioncapture` supports the following hardware:

- VICON - SDK git submodule
- Qualisys - SDK git submodule
- OptiTrack - binary parsing over network (no dependency)

Support for following hardware requires additional action by the user:

- VRPN - set up `libvrpn` or `vrpn-client-ros` on the machine.
- Phasespace - manually obtain SDK and copy to `externalDependencies/phasespace_sdk/`.

After setup, enable the appropriate compile flags in `CMakeLists.txt`.

## Prerequisites

```
sudo apt install libpcl-dev ninja-build
```

## Python

```
git submodule init
git submodule update
python3 setup.py develop --user
python3 examples/python.py
```

## C++

```
git submodule init
git submodule update
mkdir build
cd build
cmake ..
```