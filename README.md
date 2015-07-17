# markdown-it-fenced-classes

**NOTE:** this is a fork of `markdown-it-container` with modified behavior such that the "name" of the fence is always mapped 1:1 to CSS classes on the rendered HTML `div`.  Note that the tests and documentation (beyond this file) have *not* been updated in this repository to reflect the behavioral change.

```
::: myclass1 myclass2
*here be dragons*
:::
```

```html
<div class="myclass1 myclass2">
<em>here be dragons</em>
</div>
```

## Example

```js
var md = require('markdown-it')();

md.use(require('markdown-it-fenced-classes'));

console.log(md.render('::: spoiler click me\n*content*\n:::\n'));

// Output:
//
// <div class="spoiler click me">
// <em>content</em>
// </div>
```

## License

[MIT](https://github.com/markdown-it/markdown-it-container/blob/master/LICENSE)
