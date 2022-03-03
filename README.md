## ramda tree shaking tests

> This repo is used for ramda tree shaking tests.

Comment / uncomment import methods in `index.js`:
```js
// No tree shaking (200+ modules, heavy weight)
// import * as R from 'ramda'
// import { identity } from 'ramda'

// Working tree shaking (4 modules, lightweight)
// import identity from 'ramda/src/identity'

// Weird tree shaking (4 modules, but heavy weight)
// import identity from 'ramda/es/identity'
```

Then, execute the following command to compare results:

 ```bash
 ANALYZE=true npm run build
 ```

See the [related issue](https://github.com/ramda/ramda/issues/2355#issuecomment-1058110641) for more informations.

## About babel-plugin-ramda

In order to enable [babel-plugin-ramda](https://github.com/megawac/babel-plugin-ramda), please create a `.babelrc` file:
```js
// .babelrc
{
  "presets": [
    ["next/babel", {
      "ramda": {
        "useES": true
      }
    }]
  ]
}
```

And use the `import identity from 'ramda/es/identity'` import method.
