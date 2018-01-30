---
title: "Concurrency 2"
lesson: 3
chapter: 3
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - channels
    - concurrency
---

### channels

example:

```
package main

import "fmt"

func foo(c chan int, someValue int){
  c <- someValue * 5
}

func main() {
  fooVal := make(chan int) // can include a struct.

  go foo(fooVal, 5)
  go foo(fooVal, 3)

  //v1 := <-fooVal
  //v2 := <-fooVal
  v1, v2 := <-fooVal, <-fooVal // This by default is blocking

  fmt.Println(v1,v2)
}
```
