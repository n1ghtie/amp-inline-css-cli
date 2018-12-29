# amp-inline-critical-cli

This is a project, a slight modification of an existing npm module called [inline-critical](https://github.com/bezoerb/inline-critical). All Credit for developing the original packages goes to the guys who developed *inline-critical*.

##!Important

This sole purpose of this package is to assist in developing amp webpages, that require special `<style amp-custom></style>` attibute to be valid, and not to modify any external css like `google fonts api`, or `font-awesome`

## Installation

This module is installed via npm:

``` bash
$ npm install amp-inline-critical-cli
```


## CLI

Recommened usage in example below.
Works well with either `.html` or `.php` files.
```bash
amp-inline-critical-cli -c /path/to/css/main.css -h /path/to/index.html > /path/to/output/index.html
```
Run `amp-inline-critical-cli --help` to see the list of options.

## inline(html, styles, options?)

- `html` is the HTML you want to use to inline your critical styles, or any other styles
- `styles` are the styles you're looking to inline
- `options` is an optional configuration object
  - `minify` will minify the styles before inlining (default: true)
  - `extract` will remove the inlined styles from any stylesheets referenced in the HTML
  - `basePath` will be used when extracting styles to find the files references by `href` attributes
  - `ignore` ignore matching stylesheets when inlining.
  - `selector` defines the element used by loadCSS as a reference for inlining.

## License

No License
