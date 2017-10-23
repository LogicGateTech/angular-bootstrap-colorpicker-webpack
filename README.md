This fork was made with a simple change to use var instead of let when requiring angular. Let usage was causing issues with UglifyJs in our webpack build.

# angular-bootstrap-colorpicker-webpack


### The Basics
  - Based on http://codepen.io/buberdds/full/fBAsr/
  - A webpack version of the this angular module

### Installation
Within your webpack module include CSS & JS
```
var angular = require('angular');

require('angular-bootstrap-colorpicker-webpack/src/colorpicker.css')
ngModule = angular.module('myModule', [
        require('angular-bootstrap-colorpicker-webpack')
    ])
require('./otherComponents')(ngModule);
module.exports = ngModule.name;
```

In your html add the `colorpicker` directive

```sh
<input colorpicker ng-model="myModel">
```

See the link above for indepth customization instructions.
