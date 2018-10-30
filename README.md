napi
====
N-API C Interop for Kotlin/Native

## Installation

The `napi` package an be installed with various package managers.

### From NPM

```sh
$ npm install datkt/napi
```

**Note:** *This will install **napi** into `node_modules/napi`*

## Prerequisites

* [Kotlin/Native](https://github.com/JetBrains/kotlin-native) and the
  `konanc` command line program.
* [node\_api.h](https://www.gnu.org/software/make/)

## Usage

```sh
## Compile a shared library with 'module.kt' and link napi.klib found in `node_modules/`
$ konanc -r node_modules/@datkt -l napi/napi -p shared -o binding module.kt
$ mv libbinding.so binding.node
$ node -e "require('./binding')"
```

> TODO

## See Also

* https://nodejs.org/api/n-api.html

## License

MIT
