---
title: Matrix piral print
date: 2016-08-16 07:31:42
tags:
- algorithm
---
### Given a 2D array (matrix) named M, print all items of M in a spiral order, clockwise.
### For example: [
###  [1, 2, 3, 4, 5],
###  [6, 7, 8, 9, 10],
###  [11, 12, 13, 14, 15],
###  [16, 17, 18, 19, 20]
### ]

### 1   2   3   4   5
### 6   7   8   9  10
### 11  12  13  14  15
### 16  17  18  19  20

#### example:

```javascript
const arr = [
  [1, 2, 3, 4, 5],
  [6, 7, 8, 9, 10],
  [11, 12, 13, 14, 15],
  [16, 17, 18, 19, 20]
];
matrixSpiralPrint(arr);
// 1 2 3 4 5 10 15 20 19 18 17 16 11 6 7 8 9 14 13 12
```

<!-- more -->

<br>{% codepen narr dXaxkg 0 js 1540 100% %}
