# amp-inline-critical-cli

This is a project, a slight modification of an existing npm module called [inline-critical](https://github.com/bezoerb/inline-critical). All Credit for developing the original packages goes to the guys who developed *inline-critical*.

##!Important

This sole purpose of this package is to assist in developing amp webpages, that require special `<style amp-custom></style>` attibute to be valid, and not to modify any external css like `google fonts api`, or `font-awesome`

## Installation

This module is installed via npm:

``` bash
$ npm install amp-inline-css-cli
```


## CLI

inline-critical works well with standard input. 
You can either pass in the html 
```bash
cat index.html | amp-inline-css-cli critical.css
```
or just flip things around
```bash
cat critical.css | amp-inline-css-cli index.html
```
or pass in the fileas as an option
```bash
amp-inline-css-cli critical.css index.html
```
without having to worry about the correct order
```bash
amp-inline-css-cli index.html critical.css
```
Run `amp-inline-css-cli --help` to see the list of options.

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
