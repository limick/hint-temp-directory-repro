# Purpose

This repository is meant to allow reproduction of [this issue](https://github.com/haskell-hint/hint/issues/78), in which
`hint` complains about a temporary directory not being empty when trying to delete it:

```
$ stack exec -- hint-repro
no port specified, defaulting to port 8000
Listening on http://0.0.0.0:8000
hint-repro: /tmp/hint-c4f80210edfd53db: removeDirectory: unsatisfied constraints (Directory not empty)
```

# How to reproduce

1. Clone this repository
1. `stack build` (note that development mode is enabled by default)
1. `stack exec -- hint-repro`
1. Visit [http://localhost:8000/](http://localhost:8000/) in your browser
1. Error similar to the above should appear in console

# Remarks

Note that the error also appears if we bump `hint` to 0.9.0 in `stack.yaml`.
