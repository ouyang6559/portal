---
title: File Style
slug: /docs/tutorials/cli/style
---

## Overview

goctl generation supports formatting of files and folders by naming styles that meet the normal reading habits of different developers, although in Golang, folders and filename instructions are recommended to use a full lowercase style, refer to <a href="https://google.github.io/styleguide/go/" target="_blank">Go Style</a>.

## Formatting symbols

In goctl code generated, the naming style of the files and folders can be formatted by `go` and `zero` compart-formatted symbols, such as common styled symbols below：

- lowercase: `gozero`
- camelcase: `goZero`
- snakecase: `go_zero`

## Formatting Symbol Table Reference

Assume that we have a source string `welcome_to_go_ner`with reference formatting table：

| Formatting symbols | Formatted string       | Note                                                                                     |
| ------------------ | ---------------------- | ---------------------------------------------------------------------------------------- |
| `gozero`           | `welcometogozero`      | lower case                                                                               |
| `goZero`           | `welcomeToGoZero`      | camel case                                                                               |
| `go_zero`          | `welcome_to_go_zero`   | snake case                                                                               |
| `Go#zero`          | `Welcome#to#go#zero`   | Custom separator like separator `#`                                                      |
| `GOZERO`           | `WELCOMETOGOZERO`      | upper case                                                                               |
| `_go#zero_`        | `_welcome#to#go#zero_` | Prefix, suffix and custom separators, use `_` as prefix and suffix, use `#` as separator |

::note illegal symbol

- go
- gOZero
- zero
- goZEro
- goZERo
- goZeRo
- foo
:::

## Usage

Formatting symbols used when goctl codes are generated by `style` parameters to control formatters, e.g.：

```bash
$ goctl api new demo --style gozero
$ goctl api new demo --style go_zero
$ goctl api new demo --style goZero
```
