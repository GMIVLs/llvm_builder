# llvm_builder
[![llvm-project](https://img.shields.io/badge/llvm_project-compiler_and_toolchain_technologies-yellow)](https://github.com/llvm/llvm-project)
![Static Badge](https://img.shields.io/badge/clang-version--18.0.0-blue)
![Static Badge](https://img.shields.io/badge/lldb_mi-version_GNU_gdb_(GDB)_7.4-green)


In this guide, we will outline step-by-step instructions for building both LLVM
and the lldb-mi debug adapter from scratch.

Before proceeding, ensure that your system meets the minimum requirements for
building these projects. LLVM requires a C++-compatible compiler, while
lldb-mi requires a recent version of Python (Python 3 is recommended).

To begin, download the source code for both LLVM and lldb-mi from their
respective websites. Here are the links:

1. LLVM: https://llvm.org/releases/download.html
2. lldb-mi: https://github.com/lldb-mi/adapter


## Building from scratch the LLVM-Project

- Check [here](./docs/B01_building_against_custom_lldb.md

![Building process](./assets/V01.gif)

## Building from scratch the LLDB-MI adapter

- Check [here](./docs/B02_buidling-against_lldb-mi.md)

## References:

- [lldbvscode renamed to lldbdap](https://www.reddit.com/r/LLVM/comments/17s5ywl/lldbvscode_renamed_to_lldbdap_in_llvmproject/)
