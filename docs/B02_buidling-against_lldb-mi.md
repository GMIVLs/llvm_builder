# How to build lldb-mi

LLDB's machine interface driver. Adapter for debugging the `C/C++` projects.

- There are two ways to build the `lldb-mi` first using the `llvm` from the
  macOS system (preinstalled with xcode) using

1. Download the `lldb-mi` project using

```sh
git clone git@github.com:lldb-tools/lldb-mi.git
```

```sh
cmake .
cmake --build .
```

2. Using the `llvm` build from the `./B01_building_against_custom_lldb.md`.
   located at `~/buildspace/llvm-inst` (see below)

## Building using the LLVM

1. Create the necessary installation directories

```sh
mkdir build
mkdir install
cd build
```

**NOTE**: First insure with everytime you want to configure this to remove `rm
-rf CMakeCache.txt CMakeFiles`, first. or simply delete `build` and `install`
and create new ones.

2. Here you have two options either

- Using the separate build directory for building lldb-mi. (inside build directory)

```sh
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_PREFIX_PATH=~/buildspace/llvm-inst/ -DCMAKE_INSTALL_PREFIX=~/buildspace/lldb-mi/install/ -GNinja ..
ninja
ninja install
```

- [I used this one]: Building against custom LLDB.framework (Darwin Only),
  using `-DUSE_LLDB_FRAMEWORK=1` (inside build directory) using:

```sh
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_PREFIX_PATH=~/buildspace/llvm-inst/ -DUSE_LLDB_FRAMEWORK=1 -DCMAKE_INSTALL_PREFIX=~/buildspace/lldb-mi/install/ -GNinja ..
ninja
ninja install
```

## References

- [lldb-mi](https://github.com/lldb-tools/lldb-mi?tab=readme-ov-file)
