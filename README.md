# Halide - WebAssembly Fork #

Fork of Halide, with a modification of the webassembly branch.

For original README, see README\_original.md .

## Build Instructions ##

To clone the correct branch:
```
git clone -b "webassembly" https://github.com/rajeevgUCI/Halide.git
```

To build:

Clone [my forked llvm repository](https://github.com/rajeevgUCI/llvm) and build it with WebAssembly support, as described in the README for that repository.

Then, build Halide:
```bash
export LLVM_CONFIG=<path to llvm>/build/bin/llvm-config
export CLANG=<path to llvm>/build/bin/clang
make
```
