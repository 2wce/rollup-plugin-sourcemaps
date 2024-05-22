# rollup-plugin-sourcemaps

[![Version](https://img.shields.io/npm/v/rollup-plugin-sourcemaps2.svg)](https://www.npmjs.com/package/rollup-plugin-sourcemaps2)
[![License](https://img.shields.io/npm/l/rollup-plugin-sourcemaps2.svg)](https://github.com/2wce/rollup-plugin-sourcemaps/blob/main/LICENSE)
![Build Status](https://github.com/2wce/rollup-plugin-sourcemaps/actions/workflows/release.yml/badge.svg)

[Rollup](https://rollupjs.org) plugin for loading files with existing source maps.
Inspired by [webpack/source-map-loader](https://github.com/webpack/source-map-loader).

Works with rollup 4 or later.

This is building on top of the awesome work of [Max Davidson](https://github.com/maxdavidson/rollup-plugin-sourcemaps). The repo wasn't getting updates so I took it upon myself to keep a copy updated

If you use [rollup-plugin-babel](https://github.com/rollup/rollup-plugin-babel),
you might be able to use the [`inputSourceMap`](https://babeljs.io/docs/en/options#inputsourcemap) option instead of this plugin.

## Why?

- You transpile your files with source maps before bundling with rollup
- You consume external modules with bundled source maps

## Usage

```javascript
import sourcemaps from 'rollup-plugin-sourcemaps';

export default {
  input: 'src/index.js',
  plugins: [sourcemaps()],
  output: {
    sourcemap: true,
    file: 'dist/my-awesome-package.js',
  },
};
```
