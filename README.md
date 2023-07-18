# The Lena Programming Langugage

## Compile the lang
```
cd src

clang++ -g lena.cpp `llvm-config --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o lena
```

## Create the code 
source.lena
```
def foo(a b) a*a + 2*a*b + b*b;
def bar(a) foo(a, 4.0) + bar(31337);
extern cos(x);
```

## Run 
```
./lena
```
