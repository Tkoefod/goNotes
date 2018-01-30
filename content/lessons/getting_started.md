---
title: "Getting Started"
lesson: 1
chapter: 1
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - stuff
    - gettingStarted
---

In GO programmers use camel case for names so things like 'CamelCase' or 'camelCase' but not 'camel_case'.

#### Main types of Declarations:

| name | type | syntax | example |
| --- | --- | --- | --- |
| var | variable | var name type = expression | var myVar int = 5 |
| const | constant |
| type | |
| func | function |


#### Types of Variables

| name | type | example |
| --- | --- | --- |
| int | integer number | 25 |
| float64 | long 64 bit decimal | 1.01234 |
| string | string | "some string" |
| bool | boolean | true |


#### Ways to declare

```
var i, j, k int
```
```
var b, f, g = true, 2.3, "text"
```

##### short variable declaration

these are very common although they can only be used inside a function and not globals.
```
variableName := "expression"
```

#### More on Declarations

functions in GO can return more then one value thus declarations are flexible for that too.

```
f, g := os.Open(name)
```
so in the above example f & g are both declared and assigned in one line simply.
