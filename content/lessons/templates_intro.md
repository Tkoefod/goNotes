---
title: "Templates"
lesson: 1
chapter: 2
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - basic
    - templates
---

### HTML Templates

are stored in separate files normally in an html file that contains an mostly HTML segment along with handlebar like variables `{{ .variableName }}`.

#### defining template within the GO program

1. import HTML template library.
2. define the template file.
3. execute the template along with passing variables.

##### Import the library
` import io/html/template `

##### Define the template file
` t, _ := template.ParseFiles("templateName.html") ` //name of new template is "t" and we do not have an error variable.

##### Execute the template.
```
  p := MyTemplateStruct{
    Title: "someTile",
    OtherSomthing: "somethingElse",
    Num: 13} // struct to enable multiple values pass.
  t.Execute((w,p))
```
