---
title: "Variables"
description: ""
date: 2020-04-09T16:20:00+02:00
author: Norbert Benczúr

summary: ''
weight: 3
draft: false
---

## Variables

The following example shows how to assign a value to a variable. We'll look different ways how it can be accomplished.

```go
package main

import "fmt"

func main() {
	// Declare the variable "code" with type "int"
	var code int
	// Assign a value to it
	code = 1234
	fmt.Printf("The code is %d\n", code)
}
```

We decleared the `code` of type `int`. If we don't assign value to it, go assigns a zero value:

```go
Type   | Zero value
---------------------
int    | 0
bool   | false
string | ""
...
```

We can decleare a variable and assign it on the same line:

```go
var code int = 1234
```

In the above line, we explicitly defined the `int` type. But that's not necessary in this case, go can infer it for us:

```go
code := 1234
```

This is very handy and compact way to say declare and assign at the same time.

Please note that it decleares a new a variable, the following exactly would not compile:

```go
code := 1234
code := 4567 // Error: no new variables on left side of :=
```

If you want to assign a new value, you need to use `=` only:

```go
code := 1234
code = 4567
```

### Assigning multiple variables

You can create multiple variables using `:=` on the same line:

```go
code, password := 1234, "admin"
```

This format can be used to assign a new value to an existing variable, as long there at least one new variable on the left hand side:

```go
oldVariable := "I'm old"
code, oldVariable := 1234, "I'm not that old"
```