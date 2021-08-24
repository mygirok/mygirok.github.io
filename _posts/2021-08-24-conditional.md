---
layout: single
title:  "[Swift] Conditional"

categories:
  - swift
tags:
  - [swift, conditional, control Statement]

toc: true
toc_sticky: true
---
## If
```swift
var x = 10
if x > 5 {
    print("greater than 5")
}
```
## If -else
```swift
var x = 2
if x % 2 == 0 {
    print("even number")
} else {
    print("odd number")
}
```

## Guard
```swift
func fullName(firstName: String, lastName: String?) {
    if let surname = lastName {
        print(surname, firstName)
    } else {
        print("Don't have family name")
    }

    guard let surname = lastName else {
        print("Don't have family name")
        return
    }
    print(surname, firstName)
}

fullName(firstName: "Youn", lastName: "Kim")
```

## Switch-case
```swift
var value = 0
switch value {
    case 0:
        print("zero")
    case 1:
        print("one")
    case 2:
        print("two")
    default:
        print("greater than 3")
}
// zero

//where
var age = 20
switch age  {
    case 1...5 where age % 2 == 0:
        print("Toddler and even age")
    case 6...13 where age % 2 != 0:
        print("Kids and odd age")
    case 14...18 where age % 2 == 0:
        print("Youth and even age")
    default:
       print("Not in the condition");
}
```
> can use the WHERE in `switch`, `catch`, `if`, `while`, `guard`, `for` etc.