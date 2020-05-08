---
title: "String formatting"
description: ""
date: 2020-04-09T16:20:00+02:00
author: Norbert Benczúr

summary: ''
weight: 4
draft: false
---

## String formatting

The `fmt` package contains functions to format strings.

```go
fmt.Println("Hello World!")
fmt.Printf("Hello World!\n")
fmt.Printf("Hello %s!\n", "World")
// Hello World!

name := "Norbert"
fmt.Printf("My name is %s\n", name)
// My name is Norbert

greet := "Hello"
msg := fmt.Sprintf("%s %s", greet, name)
fmt.Println(msg)
// Hello Norbert

code := 404
fmt.Fprintf(os.Stderr, "Error: %d\n", code)
// Error: 404
```

The most important ones are the **Print**, **Fprint** and **Sprint** functions.

- **Print** will format and write to the standard output.
- **Fprint** will format and write to the given *io.Writer*. That can be the standard output, standard error, a file, a network connection, etc.
- **Sprint** will format and return the resulting string.