# @swc/core behavior inconsistency between macOS and Linux

## To reproduce

Fist, install dependencies with command:

```bash
pnpm i
```

Second, execute `node index.js` file to reproduce the behavior.

## Expectation

It should work fine in macOS, but not in Linux. The following error is thrown in Linux:

```plain
Error: /dir_to_home/swc-inconsistency/node_modules/.pnpm/@swc+core-linux-x64-gnu@1.2.147/node_modules/@swc/core-linux-x64-gnu/swc.linux-x64-gnu.node: cannot allocate memory in static TLS block
    at Object.Module._extensions..node (internal/modules/cjs/loader.js:1122:18)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (/dir_to_home/swc-inconsistency/node_modules/.pnpm/@swc+core@1.2.147/node_modules/@swc/core/binding.js:181:45)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
```
