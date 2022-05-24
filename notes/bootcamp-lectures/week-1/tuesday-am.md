## Data Types

strings
boolean 
number (integer)
undefined (is something that doesn't exist)
null (is a value you assign to something when you want an empty value)
Symbol
BigInt

NaN
Object
Array

## Equality `==` vs `===`


## Named function
## anonymous function

## Arrow functions
### implicit return (no `return`)

## Function that accepts a function

## modules

In JS variables only exist in the file in which you created it.
To connect functions to other files you need to export it.

in file you are exporting from:
 - can contain multiple key value pairs to represent different functions

        module.exports == {
          helloFunc: hello,
          wassup, //don't need to add value
        }

in file you are importing into"

    const modules = require('./<file it is coming from>')