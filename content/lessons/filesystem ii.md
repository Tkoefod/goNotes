---
title: "File Operations"
lesson: 2
chapter: 4
cover: "https://unsplash.it/400/300/?random?BoldMage"
date: "01/01/2017"
category: "tech"
type: "lesson"
tags:
    - programming
    - channels
    - filesystem
---

#### Opening a File

* uses Package: os

```
f, err := os.Open("/tmp/dat")
```

#### Closing a File
You should always close the file when you are done with it.

```
f.close()
```

#### Reading a whole File (simple method)

* uses Package: ioutil.ReadFile

Reading an entire file at once (not efficient for large files).
```
  dat, err := ioutil.ReadFile("/tmp/dat")
  if err != nil { // check for error
      panic(err)
  }
  fmt.Print(string(dat))
```

#### Reading parts (bytes) of a file

Read some bytes from the beginning of the file. Allow up to 5 to be read but also note how many actually were read.

```
b1 := make([]byte, 5)
n1, err := f.Read(b1)
check(err)
fmt.Printf("%d bytes: %s\n", n1, string(b1))
```

Moving to a location in a file.
```
_, err = f.Seek(0, 0) // goes to beginning
```

Seek to a known location and start reading from there.

```
o2, err := f.Seek(6, 0)
check(err)
b2 := make([]byte, 2)
n2, err := f.Read(b2)
check(err)
fmt.Printf("%d bytes @ %d: %s\n", n2, o2, string(b2))
```

The above is more robust with the use of the 'io' package and ReadAtLeast function.

```
o3, err := f.Seek(6, 0)
check(err)
b3 := make([]byte, 2)
n3, err := io.ReadAtLeast(f, b3, 2)
check(err)
fmt.Printf("%d bytes @ %d: %s\n", n3, o3, string(b3))
```

Using the "bufio" package allows for better efficiency for many small reads and provides additional reading methods.

* uses package: bufio
```
r4 := bufio.NewReader(f)
b4, err := r4.Peek(5)
check(err)
fmt.Printf("5 bytes: %s\n", string(b4))
```

#### Writing a File

#### Appending to an existing File

#### Deleting a File
