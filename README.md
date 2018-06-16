To clone the correct branch:
`git clone -b "webassembly" https://github.com/rajeevgUCI/Halide.git`

To build:
Clone and build my forked llvm repository, as described in the README for that repository.
Then, build Halide:
```bash
export LLVM_CONFIG=<path to llvm>/build/bin/llvm-config
export CLANG=<path to llvm>/build/bin/clang
make
```

For original README, see README\_original.md .
