> [home](../../home.md)
# JavaScript Variables

## What are variables?

**_Variables_** are containers to store and access information from.

## Creating Variables:

> Creating a Variable is referred to as **_declaring_** a Variable.

For Variables that will change use `let`:

    let name = "tim"
    let age = "33"

For Variables that will _not_ change use `const`:

    const name = "tim"
    const age = "33"

> Side Note: Variable values can be assigned to other Variables:

    let name1 = "tim"
    let name2 = "chloe"
    let name3 = name2

## Comments

> Create **_comments_** to leave explanatory notes for other yourself and other programmers.

    // this is a comment

## Data types

### **_String_**

> A **_String_** is a series of characters.

    let name = "tim"

### **_Number (integer)_**

> A **_number(int)_** datatype is an integer, or whole number.

    Let age = 33

### **_Number (float)_**

> A **_number(float)_** datatype is for number with a decimal.

    Let loveOfCats = 9.99

### Booleans

> A Boolean is either `True` or `false`.

    let isCool = true

## Other Variable Types

### **_Array_**

> An **_Array_** is a means for storing collections of information.
>
> > _They use index numbers to interact with items in the array. "Rose" = 0, "Daisy" = 1._

    let flowers = ["Rose", "Daisy"]

### **_Objects_**

> An **_Object_** is used to store **_Key Value Pairs_** of information.
>
> > _Items in the list are accessed through ***Keys***; "address", "contactNumber" and "emailAddress" are keys._

    let contactInfo = {
      address: "123 blah road",
      contactNumber: 0997807,
      emailAddress:
    }
