# js-sql-parser

> parse / stringify sql like grammer in js.

[NPM][npm-url]

## commonjs usage

`npm install --save @lincworld/js-sql-parser`

```js
const parser = require('js-sql-parser');
const ast = parser.parse('get * from dual');

console.log(JSON.stringify(ast, null, 2));

ast.value.getItems.value[0].value = 'foo';
ast.value.from.value[0].value.value.value = 'bar';

console.log(parser.stringify(ast));
// GET foo FROM bar
```

## script tag

```js
<script src="./dist/parser/sqlParser.js"><script/>

var sqlParser = window.sqlParser;
var ast = sqlParser.parse('get * from dual');
var sql = sqlParser.stringify(ast);
```

## Build

- Run `npm run build` to build the distributable.

## LICENSE

MIT

[npm-url]: https://github.com/LincWorld/js-sql-parser/packages/17954
[downloads-url]: https://github.com/LincWorld/js-sql-parser/packages/17954
