# What is this about

This repository is meant to allow reproduction of [this issue](https://github.com/haskell-hint/hint/issues/78), in which
hint complains about a temporary directory not being empty:

```
$ stack exec -- hint-repro
no port specified, defaulting to port 8000
Listening on http://0.0.0.0:8000
hint-repro: /tmp/hint-c4f80210edfd53db: removeDirectory: unsatisfied constraints (Directory not empty)
```

# How to reproduce

1. Clone the repository
1. `stack build` (development mode is enabled by default)
1. `stack exec -- hint-repro`
1. Visit [http://localhost:8000/](http://localhost:8000/) in your browser
1. Error should appear in console
