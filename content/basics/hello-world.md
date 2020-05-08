---
title: "Hello World"
description: ""
date: 2020-04-08T20:51:04+02:00
author: Norbert Benczúr

summary: ''
weight: 1
draft: false
---

## Hello World

Create a new `main.go` file and add the following content:

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}
```

### Build

```sh
go build
```

This will build a binary for your OS and name it using the current folder name.
You can customize the output with the `-o` flag.

```sh
go build -o app
```

### Run

Just simply execute the binary that you built with the above command.

```sh
./app
# Hello World!
```

### Build an run

As long as you only have the `main.go` file, you can build and run with a single command:

```sh
go run main.go
# Hello World!
```
