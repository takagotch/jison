### jison
---
https://github.com/zaach/jison

```
npm install jison -g
jison calculator.jison

echo "2^32 / 1024" > testcalc
node calculator.js testcalc
```

```js
var Parser = require().Parser;

var grammar = {
  "lex": {
    "rules": [
      ["\\s+", "/* skip whitespace */"],
      ["[a-f0-9]+", "return 'HEX';"]
    ]
  },
  
  "bnf": {
    "hex_strings" :[ "hex_strings HEX",
          "HEX"]
  }
};

var parser = new Parser(grammar);

var parserSource = parser.generate();

parser.parse("adfe34bc e82a");
parser.parse("adfe34bc zxg");
```

```
```


