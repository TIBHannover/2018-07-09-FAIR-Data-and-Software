---
source: md
title: "Python Modules and Packages"
output: markdown_document
teaching: 
exercises: 
questions:
- "How to make Python code more reusable?"
objectives:
- "Be able to create Python modules"
- "Be able to create Python package"
- "Know how to make installable Python package"
---

# Modules

Python has a way to put definitions in a file and use them in a script or in an interactive instance of the interpreter. Such a file is called a module; definitions from a module can be imported into other modules or into the main module (the collection of variables that you have access to in a script executed at the top level and in calculator mode).

Example of the module `fibo.py`.

```py
# Fibonacci numbers module

def fib(n):    # write Fibonacci series up to n
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b
    print()

def fib2(n):   # return Fibonacci series up to n
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a, b = b, a+b
    return result
```

Import this module in the interpreter.

```py
import fibo
fibo.fib(1000)
fibo.fib2(1000)
fibo.__name__

# assign local name
fib = fibo.fib
fib(500)
```

It is customary to put `import` statements at the beginning of the file.

You can import names from the module directly.

```py
from fibo import fib, fib2
fib(500)
# `fibo` will not be defined
```

You can import all the names that a module defines.

```py
from fibo import *
fib(500)
# all names except those begining with underscore `_` will be imported
```

Python programmers do not use this facility since it introduces an unknown set of names into the interpreter, possibly hiding some things you have already defined.

If the module name is followed by as, then the name following as is bound directly to the imported module.

```py
import fibo as fib
fib.fib(500)

from fibo import fib as fibonacci
fibonacci(500)
```

## Executing modules as scripts

Running Python mdule with:
`python fibo.py <arguments>`
the code in the module will be executed, just as if you imported it, but with the `__name__` set to `"__main__"`.

You can access first argument send to the script like that:

```
import sys
sys.argv[1]
# be careful, the arguments are strings
```

**Excercise:** modify `fibo` module so that it can be executed as script, take the argument and passes it to funtion `fib()`

You can make a the file usable as a script by adding following at the end of the module:

```py
if __name__ == "__main__":
    import sys
    fib(int(sys.argv[1]))
```

Execute the file as script with arguments
```py
python fibo.py 50
```

When you import the module, this code is not run.

## The `dir()` function

The built-in function dir() is used to find out which names a module defines.

```py
import fibo, sys
dir(fibo)
dir(sys)
```

Without arguments, dir() lists the names you have defined currently:

```py
a = [1,2,3,4,5,6,7]
import fibo
fib = fibo.fib
dir()
```

`dir()` does not list the names of built-in functions and variables. If you want a list of those, they are defined in the standard module `builtins`:

```py
import builtins
dir(builtins)
```

## Packages

Packages are a way of structuring Python’s module namespace by using “dotted module names”. For example, the module name A.B designates a submodule named B in a package named A.

Example of the package structure:

```
sound/                          Top-level package
      __init__.py               Initialize the sound package
      formats/                  Subpackage for file format conversions
              __init__.py
              wavread.py
              wavwrite.py
              aiffread.py
              aiffwrite.py
              auread.py
              auwrite.py
              ...
      effects/                  Subpackage for sound effects
              __init__.py
              echo.py
              surround.py
              reverse.py
              ...
      filters/                  Subpackage for filters
              __init__.py
              equalizer.py
              vocoder.py
              karaoke.py
              ...
```

`__init__.py` files are required to make Python treat the directories as containing packages. In the simplest case, `__init__.py` can just be an empty file.

**Excercise:** modify the `fibo` module to make it into a package.

### Importting * from a package

By default nothing will be imported from package with `*`. It's up to the developer to define which modules from the package will be imported. This can by done in `__init__.py` file:

```py
__all__ = ["module1", "module2"]
```

**Excercise:** Update `fibo` package to allow import of the module with `*`.

### Intra-package references

When having submodules, we can refer to other modules:

```py
from . import echo
from .. import formats
from ..filter import equalizer
```

# Packaging

So far we can only use modules located in the current working directory. In order to access it across your whole system it needs to be installed.

How to make a package into something that can be installed?

Put `setup.py` file in the same direcotry as your package (not the modules!).

Example of the `setup.py` file:

```py
from setuptools import setup

setup(name='funniest',
      version='0.1',
      description='The funniest joke in the world',
      url='http://github.com/storborg/funniest',
      author='Flying Circus',
      author_email='flyingcircus@example.com',
      license='MIT',
      packages=['funniest'],
      zip_safe=False)
```

**Excercise:** add `setup.py` file to `fibonacci` package

Now we can install the pockage in our system with:

```
pip install .
```

and access it from wherever we want.

## Creating a distribution

```
python setup.py sdist
```

This will create `dist/funniest-0.1.tar.gz` inside our top-level directory. If you like, copy that file to another host and try unpacking it and install it, just to verify that it works for you.

## References

This lesson is based on:

1. [Python Docs Moules Chapter](https://docs.python.org/3/tutorial/modules.html)
2. [Python Packaging Guide](http://python-packaging.readthedocs.io/en/latest/minimal.html)
