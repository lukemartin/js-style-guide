# JavaScript Style Guide

For my own reference.

[Coding Style](#styles)  
[Sublime Setup](#sublime-setup)  
[Sublime Plugins](#sublime-plugins)  

## [Coding Style](id:styles)

### General

Strict mode on. Wrap everything in a closure if need be:

```js
(function() {
  'use strict';
  // …
}());
```

2-space soft tabs. Always.

```js
var something = {
  one: 1,
  mow: true,
  items: [
    'one',
    'two',
    'three'
  ]
};
```

Single quotes. Always:

```js
var something = 'Hello there.';
var items = ['Hello', 'there'];
```

camelCase variable/function/property names:  
(Underscores look better, but the JS community seems to prefer camels.)

```js
var someVariable;
function doSomething(inputVar, fn) {};
```

### Variables

Single var statement with variable declarations without assignments:

```js
var one, two, three;
```

Multiple var statements with assignments:  
(See [http://benalman.com/news/2012/05/multiple-var-statements-javascript/]())

```js
var one = 1;
var two = 2;
var three = { wibble: 'wobble' };
```

camelCase variable/function/property names:

```js
var someVariable;
```

### Comments

Sentence-case. Speak as a human:

```js
// Iterate over the cats and make them mow
cats.forEach(function(){ … })
```

[JSDoc](http://usejsdoc.org/)-compliant documentation:

```js
/**
 * Does something totally pointless
 * @param  {string} one
 * @param  {string} two
 * @param  {string} three
 * @return {string}
 */
function someFunction(one, two, three) {
  return (one + two + three).join('');
}
```

## [Sublime Setup](id:#sublime-setup)

Always work inside a Sublime Project. Example [here](https://github.com/lukemartin/js-style-guide/blob/master/sample-project.sublime-project).

JavaScript/JSON-specific syntax settings [here](https://github.com/lukemartin/js-style-guide/blob/master/JavaScript.sublime-settings).

## [Sublime Plugins](id:#sublime-plugins)

Always favour project-specific config over global. Tailor to each project.

### JSHint

Install [SublimeLinter](https://github.com/SublimeLinter/SublimeLinter) and [JSHint](http://jshint.org/) from Package Manager.

Per-project JSHint config stored in `.jshintrc`. Example [here](https://github.com/lukemartin/js-style-guide/blob/master/.jshintrc).

Global config stored in `SublimeLinter.sublime-settings`. Example [here](https://github.com/lukemartin/js-style-guide/blob/master/SublimeLinter.sublime-settings).

### TernJS

Install [sublime-tern](https://github.com/emmetio/sublime-tern) from Package Manager.

Per-project config stored in `.tern-project`. Example [here](https://github.com/lukemartin/js-style-guide/blob/master/.tern-project).

Remember to use Tern's plugins config for any external libraries for extensive completion.

### JsFormat

Install [JsFormat](https://github.com/jdc0589/JsFormat) from Package Manger.

Per-project config stored in `.jsbeautifyrc`. Example [here](https://github.com/lukemartin/js-style-guide/blob/master/.jsbeautifyrc).

Global config stored in `JsFormat.sublime-settings`. Example [here](https://github.com/lukemartin/js-style-guide/blob/master/JsFormat.sublime-settings).

### DocBlockr

Install [DocBlockr](https://github.com/spadgos/sublime-jsdocs) from Package Manager.