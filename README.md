# go-config

[![tag](https://img.shields.io/github/tag/cyg-pd/go-config.svg)](https://github.com/cyg-pd/go-config/releases)
![Go Version](https://img.shields.io/badge/Go-%3E%3D%201.24-%23007d9c)
[![GoDoc](https://godoc.org/github.com/cyg-pd/go-config?status.svg)](https://pkg.go.dev/github.com/cyg-pd/go-config)
![Build Status](https://github.com/cyg-pd/go-config/actions/workflows/test.yml/badge.svg)
[![Go report](https://goreportcard.com/badge/github.com/cyg-pd/go-config)](https://goreportcard.com/report/github.com/cyg-pd/go-config)
[![Coverage](https://img.shields.io/codecov/c/github/cyg-pd/go-config)](https://codecov.io/gh/cyg-pd/go-config)
[![Contributors](https://img.shields.io/github/contributors/cyg-pd/go-config)](https://github.com/cyg-pd/go-config/graphs/contributors)
[![License](https://img.shields.io/github/license/cyg-pd/go-config)](./LICENSE)

## 🚀 Install

```sh
go get github.com/cyg-pd/go-config@v1
```

This library is v1 and follows SemVer strictly.

No breaking changes will be made to exported APIs before v2.0.0.

## 💡 Usage

You can import `config` using:

```go
package main

import (
	"log/slog"

	"github.com/cyg-pd/go-config"
)

// prepare environment variable
// $ export VIPER_ENV_PREFIX=abc
// $ export ABC_DB_DEFAULT_DSN=123.123.123.123
func init() {
  config.Parse()
}

func main() {
dsn := config.GetString("db.default.dsn")
	slog.Info(dsn) // 123.123.123.123
}
```
