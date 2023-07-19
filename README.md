# The Lena Programming Langugage

The language supports converting to IR, using JIT, and all features of LLVM.

## Create the code 
code_example.lena
```
extern putchard(char);

lenadefines printstar(n)
  lenarepeat i = 1, i < n, 1.0 in
    putchard(42);  

lenadefines fib(x)
  lenaif x < 3 lenathen
    1
  lenaelse
    fib(x-1)+fib(x-2);

printstar(100);
fib(2);
fib(4);
fib(5);
fib(6);
```

## Run 
```
./lena code_example.lena
```
## Try it 
You can take the prebuild binaries from the Release

Or you can compile it by youself

## How to install llvm on ubuntu
https://apt.llvm.org/

The language compiles with the support of llvm 14

## Compile the lang
```
cd src

clang++ -Xlinker --export-dynamic -g lena.cpp `llvm-config --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o lena
```
