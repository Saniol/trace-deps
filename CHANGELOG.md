Changes
=======

## 0.4.8

* Bug: Remove `null` file results when passing a `packageIterator` to `resolve` library (manifests as of `resolve@1.22.0`).

## 0.4.7

* Bug: Match `ignores` prefixes to file paths that have internal relative imports in addition to non-relative imports.

## 0.4.6

* Bug: Handle built-in Node.js library detection and removal when `bailIfMissing: false`.
  [#76](https://github.com/FormidableLabs/trace-deps/pull/76)

## 0.4.5

* Feature: Handle modern ESM input types.
  [#57](https://github.com/FormidableLabs/trace-deps/issues/57) (*[@yankovalera][]*)

## 0.4.4

* Bug: Do not apply `package.json:exports` resolution to relative local file imports.
  [#70](https://github.com/FormidableLabs/trace-deps/issues/70)

## 0.4.3

* Bug: Handle (and ignore) additional passthrough wildcard `{ "./*": "./*.js" }`
  [#68](https://github.com/FormidableLabs/trace-deps/issues/68)
* Internal: Misc dependency updates.
* Infra: Upgrade `mock-fs` and enabled Node 16.3+.
  [#61](https://github.com/FormidableLabs/trace-deps/issues/61)

## 0.4.2

* Bug: Handle top-level `await` in source files.
  [#65](https://github.com/FormidableLabs/trace-deps/pull/65)

## 0.4.1

* Bug: Handle `class` fields (public, private, static).
  [#64](https://github.com/FormidableLabs/trace-deps/issues/64)

## 0.4.0

* Feature: Add full support for modern Node.js ESM and `exports`.
  [#49](https://github.com/FormidableLabs/trace-deps/issues/51)

## 0.3.9

* Bug/Feature: Support relative paths from package name root in `allowMissing`.
  [#49](https://github.com/FormidableLabs/trace-deps/issues/49)

## 0.3.8

* Feature: Support application source paths in `allowMissing` configuration.
  [#41](https://github.com/FormidableLabs/trace-deps/issues/41)

## 0.3.7

* Bug: Fix `allowMissing` when used with Node.js built-in modules.
  [#42](https://github.com/FormidableLabs/trace-deps/issues/42) (*[@martinnabhan][]*)

## 0.3.6

* Feature: Add `includeSourceMaps` parameter with support for source map file inclusion.
* Infra: Switch CI to GitHub Actions.

## 0.3.5

* Feature: Add `trace-deps` CLI.
* Feature: Add `bailOnMissing` parameter to `traceFile`/`traceFiles`.
* Feature: Add `dep` and `type` fields to `misses` array values returned by `traceFile`/`traceFiles`.

## 0.3.4

* Bug: Handle non-`.js|mjs|json` extensions in JS files and parse when directly included. (E.g, `require('./url-alphabet/index.cjs')`).
* Internal: Misc dependency updates.

## 0.3.3

* Feature: Add `extraImports` parameter to `traceFile`/`traceFiles`.

## 0.3.2

* Feature/Bug: More permissively parse JS code using `module` Acorn type first, with fallback to `script`.

## 0.3.1

* Chore: Minor internal refactor.

## 0.3.0

**Breaking**

* Feature: Change `traceFile|traceFiles` return object shape to `{ dependencies, misses }` to include imports that cannot be traced.
  [#25](https://github.com/FormidableLabs/trace-deps/issues/25)

**Features**

* Feature: Add tracing for template literal strings in imports (e.g., ``require(`tmpl-str`)``).

## 0.2.4

* Bug: Search for `index.json` files when no `package.json:main` is specified.

## 0.2.3

* Bug/Feature: Allow permissive handling of try/catch `require`s with `allowMissing` parameter.
  [#19](https://github.com/FormidableLabs/trace-deps/issues/19)

## 0.2.2

* Upgrade `node-acorn` to `^2.0.0`.

## 0.2.1

* Feature: Add `export *|{} from` ESM support.
  [#9](https://github.com/FormidableLabs/trace-deps/issues/9)

## 0.2.0

* Bug: Include `package.json` files that are needed for Node.js resolution.
  [#12](https://github.com/FormidableLabs/trace-deps/issues/12)

## 0.1.0

* Initial release.

[@martinnabhan]: https://github.com/martinnabhan
[@yankovalera]: https://github.com/yankovalera
