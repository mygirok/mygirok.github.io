---
layout: single
title: "[Go] Variable"

categories:
  - go
tags:
  - [go]

toc: true
toc_sticky: true
---

## Variable Declaration

```go
package main

import "fmt"

func main() {
    var a int = 1 // a variable declaration and initialization
    var msg string = "Hello World" // msg variable declaration and initialization

    var i int = 2 // basic form
    var j int // variable declaration
    var k = 3 // type omitted
    b := 4 // var keywords and type omitted
}
```