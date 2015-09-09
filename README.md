# PostCSS Initial  
[![Build Status][ci-img]][ci] [![NPM Module][npm-img]][npm] [![David DM][david-img]][david]

<img align="right" width="135" height="95"
     title="Philosopher’s stone, logo of PostCSS"
     src="http://postcss.github.io/postcss/logo-leftp.png">

[PostCSS] plugin to fallback `initial` keyword. Very useful in combination with
[postcss-autoreset][reset].

[PostCSS]: https://github.com/postcss/postcss
[ci-img]:  https://travis-ci.org/maximkoretskiy/postcss-initial.svg
[ci]:      https://travis-ci.org/maximkoretskiy/postcss-initial
[npm-img]: https://badge.fury.io/js/postcss-initial.svg
[npm]:     https://www.npmjs.com/package/postcss-initial
[david-img]:   https://david-dm.org/maximkoretskiy/postcss-initial.svg
[david]:   https://david-dm.org/maximkoretskiy/postcss-initial
[reset]:   https://github.com/maximkoretskiy/postcss-autoreset


```css
a {
  animation: initial;
  background: initial;
  white-space: initial;
}
```

```css
a {
  animation: none 0s ease 0s 1 normal none running;
  animation: initial;
  background: transparent none repeat 0 0 / auto auto padding-box border-box scroll;
  background: initial;
  white-space: normal;
  white-space: initial;
}
```

**Killer feature!**  
Universal reset from future css!
```css
a {
  all: initial;
}
```

```css
a {
  animation: none 0s ease 0s 1 normal none running;
  backface-visibility: visible;
  background: transparent none repeat 0% 0% / auto auto padding-box border-box scroll;
  border: medium none currentColor;
  border-radius: 0;
  border-collapse: separate;
  border-image: none;
  border-spacing: 0;
  bottom: auto;
  box-shadow: none;
  box-sizing: content-box;
  caption-side: top;
  clear: none;
  clip: auto;
  color: inherit;
  columns: auto;
  column-count: auto;
  column-fill: balance;
  column-gap: normal;
  column-rule: medium none currentColor;
  column-span: 1;
  column-width: auto;
  content: normal;
  counter-increment: none;
  counter-reset: none;
  cursor: auto;
  direction: ltr;
  display: inline;
  empty-cells: show;
  float: none;
  font: normal normal normal normal medium normal sans-serif;
  height: auto;
  hyphens: none;
  left: auto;
  letter-spacing: normal;
  line-height: normal;
  list-style: disc outside none;
  margin: 0;
  max-height: none;
  max-width: none;
  min-height: 0;
  min-width: 0;
  opacity: 1;
  orphans: 0;
  outline: medium none invert;
  overflow: visible;
  overflow-x: visible;
  overflow-y: visible;
  padding: 0;
  page-break-after: auto;
  page-break-before: auto;
  page-break-inside: auto;
  perspective: none;
  perspective-origin: 50% 50%;
  position: static;
  right: auto;
  tab-size: 8;
  table-layout: auto;
  text-align: inherit;
  text-align-last: auto;
  text-decoration: none solid currentColor;
  text-indent: 0;
  text-shadow: none;
  text-transform: none;
  top: auto;
  transform: none;
  transform-origin: 50% 50% 0;
  transform-style: flat;
  transition: none;
  unicode-bidi: normal;
  vertical-align: baseline;
  visibility: visible;
  white-space: normal;
  widows: 0;
  width: auto;
  word-spacing: normal;
  z-index: auto;
  all: initial;
}
```

## Options

### reset
Takes `string`.  
Describes what subset of rules should be unsetted with `all` property (to reduce code weight).  
Posible subsets: `all`, `inherited`.  
Default value: `'all'`.  

## Usage

```js
postcss([ require('postcss-all-property')({
  reset: 'inherited' // reset only inherited rules
}) ])
```

See [PostCSS] docs for examples for your environment.
