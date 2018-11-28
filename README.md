To clone the correct branch:
```
git clone -b "webassembly" https://github.com/rajeevgUCI/Halide.git
```

To build:

Clone and build LLVM 7.0.0 with clang and lld as follows:
```
cd <parent-dir-of-llvm>
git clone -b "release_70" https://github.com/llvm-mirror/llvm.git llvm
git clone -b "release_70" https://github.com/llvm-mirror/clang.git llvm/tools/clang
git clone -b "release_70" https://github.com/llvm-mirror/lld llvm/tools/lld
cd llvm
mkdir build
cd build
cmake -DLLVM_ENABLE_TERMINFO=OFF -DLLVM_TARGETS_TO_BUILD=X86 -DLLVM_EXPERIMENTAL_TARGETS_TO_BUILD=WebAssembly -DLLVM_ENABLE_ASSERTIONS=ON -DCMAKE_BUILD_TYPE=Release ..
make
```

Then, build Halide:
```bash
export LLVM_CONFIG=<path to llvm>/build/bin/llvm-config
export CLANG=<path to llvm>/build/bin/clang
make
```

For original README, see README\_original.md .
