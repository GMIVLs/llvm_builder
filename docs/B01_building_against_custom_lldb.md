# Building LLDB

## Building LLVM Project

1. Building the lldb at the home directory,

- Create a `buildspace` directory

2. Download LLVM/Clang/LLDB and build them using:

```sh
git clone https://github.com/llvm/llvm-project.git
```

3. Create the necessary directories

```sh
mkdir llvm-inst
mkdir llvm-build
cd llvm-build
```

4. Build using

```sh
cmake -DCMAKE_BUILD_TYPE=Release -DLLVM_ENABLE_PROJECTS="clang;lldb" -DLLVM_ENABLE_RUNTIMES="libcxx;libcxxabi" -DCMAKE_INSTALL_PREFIX=~/buildspace/llvm-inst/ -GNinja ../llvm-project/llvm
ninja  # This takes sometime to build the full llvm-project
ninja install
```

### LLVM BUILD PROCESS

```sh
 cmake (command operate inside the directory)
-------
   |
   |
   v
+---------------+      +---------------+       +---------------------+
| llvm-project  |  ->  | llvm-build    |   ->  | llvm-inst (install) |
+---------------+  -   +---------------+   -   +---------------------+
                   |                       |
                   v                       v
                 ninja                    ninja install

```

- The results by now you should have the full `llvm` project build, located at
  `llvm-inst`, and has the following directories:

```sh
 gmbp 󰇄 GMacBookPro   ~/buildspace/llvm-inst
├─ 󰚩 INSERT 󰇍
╰─ lsd
   rwxr-xr-x   113   gmbp   staff      3 KiB   Fri Nov 10 20:33:49 2023    bin/
   rwxr-xr-x     8   gmbp   staff    256 B     Fri Nov 10 20:33:50 2023    include/
   rwxr-xr-x   253   gmbp   staff      7 KiB   Fri Nov 10 20:33:50 2023    lib/
   rwxr-xr-x     8   gmbp   staff    256 B     Fri Nov 10 20:33:49 2023    libexec/
   rwxr-xr-x     7   gmbp   staff    224 B     Fri Nov 10 20:33:49 2023    share/
```

