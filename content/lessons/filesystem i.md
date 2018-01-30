---
title: "Filesystem"
lesson: 1
chapter: 4
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - channels
    - concurrency
---

#### Packages
* `path/filepath` &#151 filepath functions
* `os` &#151 main os functions
* `flag` &#151 used to get passed flags/parameters/arguments

#### How to collect passed flags/parameters/arguments to the GO program
1. import the `flag` Package ie.
```
import "flag"
```
2. use the `flag.Arg` function ie.
```
firstArgument := flag.Arg(0)
```
