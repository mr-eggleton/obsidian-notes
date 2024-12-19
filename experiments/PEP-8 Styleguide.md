
# What is PEP-8?
PEP-8 is the official styleguide for Python-based applications. It covers how you should write python so that it is easy to read and understand, even for developers who are unexperienced with your codebase.

# What does it include?
It includes information on:
- Indentation
- Maximum Line Lengths
- Blank Lines
- Source code encoding
- Imports
- Whitespace
- Comments
- Naming Conventions

```python
print("PEP-8 Incompatible Code")

foo = long_function_name(var_one, var_two,
var_three, var_four)

def long_function_name(
var_one, var_two, var_three,
var_four):
    print(var_one)

if test:
	false # Tab

my_list = [
    1,
    2,
    3,
    4,
    5,
    6,
]

import sys, os

spam( ham[ 1 ], { eggs: 2 } )
bar = (0, )
if x == 4 : print(x , y) ; x , y = y , x

x = x + 1                 # Increment x
```


```python
print("PEP-8 Compliant Code")

# Arguments alligned with opening delimiter
foo = long_function_name(var_one, var_two,
                         var_three, var_four)

# An extra layer of indentation to distinguish arguments frm 
def long_function_name(
	    var_one, var_two, var_three,
        var_four):
    print(var_one)
    
# 4 Spaces instead of tab
if hello
.... return "world" # . indicate space

my_list = [
    1, 2, 3,
    4, 5, 6,
    ]

import os
import sys

# Avoid extranious whitespace
spam(ham[1], {eggs: 2})
foo = (0,)
if x == 4: print(x, y); x, y = y, x

x = x + 1                 # Compensate for border
```
