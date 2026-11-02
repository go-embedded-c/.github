# go-embedded-c

C for [go-notebook](https://github.com/go-notebook) cells, in pure Go (`CGO_ENABLED=0`), embeddable as a library and runnable in the browser through WebAssembly.

| repository | what it is | state |
|---|---|---|
| [c](https://github.com/go-embedded-c/c) | Front end for notebook cells (package `cell`: classification, hoisting, defines/uses, embedded wasi-libc headers), plus the clang → wasm32 oracle harness | M1 in progress, no release yet |

The plan is [go-scikit/roadmap `bib/c-cpp.md`](https://github.com/go-scikit/roadmap/blob/main/bib/c-cpp.md). It parses with modernc.org/cc/v4 and will add a C → wasm32 code generator and a cell runtime on wazero (desktop) and the browser's engine (playground). wasi-libc is the libc. Every stage is checked against clang 23.1.4 compiling to wasm32-wasip1 in the same engine.
