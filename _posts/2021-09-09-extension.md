---
layout: single
title:  "[Swift] Extension"

categories:
  - swift
tags:
  - [swift, extension]

toc: true
toc_sticky: true
---

## Extension
- add property

```swift
// Adding property to the standard data-type double structure.
extension Double {
    var squared: Double {
        return self * self
    }
}

let getSquared: Double = 3.0
print(getSquared.squared)
print(3.0.squared)

// 9.0
// 9.0
```