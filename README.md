## ramda tree shaking tests

> This repo is used for ramda tree shaking tests.

Comment / uncomment import methods before executing the following command to compare results:

 `ANALYZE=true npm run build`

See the [related issue](https://github.com/ramda/ramda/issues/2355#issuecomment-1058110641) for more informations.

## About babel-plugin-ramda

In order to enable [babel-plugin-ramda](https://github.com/megawac/babel-plugin-ramda), please create a `.babelrc` file:
```
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
