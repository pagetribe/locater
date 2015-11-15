# Locater

Search for a pattern's line number and cursor in a multi-line input.

## Install

    npm install locater

## Usage

Locater supports string and regex matching. Below is an example showing both
usage.

*input.txt*
```txt
In my younger and more vulnerable years
my father gave me some advice that
I've been turning over in my mind ever since.
```

```js
var locater = require('locater');
var input = fs.readFileSync('./input.txt', {encoding: 'utf8'});

locater('my', input);
// => [{ line: 1, cursor: 4 }, { line: 2, cursor: 1 }, { line: 3, cursor: 27 }]

locater(/[a-zA-Z]{7}/, input);
// => [{ line: 1, cursor: 7 }, { line: 3, cursor: 11 }]
```

## Contributing

Feel free to open issues with bugs and feature requests.

## License

MIT