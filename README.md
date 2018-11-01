napi
====
N-API C Interop for Kotlin/Native

## Installation

```sh
$ npm install @datkt/napi
```

## Prerequisites

* [Kotlin/Native](https://github.com/JetBrains/kotlin-native) and the
  `konanc` command line program.
* [node\_api.h](https://github.com/nodejs/node/blob/master/src/node_api.h)

## Usage

```sh
## Compile a shared library with 'module.kt' and link napi.klib found in `node_modules/`

$ konanc -r node_modules/@datkt -l napi/napi -p shared -o binding module.kt ## Linux
$ konanc -r node_modules/@datkt -l napi/napi -p dynamic -o binding module.kt ## OSX

$ mv libbinding.so binding.node
$ node -e "require('./binding')"
```

> TODO

## See Also

* https://nodejs.org/api/n-api.html

## License

MIT
