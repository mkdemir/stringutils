![Version](https://img.shields.io/badge/version-0.2.0-orange.svg)
![Test](https://github.com/mkdemir/stringutils-demo/actions/workflows/go.yml/badge.svg)
![Go](https://img.shields.io/github/go-mod/go-version/mkdemir/stringutils-demo)
[![Documentation](https://godoc.org/github.com/mkdemir/stringutils-demo?status.svg)](https://pkg.go.dev/github.com/mkdemir/stringutils-demo)
[![Go Report Card](https://goreportcard.com/badge/github.com/mkdemir/stringutils-demo)](https://goreportcard.com/report/github.com/mkdemir/stringutils-demo)

# stringutils

A basic golang package for demonstration purpose. Package currently contains 
only one function:

```go
func Reverse(s string) (string, error)
```

---

## Installation

Go to your project root, where `go.mod` file exists, than grab the library via:

```bash
go get github.com/mkdemir/stringutils-demo@latest
```

---

## Usage

```go
package main

import (
	"fmt"

	"github.com/mkdemir/stringutils-demo"
)

func main(){
	reversed, err := stringutils.Reverse("mkdemir")
	if err != nil {
		log.Fatal(err)
	}    
	fmt.Println(reversed) // ogiv
}
```

---

## Makefile

```bash
make help
```

Commands usage:

```bash
make <command>

commands:

test       run tests
testfuzz   run tests with fuzz (30 seconds)
bench      run benchmark tests
doc        run godoc server at 3000 unless PORT env-var is set
```

- `make test`: Runs tests
- `make testfuzz`: Runs Fuzzy tests for 30seconds (`go 1.18`)
- `make bench`: Runs benchmark tests
- `make doc`: Runs godoc server on port 3000. Use `PORT` environment variable
  for different port -> `PORT=4000 make doc`

---

## Contributor(s)

* [Uğur Özyılmazel](https://github.com/mkdemir) - Creator, maintainer

---

## Contribute

All PR’s are welcome!

1. `fork` (https://github.com/mkdemir/stringutils-demo/fork)
1. Create your `branch` (`git checkout -b my-feature`)
1. `commit` yours (`git commit -am 'add some functionality'`)
1. `push` your `branch` (`git push origin my-feature`)
1. Than create a new **Pull Request**!

---

## License

This project is licensed under MIT

---

This project is intended to be a safe, welcoming space for collaboration, and
contributors are expected to adhere to the [code of conduct][coc].

[coc]: https://github.com/mkdemir/stringutils-demo/blob/main/CODE_OF_CONDUCT.md