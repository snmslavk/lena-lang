# The Lena Programming Langugage

## How to install llvm on ubuntu
https://apt.llvm.org/

## Compile the lang
```
cd src

clang++ -g lena.cpp `llvm-config --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o lena
```

## Create the code 
source.lena
```
def foo(x) x + 1;
foo(2);
```

## Run 
```
./lena
```
