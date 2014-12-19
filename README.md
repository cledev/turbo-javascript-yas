#turbo-javascript-YAS
A collection of snippets for optimizing Javascript development productivity in Emacs using YASnippet, ported in large part from [turbo-javascript](https://atom.io/packages/turbo-javascript), with additions, omissions, and changes detailed below:

## Snippets
### Console

Quickly log things to the console

#### cl: console.log
```js
console.log($0);
```

#### ce: console.error
```js
console.error($0);
```

#### cw: console.warn
```js
console.warn($0);
```

### Flow Control

Fast expansion for common flow control statements

#### if: if statement
```js
if (${1:condition}) {
  $0
}
```

#### el: else statement
```js
else {
  $0
}
```

#### ei: else if statement
```js
else if (${1:condition}) {
  $0
}
```

#### fl: for loop
```js
for (var ${1:i} = 0, ${2:len} = ${3:iterable}.length; ${1:i} < ${2:len}; ${1:i}++) {
  $0
});
```

#### fi: for in loop
```js
for (var ${1:key} in ${2:source}) {
  if (${2:source}.hasOwnProperty(${1:key})) {
    $0
  }
}
```

#### wl: while loop
```js
while (${1:condition}) {
  $0
}
```

### Functions

Declare and manipulate functions with ease

#### f: single-line anonymous function
```js
function (${1:arguments}) {$0}
```

#### fn: named function
```js
function ${1:name} (${2:arguments}) {
  $0
}
```

#### iife: immediately-invoked function expression
```js
(function (${1:arguments}) {
  $0
})(${2});
```

#### fa: function apply
```js
${1:fn}.apply(${2:this}, ${3:arguments})
```

#### fc: function call
```js
${1:fn}.call(${2:this}, ${3:arguments})
```

#### fb: function bind
```js
${1:fn}.bind(${2:this}, ${3:arguments})
```

### Iterables

#### fe: for each loop
```js
${1:iterable}.forEach(function (${2:item}) {
  $0
})
```

#### map: map function
```js
${1:iterable}.map(function (${2:item}) {
  $0
})
```

#### reduce: reduce function
```js
${1:iterable}.reduce(function (${2:previous}, ${3:current}) {
  $0
}${4:, initial})
```

#### filter: filter function
```js
${1:iterable}.filter(function (${2:item}) {
  $0
})
```

### Objects and types

Shortcuts for dealing with types, objects, classes and inheritance.

#### kv: key/value pair
```js
${1:key}: ${2:'value'}$0
```

#### proto: prototype method (chainable)
```js
${1:Class}.prototype.${2:methodName} = function (${3:arguments}) {
  $0
}
```

#### tof: typeof obj === 'TypeName'
```js
typeof ${1:source} === '${2:undefined}'
```

#### iof: obj instanceof Constructor
```js
${1:source} instanceof ${2:Object}
```

### BDD testing

BDD-style testing shortcuts for Intern, Mocha, Jasmine and others

#### desc: describe
```js
describe('${1:description}', function () {
  $0
})
```
#### it: it
```js
it('${1:description}', function() {
  $0
})
```
#### ex: expect
```js
expect($1).$0
```
### Timers

Timer shortcuts

#### st: setTimeout
```js
setTimeout(function () {
  $0
}, ${1:delay});
```

#### si: setInterval
```js
setTimeout(function () {
  $0
}, ${1:delay});
```

### Node.js specifics

The following snippets apply only within Node.js or scripts with Browserify

#### cb: Node.js style callback
```js
function (err${1:, value}) {$0}
```

#### req: require a module
```js
${1:var ${2:variable}} = require('${3:module}')
```

#### exp: export member
```js
exports.${1:name} = ${2:value};
```

#### mexp: module.exports
```js
module.exports = ${1:name};
```

#### on: attach an event handler (chainable)
```js
${1:${2:emitter}.}on('${3:event}', function(${4:arguments}) {
  $0
})
```
