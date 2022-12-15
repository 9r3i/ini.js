
[![Author](https://img.shields.io/badge/author-9r3i-lightgrey.svg)](https://github.com/9r3i)
[![License](https://img.shields.io/github/license/9r3i/ini.js.svg)](https://github.com/9r3i/ini.js/blob/master/license.txt)
[![Forks](https://img.shields.io/github/forks/9r3i/ini.js.svg)](https://github.com/9r3i/ini.js/network)
[![Stars](https://img.shields.io/github/stars/9r3i/ini.js.svg)](https://github.com/9r3i/ini.js/stargazers)
[![Issues](https://img.shields.io/github/issues/9r3i/ini.js.svg)](https://github.com/9r3i/ini.js/issues)
[![Release](https://img.shields.io/github/release/9r3i/ini.js.svg)](https://github.com/9r3i/ini.js/releases)


# ini.js
Parse and build string of ini format


# Sample parse with multi-line value

```js
var str=`
[section]
key=value
another_key=another value

[another_section]
miltiline="this is value
of the milti-line ini format
and this is another line"
single="this is \"single\" line with quotes"
`;

var parsed=(new ini).parse(str);
console.log(parsed);
```


# Sample build

```js
var obj={
  section: {
    key: "value",
    another_key: "another value"
  }
};
var withSection=(new ini).build(obj,true),
withoutSection=(new ini).build(obj.section);
console.log(withSection,withoutSection);
```


# Closing
That's all there is to it.
Alhamdulillaah...
