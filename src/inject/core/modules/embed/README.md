## `embed` module

Replaces the DOM with a 100% x 100% iframe

## Usage

```js
injectify.module('embed', 'http://example.com')
// undefined


injectify.module('embed', 'http://example.com').then((element) => {
    console.log(element.src)
})
// returns 'http://example.com'


injectify.module('embed', {
    url: 'http://example.com',
    interaction: false,
    hidden: true
}).then(element => {
    console.log(element.src)
})
// returns 'http://example.com'


injectify.module('embed').then(element => {
    element.src = 'http://example.com'
    element.style = 'background: #000'
})
// undefined
```