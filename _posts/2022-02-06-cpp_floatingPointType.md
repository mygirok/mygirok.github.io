---
layout: single
title: "[C/C++] Floating Point Type"

categories:
  - cpp
tags:
  - [cpp, c, c++]

toc: true
toc_sticky: true
---

## Floating Point Type Print
```c++
#include <stdio.h>

int main(void)
{  
    printf("%lf\n", 123.45); // 123.450000
    printf("%.2lf\n", 123.45); // 123.45
    printf("%.0lf\n", 123.45); // 123
    printf("%.lf\n", 123.45); // 123

  return 0;
}
```

- `%lf` &nbsp;&nbsp;&nbsp; : Round off to the 7th decimal place.
- `%.2lf` : Round off to the 3th decimal place.
- `%.0lf` &nbsp;: Round off to the first decimal place.
- `%.lf`  &nbsp;&nbsp;&nbsp;: same with `%.0lf`.
