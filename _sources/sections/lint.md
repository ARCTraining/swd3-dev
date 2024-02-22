# Linting

## Naming conventions

Python conventions are governed largely by a set of documents called Python
Enhancement Proposals (PEP). You can see more about PEP index in the official
[Python website](https://www.python.org/dev/peps/).

The PEP related with python coding style is the
[PEP8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/).

This file has guidance for all layout related aspects. For instance we are
interested in the [Package and Module Names](https://www.python.org/dev/peps/pep-0008/#package-and-module-names) section.

> **Modules** should have short, all-lowercase names. *Underscores can be used* in
> the module name if it improves readability. Python **packages** should also have
> short, all-lowercase names, although the use of *underscores is discouraged*.

## Code formatting

Why does formatting matter?

- Code is read more often than written
- Setting up a formatter in your editor takes 5 minutes
- Those 5 minutes are redeemed across the lifetime of the project

### Ugly formatting example

Put the following into a file `myscript.py` and save it.

```bash
x = {  'a':37,'b':42,
'c':927}
y = 'hello '+       'world'
class foo  (     object  ):
   def f    (self   ):
       return       y **2
   def g(self, x :int,
       y : int=42
       ) -> int:
       return x--y
def f  (   a ) :
   return      37+-a[42-a :  y*3]
```

### Black Code Formatter

We chose [black](https://pypi.org/project/black/) because it has very few
options with which to fiddle.

First you need to install `Black` in your environment:

```bash
conda install black
```

Then, the simplest way to use is

```bash
black myscript.py
```

The code should be automatically formatted to:

```bash
x = {"a": 37, "b": 42, "c": 927}
y = "hello " + "world"

class foo(object):
    def f(self):
        return y ** 2

    def g(self, x: int, y: int = 42) -> int:
        return x - -y
```

```{warning}
Note that `black` just fix the code layout - this code still has syntax error!
```
