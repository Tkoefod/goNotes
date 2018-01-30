---
title: "Concurrency"
lesson: 2
chapter: 3
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - goroutines
    - concurrency
---

### Goroutines

* include 'go' infront of function to make it run async.
* ` go funcName() `

### sync package
allows the use of wait groups that empower us to include multiple goroutines into a single wait group and we can then do something once all those are complete.

```
  import "sync"
  var wg sync.WaitGroup
  wg.Add(1)
  wg.Wait()
  wg.Done()
```
* [Video Tutorial](https://www.youtube.com/watch?v=HRKfVjCB3lM)

### Defer statement
defines that something should only run after the rest of the function is complete.
* first in is last out if there are multiple defer statements.
* defer is a statement so it is included before the rest of the statement.
* defer statement runs even if the program panics.

```
defer fmt.Println("something")
```

```
defer wg.Done()
```
