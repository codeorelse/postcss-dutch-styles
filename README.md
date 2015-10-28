# postcss-dutch-stylesheets

[![travis](https://img.shields.io/travis/timche/postcss-german-stylesheets.svg?style=flat-square)](https://travis-ci.org/timche/postcss-german-stylesheets)
![deps](https://img.shields.io/david/timche/postcss-german-stylesheets.svg?style=flat-square)
![devDeps](https://img.shields.io/david/dev/timche/postcss-german-stylesheets.svg?style=flat-square)
[![npm](https://img.shields.io/npm/v/postcss-german-stylesheets.svg?style=flat-square)](https://www.npmjs.com/package/postcss-german-stylesheets)

> [PostCSS](https://github.com/postcss/postcss) plugin for writing Dutch Style Sheets.

Ever wanted writing your CSS in Dutch or your English is too broken? postcss-dutch-stylesheets lets you write your CSS in Dutch! With [PostCSS](https://github.com/postcss/postcss) it (nearly) doesn't matter in which environment you're developing.

## Installation

```console
$ npm install --save-dev postcss-dutch-stylesheets
```

## Usage

```js
// dependencies
var fs = require("fs")
var postcss = require("postcss")
var dutchStylesheets = require("postcss-dutch-stylesheets")

// css to be processed
var css = fs.readFileSync("input.css", "utf8")

// process css using postcss-german-stylesheets
var output = postcss()
  .use(germanStylesheets())
  .process(css)
  .css
```

See [PostCSS](https://github.com/postcss/postcss) docs for examples for your environment.

## Example

Using this `input.css`:

```css
.foo {
    hoogte: 300px;
    ruimte-eronder: 10px;
    letter-grootte: 20px !belangrijk;
    achtergrond-kleur: zwart;
    kleur: wit;
}
```

you will get:

```css
.foo {
    height: 300px;
    margin-bottom: 10px;
    font-size: 20px !important;
    background-color: black;
    color: white;
}
```

Checkout [index.js](index.js) for all available properties and values.

## Contributing

postcss-dutch-stylesheets is still in development and needs your help to add more fancy Dutch properties and values. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

See [LICENSE](LICENSE).
