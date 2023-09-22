# mojo test 

## Installation

To use the Mojo language, you first need to download and install Mojo via [this link](https://developer.modular.com/download).

## Features of Mojo

1. **Speed**: Mojo boasts a speed about 35000 times faster than Python. This provides a significant advantage in high-performance programming.

2. **Python3 Support**: It supports all the syntax of Python3, making it easily accessible for developers familiar with Python.

3. **Supports Various Programming Paradigms**: It supports a wide range of programming paradigms including functional programming, procedural programming, and data science.

4. **Type System**: Python is a dynamically typed language; the data type of variables is not explicitly declared. On the other hand, Mojo is statically typed; you must explicitly declare the data type of variables.

5. **Usage**: Both Python and Mojo are powerful programming languages each with their own strengths and weaknesses. Generally speaking, while Python is suitable for general-purpose programming, Mojo is well-suited for machine learning and artificial intelligence applications.

## Using The Compiler
With the Mojo SDK, you can run a Mojo program from a terminal just like you would with Python. If your file name is hello.mojo (or hello.🔥—yes, file extensions can be emojis!), simply type mojo hello.mojo:

```shell
$ cat hello.🔥
def main():
    print("hello world")
    for x in range(9, 0, -3):
        print(x)
$ mojo hello.🔥
hello world
9
6
3
$
```

## Basic Systems Programming Extensions

### let and var Declarations

let represents immutable values while var represents mutable values; both provide scoped runtime value declarations.

```python 
def your_function(a, b):
    let c = a

    if c != b:
        let d = b
        print(d)

your_function(2, 3)
```

### Struct Types 

Mojo's struct types aid in performance improvement through better control over data organization and direct access to data fields.

```python 
struct MyPair:
    var first: Int
    var second: Int

    fn __init__(inout self, first: Int, second: Int):
        self.first = first
        self.second = second

    fn __lt__(self, rhs: MyPair) -> Bool:
        return self.first < rhs.first or (self.first == rhs.first and self.second < rhs.second)
```

### Strong Type Checking 

While Mojo allows flexible types like in Python it also lets you employ strict type checking which makes your code more predictable and manageable.

```python 
def pair_test() -> Bool:
    let p = MyPair(1, 2)
    return True  
```

### Overloaded Functions and Methods 

In Mojo functions can be defined without specifying argument data types allowing APIs that work dynamically by accepting arbitrary inputs.

```python 
struct Complex:
    var re: Float32
    var im: Float32

     fn __init__(inout self,x :Float32):
         """Constructs a complex number given a real number."""
         self.re = x 
         self.im=0.0
      
     fn __init__(inout self,r :Float32,i :Float32):
         """Constructs a complex number given its real & imaginary components."""
         self.re=r 
         Self.im=i   
```
