# The Lena Programming Langugage

## How to install llvm on ubuntu
https://apt.llvm.org/

## Compile the lang
```
cd src

clang++ -Xlinker --export-dynamic -g lena.cpp `llvm-config --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o lena
```

## Create the code 
source.lena
```
extern putchard(char);
def printstar(n)
  for i = 1, i < n, 1.0 in
    putchard(42);  # ascii 42 = '*'

def fib(x)
  if x < 3 then
    1
  else
    fib(x-1)+fib(x-2);

# print 100 '*' characters
printstar(100);
fib(2);
fib(4);
fib(5);
fib(6);
```

## Run 
```
./lena source.lena
```
