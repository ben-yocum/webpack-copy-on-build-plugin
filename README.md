# webpack-copy-on-build-plugin

[Webpack](http://webpack.github.io/) plugin that will copy/paste files after build.

## Installation

```
npm install --save-dev webpack-copy-on-build-plugin
```

## Usage

In config file:

``` javascript
var WebpackCopyOnBuildPlugin = require('on-build-webpack');

// ...
  module: {
    plugins: [
      new WebpackCopyOnBuildPlugin([
         {
           from: config.output.path + '/app.[hash].js',
           to: config.output.path + '/app.js'
         },
         {
           from: config.output.path + '/app.[hash].js.map',
           to: config.output.path + '/app.js.map'
         }
        ])
    ]
  },
// ...
```
