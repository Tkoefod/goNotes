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
2. use the `flag.Arg` function to get the non-flag arguments in the form of a string ie.
```
firstArgument := flag.Arg(0)
```
3. use the `flag.Parse()` to flags (have a dash) like: `-d`
    - this sets the flags to their non-default values
    - `flag.Bool` &#151 sets a boolean flag
    - `flag.String` &#151 sets a string flag
    - take three arguments: name of the flag, default value for the flag, and a help message or error message that will print if flag errors.
```
var b = flag.Bool("b", false, "some help string")
var myString = flag.String("my string", " default my string", "some help string for myString")
```
