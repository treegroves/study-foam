> [home](../../home.md)
# Javascript Objects

### **_Objects_**

> An **_Object_** is used to store **_Key Value Pairs_** of information.
>
> > _Items in the list are accessed through ***Keys***; "address", "contactNumber" and "emailAddress" are keys._

      let tim = {
        name: 'tim',
        age: 33,
        eyeColor: 'hazel',
        plants: ['Chives', 'Basil'],
        partner: 'chloe',
    }

### **_Accessing information from objects_**

> `console.log(tim)`

**Returns:**

    {name: 'tim', age: 33, eyeColor: 'hazel', plants: Array(2), partner: 'chloe'}
    age: 33
    eyeColor: "hazel"
    name: "tim"
    partner: "chloe"
    >plants: (2) ['Chives', 'Basil']
    >[[Prototype]]: Object

> `console.log(tim.age)` > **Returns:**

    33

### **_Object linked to an Object_**

> To access `key value` linked Objects

    let tim = {
      name: 'tim',
      age: 33,
      eyeColor: 'hazel',
      plants: ['Chives', 'Basil'],
      partner: 'chloe',
    }

    let chloe = {
      name: 'chloe',
      age: 31,
      eyeColor: 'brown',
      partner: tim,
    }

    console.log(chloe.partner)

> To add a `key value` to an Object

    tim.partner = chloe
    chloe.partner = tim

> To modify a `key value` to an Object

    chloe.age += 1

### **_Two ways to access information in an Object_**

> Square Bracket syntax:
> Dot syntax:

`console.log(tim.age)`  
It is limited to referencing keys in the Object directly

`console.log(chloe["age"])`

It allows you to used with variables to access information

**_To illustrate the difference:_**

> **Note:** **_Keys_** are translated into **_Strings_**

    let tim = {
      name: 'tim',
      age: 33,
      isCool: true,
      eyeColor: 'hazel',
      plants: ['Chives', 'Basil'],
    }

    let key = 'age'

    console.log(tim[key])

    console.log(tim.key)

> `console.log(tim[key])` returns "33" because it is searching the Object via a _Function_

> `console.log(tim.key)` returns "undefined" because it is searching the Object for a Key named "key"

## **Activities of Note:**

Create a variable called 'customer' and assign it the value of the `name` property from the `receipt` object.  
Make sure you access the object's property, do not just type the string name.

    const receipt = {
      price: 89.99,
      store: 'Ariels Diner',
      name: 'Marta',
    }

    let customer = receipt.name
