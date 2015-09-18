![JSS logo](http://avatars1.githubusercontent.com/u/9503099?v=3&s=60)

## JSS plugin that ensures style properties extend each other instead of override

Inspired by React Native. When using this plugin,
more specific properties will not be overwritten by less specific.

[Demo](http://jsstyles.github.io/jss-examples/index.html#plugin-jss-props-sort) -
[JSS](https://github.com/jsstyles/jss)

[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/jsstyles/jss?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


## Usage example

```javascript
import jss from 'jss'
import propsSort from 'jss-props-sort'

jss.use(propsSort)

const styleSheet = jss.createStyleSheet({
  container: {
    'border-left': '1px solid red',
    border: '3px solid green'
  }
})
```

```javascript
console.log(styleSheet.toString())
```
```css
.jss-0-0 {
  border: 3px solid green;
  border-left: 1px solid red;
}
```

```javascript
console.log(styleSheet.classes)
```
```javascript
{ container: "jss-0-0" }
```


## Run tests

### Locally

```bash
npm i
open test/local.html
```

### From github

[Tests](https://jsstyles.github.com/jss-props-sort/test)


## License

MIT
