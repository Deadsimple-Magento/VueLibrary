[![Latest Stable Version](https://poser.pugx.org/deadsimple/vuelibrary/version)](https://packagist.org/packages/deadsimple/vuelibrary) [![Total Downloads](https://poser.pugx.org/deadsimple/vuelibrary/downloads)](https://packagist.org/packages/deadsimple/vuelibrary) [![License](https://poser.pugx.org/deadsimple/vuelibrary/license)](https://packagist.org/packages/deadsimple/vuelibrary)

# Deadsimple VueJS Magento2 Composer Library

This package allows you to use VueJs together with requirejs in your Magento2 setup straight out of the box

## Installation

Use composer to install the module: `composer require deadsimple/vuelibrary`

## Development mode

This module loads VueJS in minified production mode by default but is served with a developer version too, if you need VueJS in development mode change your `requirejs-config.js` to: 

```
var config = {
	paths: {
		Vue: 'Deadsimple_VueLibrary/js/lib/vue',
		vue: 'Deadsimple_VueLibrary/js/lib/require-vuejs',
	},
	shim: {
		Vue: {
			exports: 'Vue'
		}
	}
};
```

## Usage
Create a main js file to load through requirejs in this main.js file define `Vue` (with a capital V) and use `vue` (see the non capital v) to load your created vue components in this example `Searchinput.vue`. From this point on you can initialize vue the way your used to with the `new Vue()` initializer, please make sure you have a container available to run your VueJS code in `#essearch` in this example;


```
define([
  'Vue',
  'vue!components/SearchInput.vue'
], function (Vue) {
  'use strict';
  
   new Vue({
      el: '#essearch',
   });
})
``` 

### Version

This library loads: `Vue.js v2.6.14`

### TODO
- [ ] Create easier switch between production and development version of VueJS
- [ ] Add to library bundling if available

