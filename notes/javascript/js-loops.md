> [home](../../home.md)
# Javascript Loop

## **_for Loop_**

> `for (let i = 0; i < 10; i++)`

### **Iterator**

`for (let i = 0; )`  
An initial expression with variable - like a counter.

### **Condition**

`i <10; `  
Dictates when the loop should end.

### **Cycle complete**

`i++`  
Defines what happens to the number `i` is currently representing. In this case, `i` is increasing by 1 (can be decremental or divided etc.)

**_For Example:_**

    for (let i = 0; i < 10; i++) {
      console.log('I have looped: ' + i + ' times!')
    }

Will print:

    I have looped: 0 times!
    I have looped: 1 times!
    I have looped: 2 times!
    I have looped: 3 times!
    I have looped: 4 times!
    I have looped: 5 times!
    I have looped: 6 times!
    I have looped: 7 times!
    I have looped: 8 times!
    I have looped: 9 times!

**_Another Example:_**

    let numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]

    console.log(numbers)

    for (let i = 0; i < numbers.length; i++) {
      console.log('I have looped: ' + i + ' times!')

      numbers[i]++
    }

    console.log(numbers)

Resulting in `i` iteratively adding 1 to 13 values

## **Exercises of Note:**

Write a function named 'printCountdown' that takes an array as a parameter  
It should loop in reverse through the length of the array and  
console.log each item with an exclamation mark added to the end.
// For example: printCountdown(['blast off', 'one', 'two', 'three']) would console.log "three! two! one! blast off!".
