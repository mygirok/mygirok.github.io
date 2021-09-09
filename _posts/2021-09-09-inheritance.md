---
layout: single
title:  "[Swift] Inheritance"

categories:
  - swift
tags:
  - [swift, inheritance]

toc: true
toc_sticky: true
---

## Superclass and subclass
- parent class is `super class`
- child class is `subclass`
- child class can use all things of parent class
- single inheritance.

```swift
class child: parent {}
// only one parent class
// multiple protocols.

class ViewController: UIViewController, UIPickerViewDelegate, UIPickerViewDataSource {}

// class className: parentName, protocolName1, protocolName2 {}
```

> Only class can inherit.

```swift
class Man {
	var age: Int = 1
	var weight: Double = 3.5
	func display() {
		print("Age is \(age), Weight is \(weight)")
	}
	init(age: Int, weight: Double) {
		self.age = age
		self.weight = weight
	}
}

class Student: Man {
// hava all things of parent class
}

var lee: Student = Student(age: 20, weight: 65.2)
lee.display()
print(lee.age)
```

## Super
```swift
class Man {
	var age: Int = 1
	var weight: Double = 3.5
	func display() {
		print("Age is \(age), Weight is \(weight)")
	}
	init(age: Int, weight: Double) {
		self.age = age
		self.weight = weight
	}
}

class Student: Man {
	var name: String = "Youn"
	func displayS() {
		print("Name is \(name), Age is \(age), Weight is \(weight)")	
	}
	init(age: Int, weight: Double, name: String) {
        // super
		super.init(age: age, weight: weight)
		self.name = name
	}
}

var lee: Student = Student(age: 20, weight: 65.2, name: "Kim")
lee.displayS()
lee.display()
// Name is Kim, Age is 20, Weight is 65.2
// Age is 20, Weight is 65.2
```

## Overriding
```swift
class Man {
	var age: Int = 1
	var weight: Double = 3.5
	func display() {
		print("Age is \(age), Weight is \(weight)")
	}
	init(age: Int, weight: Double) {
		self.age = age
		self.weight = weight
	}
}

class Student: Man {
	var name: String = "Youn"
    // overriding
	override func display() {
		print("Name is \(name), Age is \(age), Weight is \(weight)")	
	}
	init(age: Int, weight: Double, name: String) {
		super.init(age: age, weight: weight)
		self.name = name
	}
}

var lee: Student = Student(age: 20, weight: 65.2, name: "Kim")
lee.display()
// Name is Kim, Age is 20, Weight is 65.2
```