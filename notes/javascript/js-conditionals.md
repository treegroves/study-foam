> [home](../../home.md)
# Javascript Conditionals

## What is a Conditional?

Conditional statements set conditions in Javascript code and run logic checks to determine if parts of the code can run or not.

## Examples of Statements

- `if` statement: if a condition is true, run x code
- `Else` statement: if a condition is false, do x
- `Else if` statement: a new test if condition is false

> Example 1:

        let name = 'barb'

        if (name == 'chloe') {
          console.log('hi chloe!')
        } else if (name == 'tim') {
          console.log('Hi tim!')
        } else {
          console.log('you are not cool')
        }

> Example 2:

        let age = 31

        if (age > 30) {
          console.log('you are old')
        } else {
          console.log('you are young')
        }

> Example 3:

        let age = 30

        if (age >= 30) {
          console.log('you are old')
        } else {
          console.log('you are young')
        }

### **_Activities of note:_**

**Switch Statement:**

    function chooseGreetingLanguage(string) {
      switch (string) {
        case 'Te Reo':
          return 'Kia ora'
          break

        case 'English':
          return 'Hello'
          break

        case 'Spanish':
          return 'Hola'
          break

        case 'Mandarin':
          return 'Nǐ hǎo'
          break

        case 'Samoan':
          return 'Talofa'
          break

        default:
          return '👋'
      }
    }

    chooseGreetingLanguage('English')

### **Ternary**

    function isSignedIn(isMember) {
      return isMember ? 'Log out' : 'Sign in'
    }

    console.log(isSignedIn(true))
    console.log(isSignedIn(false))
