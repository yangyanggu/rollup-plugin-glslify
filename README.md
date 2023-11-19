# rollup-plugin-glslify

[![NPM Package][npm]][npm-url]
[![NPM Package][lgtm]][lgtm-url]

> fork自 [https://github.com/glslify/rollup-plugin-glslify](https://github.com/glslify/rollup-plugin-glslify) 调整rollup版本


Import GLSL strings with [glslify](https://github.com/glslify/glslify) (a node.js-style module system for GLSL).

```js
import frag from './shaders/frag.glsl';
console.log(frag);
```

## Installation

```sh
npm i -D rollup-plugin-glslify

# or

yarn add -D rollup-plugin-glslify
```

## Usage

```js
// rollup.config.js
import glslify from 'rollup-plugin-glslify';

export default {
    // ...
    plugins: [
        glslify()
    ]
};
```

## Options

```js
glslify(options)
```

```js
{
    // Default
    include: [
        '**/*.vs',
        '**/*.fs',
        '**/*.vert',
        '**/*.frag',
        '**/*.glsl'
    ],

    // Undefined by default
    exclude: 'node_modules/**',

    // Enabled by default
    compress: true

    // The compress option also accepts a function with its first argument
    // being the string containing the glslified shader code.
    // The function is expected to return a string (or object) - the compressed shader
}
```

[glslify API options](https://github.com/glslify/glslify#var-src--glslcompilesrc-opts)

## Changelog

* [Releases](https://github.com/glslify/rollup-plugin-glslify/releases)

## License

[MIT](LICENSE)


[npm]: https://img.shields.io/npm/v/@vuemap/rollup-plugin-glslify.svg
[npm-url]: https://www.npmjs.com/package/@vuemap/rollup-plugin-glslify
[lgtm]: https://img.shields.io/lgtm/alerts/github/yangyanggu/rollup-plugin-glslify.svg
[lgtm-url]: https://lgtm.com/projects/g/yangyanggu/rollup-plugin-glslify
