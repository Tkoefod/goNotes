---
title: "Templates What are they"
lesson: 2
chapter: 2
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - stuff
    - other
---

### using range to iterate over a map, array etc inside an HTML template.

You can loop over a map or array inside an HTML template by using range.

```
{{ range $key, $value := .News}}
  <p>some stuff</p>

{{ end }}
```
