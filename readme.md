# tachyons-css.github.io 4.0.0-beta

Documentation for Tachyons -- a performant, mobile-first, and 100% responsive modular css framework.

#### Stats

12116 | 1377 | 1526
---|---|---
bytes | selectors | declarations

## Installation

#### With [npm](https://npmjs.com)

```
npm install --save-dev tachyons-css.github.io
```

#### With Git

```
git clone https://github.com/tachyons-css/tachyons-css.github.io
```

## Usage

#### Using with [PostCSS](https://github.com/postcss/postcss)

Import the css module

```css
@import "tachyons-css.github.io";
```

Then process the CSS using the [`tachyons-cli`](https://github.com/tachyons-css/tachyons-cli)

```sh
$ npm i -g tachyons-cli
$ tachyons-cli path/to/css-file.css > dist/t.css
```

#### Using the CSS

The built CSS is located in the `css` directory. It contains an unminified and minified version.
You can either cut and paste that css or link to it directly in your html.

```html
<link rel="stylesheet" href="path/to/module/css/tachyons-css.github.io">
```

#### Development

The source CSS files can be found in the `src` directory.
Running `$ npm start` will process the source CSS and place the built CSS in the `css` directory.

## The CSS

```css
/*

  TACHYONS

*/
/* Variables */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
/**
 * 1. Set default font family to sans-serif.
 * 2. Prevent iOS and IE text size adjust after device orientation change,
 *    without disabling user zoom.
 */
html { font-family: sans-serif; /* 1 */ -ms-text-size-adjust: 100%; /* 2 */ -webkit-text-size-adjust: 100%; /* 2 */ }
/**
 * Remove default margin.
 */
body { margin: 0; }
/* HTML5 display definitions
   ========================================================================== */
/**
 * Correct `block` display not defined for any HTML5 element in IE 8/9.
 * Correct `block` display not defined for `details` or `summary` in IE 10/11
 * and Firefox.
 * Correct `block` display not defined for `main` in IE 11.
 */
article, aside, details, figcaption, figure, footer, header, hgroup, main, menu,
nav, section, summary { display: block; }
/**
 * 1. Correct `inline-block` display not defined in IE 8/9.
 * 2. Normalize vertical alignment of `progress` in Chrome, Firefox, and Opera.
 */
audio, canvas, progress, video { display: inline-block; /* 1 */ vertical-align: baseline; /* 2 */ }
/**
 * Prevent modern browsers from displaying `audio` without controls.
 * Remove excess height in iOS 5 devices.
 */
audio:not([controls]) { display: none; height: 0; }
/**
 * Address `[hidden]` styling not present in IE 8/9/10.
 * Hide the `template` element in IE 8/9/10/11, Safari, and Firefox < 22.
 */
[hidden], template { display: none; }
/* Links
   ========================================================================== */
/**
 * Remove the gray background color from active links in IE 10.
 */
a { background-color: transparent; }
/**
 * Improve readability of focused elements when they are also in an
 * active/hover state.
 */
a:active, a:hover { outline: 0; }
/* Text-level semantics
   ========================================================================== */
/**
 * Address styling not present in IE 8/9/10/11, Safari, and Chrome.
 */
abbr[title] { border-bottom: 1px dotted; }
/**
 * Address style set to `bolder` in Firefox 4+, Safari, and Chrome.
 */
b, strong { font-weight: bold; }
/**
 * Address styling not present in Safari and Chrome.
 */
dfn { font-style: italic; }
/**
 * Address variable `h1` font-size and margin within `section` and `article`
 * contexts in Firefox 4+, Safari, and Chrome.
 */
h1 { font-size: 2em; margin: 0.67em 0; }
/**
 * Address styling not present in IE 8/9.
 */
mark { background: #ff0; color: #000; }
/**
 * Address inconsistent and variable font size in all browsers.
 */
small { font-size: 80%; }
/**
 * Prevent `sub` and `sup` affecting `line-height` in all browsers.
 */
sub, sup { font-size: 75%; line-height: 0; position: relative; vertical-align: baseline; }
sup { top: -0.5em; }
sub { bottom: -0.25em; }
/* Embedded content
   ========================================================================== */
/**
 * Remove border when inside `a` element in IE 8/9/10.
 */
img { border: 0; }
/**
 * Correct overflow not hidden in IE 9/10/11.
 */
svg:not(:root) { overflow: hidden; }
/* Grouping content
   ========================================================================== */
/**
 * Address margin not present in IE 8/9 and Safari.
 */
figure { margin: 1em 40px; }
/**
 * Address differences between Firefox and other browsers.
 */
hr { box-sizing: content-box; height: 0; }
/**
 * Contain overflow in all browsers.
 */
pre { overflow: auto; }
/**
 * Address odd `em`-unit font size rendering in all browsers.
 */
code, kbd, pre, samp { font-family: monospace, monospace; font-size: 1em; }
/* Forms
   ========================================================================== */
/**
 * Known limitation: by default, Chrome and Safari on OS X allow very limited
 * styling of `select`, unless a `border` property is set.
 */
/**
 * 1. Correct color not being inherited.
 *    Known issue: affects color of disabled elements.
 * 2. Correct font properties not being inherited.
 * 3. Address margins set differently in Firefox 4+, Safari, and Chrome.
 */
button, input, optgroup, select, textarea { color: inherit; /* 1 */ font: inherit; /* 2 */ margin: 0; /* 3 */ }
/**
 * Address `overflow` set to `hidden` in IE 8/9/10/11.
 */
button { overflow: visible; }
/**
 * Address inconsistent `text-transform` inheritance for `button` and `select`.
 * All other form control elements do not inherit `text-transform` values.
 * Correct `button` style inheritance in Firefox, IE 8/9/10/11, and Opera.
 * Correct `select` style inheritance in Firefox.
 */
button, select { text-transform: none; }
/**
 * 1. Avoid the WebKit bug in Android 4.0.* where (2) destroys native `audio`
 *    and `video` controls.
 * 2. Correct inability to style clickable `input` types in iOS.
 * 3. Improve usability and consistency of cursor style between image-type
 *    `input` and others.
 */
button, html input[type="button"], /* 1 */
input[type="reset"],
input[type="submit"] { -webkit-appearance: button; /* 2 */ cursor: pointer; /* 3 */ }
/**
 * Re-set default cursor for disabled elements.
 */
button[disabled], html input[disabled] { cursor: default; }
/**
 * Remove inner padding and border in Firefox 4+.
 */
button::-moz-focus-inner, input::-moz-focus-inner { border: 0; padding: 0; }
/**
 * Address Firefox 4+ setting `line-height` on `input` using `!important` in
 * the UA stylesheet.
 */
input { line-height: normal; }
/**
 * It's recommended that you don't attempt to style these elements.
 * Firefox's implementation doesn't respect box-sizing, padding, or width.
 *
 * 1. Address box sizing set to `content-box` in IE 8/9/10.
 * 2. Remove excess padding in IE 8/9/10.
 */
input[type="checkbox"], input[type="radio"] { box-sizing: border-box; /* 1 */ padding: 0; /* 2 */ }
/**
 * Fix the cursor style for Chrome's increment/decrement buttons. For certain
 * `font-size` values of the `input`, it causes the cursor style of the
 * decrement button to change from `default` to `text`.
 */
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button { height: auto; }
/**
 * 1. Address `appearance` set to `searchfield` in Safari and Chrome.
 * 2. Address `box-sizing` set to `border-box` in Safari and Chrome.
 */
input[type="search"] { -webkit-appearance: textfield; /* 1 */ box-sizing: content-box; /* 2 */ }
/**
 * Remove inner padding and search cancel button in Safari and Chrome on OS X.
 * Safari (but not Chrome) clips the cancel button when the search input has
 * padding (and `textfield` appearance).
 */
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration { -webkit-appearance: none; }
/**
 * Define consistent border, margin, and padding.
 */
fieldset { border: 1px solid #c0c0c0; margin: 0 2px; padding: 0.35em 0.625em 0.75em; }
/**
 * 1. Correct `color` not being inherited in IE 8/9/10/11.
 * 2. Remove padding so people aren't caught out if they zero out fieldsets.
 */
legend { border: 0; /* 1 */ padding: 0; /* 2 */ }
/**
 * Remove default vertical scrollbar in IE 8/9/10/11.
 */
textarea { overflow: auto; }
/**
 * Don't inherit the `font-weight` (applied by a rule above).
 * NOTE: the default cannot safely be changed in Chrome and Safari on OS X.
 */
optgroup { font-weight: bold; }
/* Tables
   ========================================================================== */
/**
 * Remove most spacing between table cells.
 */
table { border-collapse: collapse; border-spacing: 0; }
td, th { padding: 0; }
/*

  CUSTOM MEDIA QUERIES

  Media query values can be changed to fit your own content.
  There are no magic bullets when it comes to media query width values.
  They should be declared in em units - and they should be set to meet
  the needs of your content.

  These media queries can be referenced like so:

  @media (--breakpoint-not-small) {
    .medium-and-larger-specific-style {
      background-color: red;
    }
  }

  @media (--breakpoint-medium) {
    .medium-screen-specific-style {
      background-color: red;
    }
  }

  @media (--breakpoint-large) {
    .large-screen-specific-style {
      background-color: red;
    }
  }

  @media (--breakpoint-extra-large) {
    .extra-large-screen-specific-style {
      background-color: red;
    }
  }

*/
/*

   Tachyons
   COLOR VARIABLES

   - Grayscale
   - Blues
   - Teals
   - Green
   - Reds
   - Oranges
   - Yellows
   - Pink
   - Purple

*/
/* Modules */
/*
  Box Sizing
*/
html, body, div, article, section, main, footer, header, form, fieldset, pre,
code, p, ul, ol, li, dl, dt, dd, textarea, input[type="text"], input[type="tel"],
input[type="email"], input[type="url"], input[type="password"], .border-box { box-sizing: border-box; }
/*

   BACKGROUND SIZE

   Base:
    bg = background-size

   Modifiers:
    -cv = cover
    -cn = contain

   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

*/
.bg-cv { background-size: cover; }
.bg-cn { background-size: contain; }
/*

   BORDER BASE

   Legend

   a = all
   t = top
   r = right
   b = bottom
   l = left

*/
.ba { border-style: solid; border-width: 1px; }
.bt { border-top-style: solid; border-top-width: 1px; }
.br { border-right-style: solid; border-right-width: 1px; }
.bb { border-bottom-style: solid; border-bottom-width: 1px; }
.bl { border-left-style: solid; border-left-width: 1px; }
/*

   Tachyons Colors

   Grayscale
   - Solids
   - Transparencies
*/
/*

   BORDER COLORS

*/
.b--black { border-color: #111; }
.b--near-black { border-color: #111; }
.b--dark-gray { border-color: #333; }
.b--mid-gray { border-color: #555; }
.b--gray { border-color: #777; }
.b--silver { border-color: #999; }
.b--light-silver { border-color: #aaa; }
.b--light-gray { border-color: #eee; }
.b--near-white { border-color: #f4f4f4; }
.b--white { border-color: #fff; }
.b--white-90 { border-color: rgba( 255, 255, 255, .9 ); }
.b--white-80 { border-color: rgba( 255, 255, 255, .8 ); }
.b--white-70 { border-color: rgba( 255, 255, 255, .7 ); }
.b--white-60 { border-color: rgba( 255, 255, 255, .6 ); }
.b--white-50 { border-color: rgba( 255, 255, 255, .5 ); }
.b--white-40 { border-color: rgba( 255, 255, 255, .4 ); }
.b--white-30 { border-color: rgba( 255, 255, 255, .3 ); }
.b--white-20 { border-color: rgba( 255, 255, 255, .2 ); }
.b--white-10 { border-color: rgba( 255, 255, 255, .1 ); }
.b--white-05 { border-color: rgba( 255, 255, 255, .05 ); }
.b--white-025 { border-color: rgba( 255, 255, 255, .025 ); }
.b--white-0125 { border-color: rgba( 255, 255, 255, .0125 ); }
.b--black-90 { border-color: rgba( 0, 0, 0, .9 ); }
.b--black-80 { border-color: rgba( 0, 0, 0, .8 ); }
.b--black-70 { border-color: rgba( 0, 0, 0, .7 ); }
.b--black-60 { border-color: rgba( 0, 0, 0, .6 ); }
.b--black-50 { border-color: rgba( 0, 0, 0, .5 ); }
.b--black-40 { border-color: rgba( 0, 0, 0, .4 ); }
.b--black-30 { border-color: rgba( 0, 0, 0, .3 ); }
.b--black-20 { border-color: rgba( 0, 0, 0, .2 ); }
.b--black-10 { border-color: rgba( 0, 0, 0, .1 ); }
.b--black-05 { border-color: rgba( 0, 0, 0, .05 ); }
.b--black-025 { border-color: rgba( 0, 0, 0, .025 ); }
.b--black-0125 { border-color: rgba( 0, 0, 0, .0125 ); }
.b--transparent { border-color: transprent; }
/*

   BORDER RADIUS

   Base:
     br   = border-radius

   Modifiers:
     n    = none
     1    = 1st step in scale
     2    = 2nd step in scale
     3    = 3rd step in scale
     4    = 4th step in scale
     5    = 5th step in scale
     circ = circle
     -100 = 100%

   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

*/
.brn { border-radius: 0; }
.br1 { border-radius: .125rem; }
.br2 { border-radius: .25rem; }
.br3 { border-radius: .5rem; }
.br4 { border-radius: 1rem; }
.br-100 { border-radius: 100%; }
/*

   BORDER STYLES

   Base:
     bs = border-style

   Modifiers:
     none   = none
     dotted = dotted
     dashed = dashed
     solid  = solid

   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

 */
.b--none { border-style: none; }
.b--dotted { border-style: dotted; }
.b--dashed { border-style: dashed; }
.b--solid { border-style: solid; }
/*

   BORDER WIDTHS

   Base:
     bw = border-width

   Modifiers:
     0 = 0 width border
     1 = 1st step in border-width scale
     2 = 2nd step in border-width scale
     3 = 3rd step in border-width scale
     4 = 4th step in border-width scale
     5 = 5th step in border-width scale

   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

*/
.bw0 { border-width: 0; }
.bw1 { border-width: .125rem; }
.bw2 { border-width: .25rem; }
.bw3 { border-width: .5rem; }
.bw4 { border-width: 1rem; }
.bw5 { border-width: 2rem; }
/*

   CODE

*/
.pre { overflow-x: auto; overflow-y: hidden; overflow: scroll; }
.code { white-space: pre; font-size: 14px; }
/*

   COORDINATES

   Use in combination with the position module.

*/
.top-0 { top: 0; }
.left-0 { left: 0; }
.right-0 { right: 0; }
.bottom-0 { bottom: 0; }
.top-1 { top: 1rem; }
.left-1 { left: 1rem; }
.right-1 { right: 1rem; }
.bottom-1 { bottom: 1rem; }
.top-2 { top: 2rem; }
.left-2 { left: 2rem; }
.right-2 { right: 2rem; }
.bottom-2 { bottom: 2rem; }
.top-4 { top: 4rem; }
.left-4 { left: 4rem; }
.right-4 { right: 4rem; }
.bottom-4 { bottom: 4rem; }
/*

   CLEARS

*/
/* Nicolas Gallaghers Clearfix solution
   Ref: http://nicolasgallagher.com/micro-clearfix-hack/ */
.cf:before, .cf:after { content: " "; display: table; }
.cf:after { clear: both; }
.cf { *zoom: 1; }
/*

   DISPLAY

   Base:
    d = display

   Modifiers:
    n     = none
    b     = block
    ib    = inline-block
    it    = inline-table
    t     = table
    tc    = table-cell
    tr    = table-row
    tcol  = table-column
    tcolg = table-column-group

   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

*/
.dn { display: none; }
.di { display: inline; }
.db { display: block; }
.dib { display: inline-block; }
.dit { display: inline-table; }
.dt { display: table; }
.dtc { display: table-cell; }
.dtcol { display: table-column; }
.dtcolg { display: table-column-group; }
/* Media Query Variables */
/*

   FLOATS

   1. Floated elements are automatically rendered as block level elements.
      Setting floats to display inline will fix the double margin bug in
      ie6. You know... just in case.

   2. Don't forget to clearfix your floats with .cf

   Base:
     f = float

   Modifiers:
     l = left
     r = right
     n = none

   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

*/
.fl { float: left; display: inline; }
.fr { float: right; display: inline; }
.fn { float: none; }
/*

   FONT FAMILY GROUPS

*/
.sans-serif { font-family: -apple-system, BlinkMacSystemFont, 'avenir next', avenir, helvetica, 'helvetica neue', Ubuntu, 'segoe ui', arial, sans-serif; }
.serif { font-family: georgia, times, serif; }
.system-sans-serif { font-family: sans-serif; }
.system-serif { font-family: serif; }
/* Monospaced Typefaces (for code) */
/* From http://cssfontstack.com */
code, .code { font-family: Consolas, monaco, monospace; }
/* Sans-Serif Typefaces */
.helvetica { font-family: helvetica, 'helvetica neue', arial, sans-serif; }
/* Serif Typefaces */
.georgia { font-family: georgia, serif; }
.times { font-family: Times, serif; }
.bodoni { font-family: "Bodoni MT", serif; }
.calisto { font-family: "Calisto MT", serif; }
.garamond { font-family: garamond, serif; }
/*

   FONT STYLE

*/
.i { font-style: italic; }
.fsn { font-style: normal; }
/*

   FONT WEIGHT

*/
.normal { font-weight: normal; }
.b { font-weight: bold; }
.fw1 { font-weight: 100; }
.fw2 { font-weight: 200; }
.fw3 { font-weight: 300; }
.fw4 { font-weight: 400; }
.fw5 { font-weight: 500; }
.fw6 { font-weight: 600; }
.fw7 { font-weight: 700; }
.fw8 { font-weight: 800; }
.fw9 { font-weight: 900; }
/*

   FORMS

*/
.input-reset { -webkit-appearance: none; -moz-appearance: none; }
.input-invisible { outline: 0; border: 0; }
/*

   HEIGHTS

*/
/* Height Scale */
.h1 { height: 1rem; }
.h2 { height: 2rem; }
.h3 { height: 4rem; }
.h4 { height: 8rem; }
.h5 { height: 16rem; }
/* Height Percentages */
.h-25 { height: 25%; }
.h-50 { height: 50%; }
.h-75 { height: 75%; }
.h-100 { height: 100%; }
/* String Properties */
.h-at { height: auto; }
.h-i { height: inherit; }
/*

   IMAGES

*/
/* Responsive images! */
img { max-width: 100%; }
/*

   LETTER SPACING

*/
.tracked { letter-spacing: .16em; }
.tracked-tight { letter-spacing: -.08em; }
.tracked-mega { letter-spacing: .32em; }
/*

   LINE HEIGHT / LEADING

*/
.lh { line-height: 1; }
.lh-title { line-height: 1.3; }
.lh-copy { line-height: 1.6; }
/*

   LINKS

*/
.link { text-decoration: none; transition: color .15s ease-in; }
.link:link, .link:visited { transition: color .15s ease-in; }
.link:hover { transition: color .15s ease-in; }
.link:active { transition: color .15s ease-in; }
.link:focus { transition: color .15s ease-in; }
/*

   LISTS

*/
.list { list-style-type: none; }
/*

   MAX WIDTHS

*/
/* Max Width Percentages */
.mw-100 { max-width: 100%; }
/* Max Width Scale */
.mw1 { max-width: 1rem; }
.mw2 { max-width: 2rem; }
.mw3 { max-width: 4rem; }
.mw4 { max-width: 8rem; }
.mw5 { max-width: 16rem; }
.mw6 { max-width: 32rem; }
.mw7 { max-width: 48rem; }
.mw8 { max-width: 64rem; }
.mw9 { max-width: 96rem; }
/* Max Width String Properties */
.mw-none { max-width: none; }
/*

   WIDTHS

   Base:
     w = width

   Modifiers
     1 = 1st step in width scale
     2 = 2nd step in width scale
     3 = 3rd step in width scale
     4 = 4th step in width scale
     5 = 5th step in width scale

     -10  = literal value 10%
     -20  = literal value 20%
     -25  = literal value 25%
     -33  = literal value 33%
     -34  = literal value 34%
     -40  = literal value 40%
     -50  = literal value 50%
     -60  = literal value 60%
     -75  = literal value 75%
     -80  = literal value 80%
     -100 = literal value 100%

     -auto  = string value auto


   Media Query Extensions:
     -ns = not-small
     -m  = medium
     -l  = large

*/
/* Width Scale */
.w1 { width: 1rem; }
.w2 { width: 2rem; }
.w3 { width: 4rem; }
.w4 { width: 8rem; }
.w5 { width: 16rem; }
.w-10 { width: 10%; }
.w-20 { width: 20%; }
.w-25 { width: 25%; }
.w-33 { width: 33%; }
.w-34 { width: 34%; }
.w-40 { width: 40%; }
.w-50 { width: 50%; }
.w-60 { width: 60%; }
.w-75 { width: 75%; }
.w-80 { width: 80%; }
.w-100 { width: 100%; }
.w-auto { width: auto; }
/*

    OVERFLOW

 */
.overflow-visible { overflow: visible; }
.overflow-hidden { overflow: hidden; }
.overflow-scroll { overflow: scroll; }
.overflow-auto { overflow: auto; }
.overflow-x-visible { overflow-x: visible; }
.overflow-x-hidden { overflow-x: hidden; }
.overflow-x-scroll { overflow-x: scroll; }
.overflow-x-auto { overflow-x: auto; }
.overflow-y-visible { overflow-y: visible; }
.overflow-y-hidden { overflow-y: hidden; }
.overflow-y-scroll { overflow-y: scroll; }
.overflow-y-auto { overflow-y: auto; }
/*

    POSITIONING

 */
.static { position: static; }
.relative { position: relative; }
.absolute { position: absolute; }
.fixed { position: fixed; }
/*

   COLOR VARIABLES

   Variables to set colors for
   color, background-color, and border-color

*/
/* variables */
/*

   SKINS

*/
/* Text colors */
.black-90 { color: rgba( 0, 0, 0, .9 ); }
.black-80 { color: rgba( 0, 0, 0, .8 ); }
.black-70 { color: rgba( 0, 0, 0, .7 ); }
.black-60 { color: rgba( 0, 0, 0, .6 ); }
.black-50 { color: rgba( 0, 0, 0, .5 ); }
.black-40 { color: rgba( 0, 0, 0, .4 ); }
.black-30 { color: rgba( 0, 0, 0, .3 ); }
.black-20 { color: rgba( 0, 0, 0, .2 ); }
.black-10 { color: rgba( 0, 0, 0, .1 ); }
.black-05 { color: rgba( 0, 0, 0, .05 ); }
.bg-black-90 { background-color: rgba( 0, 0, 0, .9 ); }
.bg-black-80 { background-color: rgba( 0, 0, 0, .8 ); }
.bg-black-70 { background-color: rgba( 0, 0, 0, .7 ); }
.bg-black-60 { background-color: rgba( 0, 0, 0, .6 ); }
.bg-black-50 { background-color: rgba( 0, 0, 0, .5 ); }
.bg-black-40 { background-color: rgba( 0, 0, 0, .4 ); }
.bg-black-30 { background-color: rgba( 0, 0, 0, .3 ); }
.bg-black-20 { background-color: rgba( 0, 0, 0, .2 ); }
.bg-black-10 { background-color: rgba( 0, 0, 0, .1 ); }
.bg-black-05 { background-color: rgba( 0, 0, 0, .05 ); }
.white-90 { color: rgba( 255, 255, 255, .9 ); }
.white-80 { color: rgba( 255, 255, 255, .8 ); }
.white-70 { color: rgba( 255, 255, 255, .7 ); }
.white-60 { color: rgba( 255, 255, 255, .6 ); }
.white-50 { color: rgba( 255, 255, 255, .5 ); }
.white-40 { color: rgba( 255, 255, 255, .4 ); }
.white-30 { color: rgba( 255, 255, 255, .3 ); }
.white-20 { color: rgba( 255, 255, 255, .2 ); }
.white-10 { color: rgba( 255, 255, 255, .1 ); }
.bg-white-90 { background-color: rgba( 255, 255, 255, .9 ); }
.bg-white-80 { background-color: rgba( 255, 255, 255, .8 ); }
.bg-white-70 { background-color: rgba( 255, 255, 255, .7 ); }
.bg-white-60 { background-color: rgba( 255, 255, 255, .6 ); }
.bg-white-50 { background-color: rgba( 255, 255, 255, .5 ); }
.bg-white-40 { background-color: rgba( 255, 255, 255, .4 ); }
.bg-white-30 { background-color: rgba( 255, 255, 255, .3 ); }
.bg-white-20 { background-color: rgba( 255, 255, 255, .2 ); }
.bg-white-10 { background-color: rgba( 255, 255, 255, .1 ); }
.black { color: #111; }
.near-black { color: #111; }
.dark-gray { color: #333; }
.mid-gray { color: #555; }
.gray { color: #777; }
.silver { color: #999; }
.light-silver { color: #aaa; }
.light-gray { color: #eee; }
.near-white { color: #f4f4f4; }
.white { color: #fff; }
/* Background colors */
.bg-black { background-color: #111; }
.bg-near-black { background-color: #111; }
.bg-dark-gray { background-color: #333; }
.bg-mid-gray { background-color: #555; }
.bg-gray { background-color: #777; }
.bg-silver { background-color: #999; }
.bg-light-silver { background-color: #aaa; }
.bg-light-gray { background-color: #eee; }
.bg-near-white { background-color: #f4f4f4; }
.bg-white { background-color: #fff; }
/* Skins for specific pseudoclasses */
.focus-black:focus { color: #111; }
.focus-near-black:focus { color: #111; }
.focus-dark-gray:focus { color: #333; }
.focus-mid-gray:focus { color: #555; }
.focus-gray:focus { color: #777; }
.focus-silver:focus { color: #999; }
.focus-light-silver:focus { color: #aaa; }
.focus-moon-gray:focus { color: #ccc; }
.focus-light-gray:focus { color: #eee; }
.focus-near-white:focus { color: #f4f4f4; }
.focus-white:focus { color: #fff; }
.bg-focus-black:focus { background-color: #111; }
.bg-focus-near-black:focus { background-color: #111; }
.bg-focus-dark-gray:focus { background-color: #333; }
.bg-focus-mid-gray:focus { background-color: #555; }
.bg-focus-gray:focus { background-color: #777; }
.bg-focus-silver:focus { background-color: #999; }
.bg-focus-light-silver:focus { background-color: #aaa; }
.bg-focus-moon-gray:focus { background-color: #ccc; }
.bg-focus-light-gray:focus { background-color: #eee; }
.bg-focus-near-white:focus { background-color: #f4f4f4; }
.bg-focus-white:focus { background-color: #fff; }
.hover-black:hover { color: #111; }
.hover-near-black:hover { color: #111; }
.hover-dark-gray:hover { color: #333; }
.hover-mid-gray:hover { color: #555; }
.hover-gray:hover { color: #777; }
.hover-silver:hover { color: #999; }
.hover-light-silver:hover { color: #aaa; }
.hover-moon-gray:hover { color: #ccc; }
.hover-light-gray:hover { color: #eee; }
.hover-near-white:hover { color: #f4f4f4; }
.hover-white:hover { color: #fff; }
.bg-hover-black:hover { background-color: #111; }
.bg-hover-near-black:hover { background-color: #111; }
.bg-hover-dark-gray:hover { background-color: #333; }
.bg-hover-mid-gray:hover { background-color: #555; }
.bg-hover-gray:hover { background-color: #777; }
.bg-hover-silver:hover { background-color: #999; }
.bg-hover-light-silver:hover { background-color: #aaa; }
.bg-hover-moon-gray:hover { background-color: #ccc; }
.bg-hover-light-gray:hover { background-color: #eee; }
.bg-hover-near-white:hover { background-color: #f4f4f4; }
.bg-hover-white:hover { background-color: #fff; }
/* Variables */
/* Media Queries */
/*
   SPACING

   An eight step powers of two scale ranging from 0 to 16rem.
   Namespaces are composab4e and thus high4y grockab4e - check the legend below

   Legend:

   p = padding
   m = margin

   a = all
   h = horizontal
   v = vertical
   t = top
   r = right
   b = bottom
   l = left

   n = none
   1 = extra small
   s = small
   m = medium
   l = large
   x = extra
   5 = extra large
   xxx = extra extra large

*/
.pa0 { padding: 0; }
.pa1 { padding: .25rem; }
.pa2 { padding: .5rem; }
.pa3 { padding: 1rem; }
.pa4 { padding: 2rem; }
.pa5 { padding: 4rem; }
.pa6 { padding: 8rem; }
.pa7 { padding: 16rem; }
.pl0 { padding-left: 0; }
.pl1 { padding-left: .25rem; }
.pl2 { padding-left: .5rem; }
.pl3 { padding-left: 1rem; }
.pl4 { padding-left: 2rem; }
.pl5 { padding-left: 4rem; }
.pl6 { padding-left: 8rem; }
.pl7 { padding-left: 16rem; }
.pr0 { padding-right: 0; }
.pr1 { padding-right: .25rem; }
.pr2 { padding-right: .5rem; }
.pr3 { padding-right: 1rem; }
.pr4 { padding-right: 2rem; }
.pr5 { padding-right: 4rem; }
.pr6 { padding-right: 8rem; }
.pr7 { padding-right: 16rem; }
.pb0 { padding-bottom: 0; }
.pb1 { padding-bottom: .25rem; }
.pb2 { padding-bottom: .5rem; }
.pb3 { padding-bottom: 1rem; }
.pb4 { padding-bottom: 2rem; }
.pb5 { padding-bottom: 4rem; }
.pb6 { padding-bottom: 8rem; }
.pb7 { padding-bottom: 16rem; }
.pt0 { padding-top: 0; }
.pt1 { padding-top: .25rem; }
.pt2 { padding-top: .5rem; }
.pt3 { padding-top: 1rem; }
.pt4 { padding-top: 2rem; }
.pt5 { padding-top: 4rem; }
.pt6 { padding-top: 8rem; }
.pt7 { padding-top: 16rem; }
.pv0 { padding-top: 0; padding-bottom: 0; }
.pv1 { padding-top: .25rem; padding-bottom: .25rem; }
.pv2 { padding-top: .5rem; padding-bottom: .5rem; }
.pv3 { padding-top: 1rem; padding-bottom: 1rem; }
.pv4 { padding-top: 2rem; padding-bottom: 2rem; }
.pv5 { padding-top: 4rem; padding-bottom: 4rem; }
.pv6 { padding-top: 8rem; padding-bottom: 8rem; }
.pv7 { padding-top: 16rem; padding-bottom: 16rem; }
.ph0 { padding-left: 0; padding-right: 0; }
.ph1 { padding-left: .25rem; padding-right: .25rem; }
.ph2 { padding-left: .5rem; padding-right: .5rem; }
.ph3 { padding-left: 1rem; padding-right: 1rem; }
.ph4 { padding-left: 2rem; padding-right: 2rem; }
.ph5 { padding-left: 4rem; padding-right: 4rem; }
.ph6 { padding-left: 8rem; padding-right: 8rem; }
.ph7 { padding-left: 16rem; padding-right: 16rem; }
.ma0 { margin: 0; }
.ma1 { margin: .25rem; }
.ma2 { margin: .5rem; }
.ma3 { margin: 1rem; }
.ma4 { margin: 2rem; }
.ma5 { margin: 4rem; }
.ma6 { margin: 8rem; }
.ma7 { margin: 16rem; }
.ml0 { margin-left: 0; }
.ml1 { margin-left: .25rem; }
.ml2 { margin-left: .5rem; }
.ml3 { margin-left: 1rem; }
.ml4 { margin-left: 2rem; }
.ml5 { margin-left: 4rem; }
.ml6 { margin-left: 8rem; }
.ml7 { margin-left: 16rem; }
.mr0 { margin-right: 0; }
.mr1 { margin-right: .25rem; }
.mr2 { margin-right: .5rem; }
.mr3 { margin-right: 1rem; }
.mr4 { margin-right: 2rem; }
.mr5 { margin-right: 4rem; }
.mr6 { margin-right: 8rem; }
.mr7 { margin-right: 16rem; }
.mb0 { margin-bottom: 0; }
.mb1 { margin-bottom: .25rem; }
.mb2 { margin-bottom: .5rem; }
.mb3 { margin-bottom: 1rem; }
.mb4 { margin-bottom: 2rem; }
.mb5 { margin-bottom: 4rem; }
.mb6 { margin-bottom: 8rem; }
.mb7 { margin-bottom: 16rem; }
.mt0 { margin-top: 0; }
.mt1 { margin-top: .25rem; }
.mt2 { margin-top: .5rem; }
.mt3 { margin-top: 1rem; }
.mt4 { margin-top: 2rem; }
.mt5 { margin-top: 4rem; }
.mt6 { margin-top: 8rem; }
.mt7 { margin-top: 16rem; }
.mv0 { margin-top: 0; margin-bottom: 0rem; }
.mv1 { margin-top: .25rem; margin-bottom: .25rem; }
.mv2 { margin-top: .5rem; margin-bottom: .5rem; }
.mv3 { margin-top: 1rem; margin-bottom: 1rem; }
.mv4 { margin-top: 2rem; margin-bottom: 2rem; }
.mv5 { margin-top: 4rem; margin-bottom: 4rem; }
.mv6 { margin-top: 8rem; margin-bottom: 8rem; }
.mv7 { margin-top: 16rem; margin-bottom: 16rem; }
.mh0 { margin-left: 0; margin-right: 0; }
.mh2 { margin-left: .5rem; margin-right: .5rem; }
.mh3 { margin-left: 1rem; margin-right: 1rem; }
.mh4 { margin-left: 2rem; margin-right: 2rem; }
.mh5 { margin-left: 4rem; margin-right: 4rem; }
.mh6 { margin-left: 8rem; margin-right: 8rem; }
.mh7 { margin-left: 16rem; margin-right: 16rem; }
/*

   TEXT DECORATION

*/
.strike { text-decoration: line-through; }
.underline { text-decoration: underline; }
.no-underline { text-decoration: none; }
/*

  TEXT ALIGN

*/
.tl { text-align: left; }
.tr { text-align: right; }
.tc { text-align: center; }
/*

   TEXT TRANSFORM

*/
.ttc { text-transform: capitalize; }
.ttl { text-transform: lowercase; }
.ttu { text-transform: uppercase; }
.ttn { text-transform: none; }
/*

   TYPE SCALE

*/
/* For Hero Titles */
.f-6-ns, .f-headline { font-size: 6rem; }
.f-5-ns, .f-subheadline { font-size: 5rem; }
/* Type Scale */
.f1 { font-size: 3rem; }
.f2 { font-size: 2.25rem; }
.f3 { font-size: 1.5rem; }
.f4 { font-size: 1.25rem; }
.f5 { font-size: 1rem; }
.f6 { font-size: .875rem; }
/*

   TYPOGRAPHY

*/
/* Measure is limited to ~75 characters */
.measure { max-width: 30em; }
/* Measure is limited to ~45 characters */
.measure-narrow { max-width: 20em; }
/* Book paragraph style - paragraphs are indented with no vertical spacing. */
.indent { text-indent: 1em; margin-top: 0; margin-bottom: 0; }
/* Combine this class with a width to truncate text */
.truncate { white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
/*

   UTILITIES

*/
.aspect-ratio { height: 0; position: relative; }
.aspect-ratio--16x9 { padding-bottom: 56.25%; }
.aspect-ratio--4x3 { padding-bottom: 75%; }
.aspect-ratio--8x5 { padding-bottom: 62.5%; }
.aspect-ratio--object { bottom: 0; height: 100%; left: 0; position: absolute; right: 0; top: 0; width: 100%; z-index: 100; }
.overflow-container { overflow-y: scroll; }
.center { margin-right: auto; margin-left: auto; }
/*

   VISIBILITY

*/
/*
    Text that is hidden but accessible
    Ref: http://snook.ca/archives/html_and_css/hiding-content-for-accessibility
*/
.clip { position: fixed !important; _position: absolute !important; clip: rect( 1px 1px 1px 1px ); /* IE6, IE7 */ clip: rect( 1px, 1px, 1px, 1px ); }
/*

   WHITE SPACE

*/
.ws-normal { white-space: normal; }
.nowrap { white-space: nowrap; }
.pre { white-space: pre; }
/*

   VERTICAL ALIGN

*/
.v-base { vertical-align: baseline; }
.v-sub { vertical-align: sub; }
.v-sup { vertical-align: super; }
.v-txt-top { vertical-align: text-top; }
.v-txt-btm { vertical-align: text-bottom; }
.v-mid { vertical-align: middle; }
.v-top { vertical-align: top; }
.v-btm { vertical-align: bottom; }
/*

  HOVER EFFECTS


*/
/* 
  
  Dim element on hover by adding the dim class.

*/
.dim { opacity: 1; transition: opacity .15s ease-in; }
.dim:hover, .dim:focus { opacity: .5; transition: opacity .15s ease-in; }
.dim:active { opacity: .8; transition: opacity .15s ease-out; }
/*

  Hide child on hover:

  Put the hide-child class on a parent element and any nested element with the
  child class will be hidden and displayed on hover or focus.

  <div class="hide-child">
    <div class="child"> Hidden until hover or focus </div>
    <div class="child"> Hidden until hover or focus </div>
    <div class="child"> Hidden until hover or focus </div>
    <div class="child"> Hidden until hover or focus </div>
  </div>
*/
.hide-child .child { opacity: 0; transition: opacity .15s ease-in; }
.hide-child:hover  .child, .hide-child:focus  .child, .hide-child:active .child { opacity: 1; transition: opacity .15s ease-in; }
/*

  STYLES

  Add custom styles here.

*/
/*

   GRADIENTS


*/
.gradient-blue { background-image: linear-gradient( #4570B0, #0081C2 ); }
.gradient-blue-reversed { background-image: linear-gradient( #0081C2, #4570B0 ); }
.gradient-light-blue { background-image: linear-gradient( #76D3FE, #008AE0 ); }
.gradient-light-blue-reversed { background-image: linear-gradient( #008AE0, #76D3FE ); }
/*

  DEBUG CHILDREN

  Just add the debug class to any element to see outlines on its
  children.

*/
.debug * { outline: 1px solid gold; }
/* Uncomment out this line if you want to debug your layout */
/* @import './_debug'; */
@media screen and (min-width: 48em) {
 .bg-cv-ns { background-size: cover; }
 .bg-cn-ns { background-size: contain; }
 .ba-ns { border-style: solid; border-width: 1px; }
 .bt-ns { border-top-style: solid; border-top-width: 1px; }
 .br-ns { border-right-style: solid; border-right-width: 1px; }
 .bb-ns { border-bottom-style: solid; border-bottom-width: 1px; }
 .bl-ns { border-left-style: solid; border-left-width: 1px; }
 .brn-ns { border-radius: 0; }
 .br1-ns { border-radius: .125rem; }
 .br2-ns { border-radius: .25rem; }
 .br3-ns { border-radius: .5rem; }
 .br4-ns { border-radius: 1rem; }
 .br-100-ns { border-radius: 100%; }
 .b--none-ns { border-style: none; }
 .b--dotted-ns { border-style: dotted; }
 .b--dashed-ns { border-style: dashed; }
 .b--solid-ns { border-style: solid; }
 .bw0-ns { border-width: 0; }
 .bw1-ns { border-width: .125rem; }
 .bw2-ns { border-width: .25rem; }
 .bw3-ns { border-width: .5rem; }
 .bw4-ns { border-width: 1rem; }
 .bw5-ns { border-width: 2rem; }
 .top-0-ns { top: 0; }
 .left-0-ns { left: 0; }
 .right-0-ns { right: 0; }
 .bottom-0-ns { bottom: 0; }
 .top-1-ns { top: 1rem; }
 .left-1-ns { left: 1rem; }
 .right-1-ns { right: 1rem; }
 .bottom-1-ns { bottom: 1rem; }
 .top-2-ns { top: 2rem; }
 .left-2-ns { left: 2rem; }
 .right-2-ns { right: 2rem; }
 .bottom-2-ns { bottom: 2rem; }
 .top-4-ns { top: 4rem; }
 .left-4-ns { left: 4rem; }
 .right-4-ns { right: 4rem; }
 .bottom-4-ns { bottom: 4rem; }
 .dn-ns { display: none; }
 .di-ns { display: inline; }
 .db-ns { display: block; }
 .dib-ns { display: inline-block; }
 .dit-ns { display: inline-table; }
 .dt-ns { display: table; }
 .dtc-ns { display: table-cell; }
 .dtcol-ns { display: table-column; }
 .dtcolg-ns { display: table-column-group; }
 .fl-ns { float: left; display: inline; }
 .fr-ns { float: right; display: inline; }
 .fn-ns { float: none !important; }
 .i-ns { font-style: italic; }
 .fsn-ns { font-style: normal; }
 .normal-ns { font-weight: normal; }
 .b-ns { font-weight: bold; }
 .fw1-ns { font-weight: 100; }
 .fw2-ns { font-weight: 200; }
 .fw3-ns { font-weight: 300; }
 .fw4-ns { font-weight: 400; }
 .fw5-ns { font-weight: 500; }
 .fw6-ns { font-weight: 600; }
 .fw7-ns { font-weight: 700; }
 .fw8-ns { font-weight: 800; }
 .fw9-ns { font-weight: 900; }
 .h-1-ns { height: 1rem; }
 .h-2-ns { height: 2rem; }
 .h-3-ns { height: 4rem; }
 .h-4-ns { height: 8rem; }
 .h-5-ns { height: 16rem; }
 .h-25-ns { height: 25%; }
 .h-50-ns { height: 50%; }
 .h-75-ns { height: 75%; }
 .h-100-ns { height: 100%; }
 .h-at-ns { height: auto; }
 .h-i-ns { height: inherit; }
 .tracked-ns { letter-spacing: .16em; }
 .tracked-tight-ns { letter-spacing: -.08em; }
 .tracked-mega-ns { letter-spacing: .32em; }
 .lh-ns { line-height: 1; }
 .lh-title-ns { line-height: 1.3; }
 .lh-copy-ns { line-height: 1.6; }
 .mw-100-ns { max-width: 100%; }
 .mw1-ns { max-width: 1rem; }
 .mw2-ns { max-width: 2rem; }
 .mw3-ns { max-width: 4rem; }
 .mw4-ns { max-width: 8rem; }
 .mw5-ns { max-width: 16rem; }
 .mw6-ns { max-width: 32rem; }
 .mw7-ns { max-width: 48rem; }
 .mw8-ns { max-width: 64rem; }
 .mw9-ns { max-width: 96rem; }
 .mw-none-ns { max-width: none; }
 .w1-ns { width: 1rem; }
 .w2-ns { width: 2rem; }
 .w3-ns { width: 4rem; }
 .w4-ns { width: 8rem; }
 .w5-ns { width: 16rem; }
 .w-10-ns { width: 10%; }
 .w-20-ns { width: 20%; }
 .w-25-ns { width: 25%; }
 .w-33-ns { width: 33%; }
 .w-34-ns { width: 34%; }
 .w-40-ns { width: 40%; }
 .w-50-ns { width: 50%; }
 .w-60-ns { width: 60%; }
 .w-75-ns { width: 75%; }
 .w-80-ns { width: 80%; }
 .w-100-ns { width: 100%; }
 .w-auto-ns { width: auto; }
 .overflow-visible-ns { overflow: visible; }
 .overflow-hidden-ns { overflow: hidden; }
 .overflow-scroll-ns { overflow: scroll; }
 .overflow-auto-ns { overflow: auto; }
 .overflow-x-visible-ns { overflow-x: visible; }
 .overflow-x-hidden-ns { overflow-x: hidden; }
 .overflow-x-scroll-ns { overflow-x: scroll; }
 .overflow-x-auto-ns { overflow-x: auto; }
 .overflow-y-visible-ns { overflow-y: visible; }
 .overflow-y-hidden-ns { overflow-y: hidden; }
 .overflow-y-scroll-ns { overflow-y: scroll; }
 .overflow-y-auto-ns { overflow-y: auto; }
 .static-ns { position: static; }
 .relative-ns { position: relative; }
 .absolute-ns { position: absolute; }
 .fixed-ns { position: fixed; }
 .pa0-ns { padding: 0; }
 .pa1-ns { padding: .25rem; }
 .pa2-ns { padding: .5rem; }
 .pa3-ns { padding: 1rem; }
 .pa4-ns { padding: 2rem; }
 .pa5-ns { padding: 4rem; }
 .pa6-ns { padding: 8rem; }
 .pa7-ns { padding: 16rem; }
 .pl0-ns { padding-left: 0; }
 .pl1-ns { padding-left: .25rem; }
 .pl2-ns { padding-left: .5rem; }
 .pl3-ns { padding-left: 1rem; }
 .pl4-ns { padding-left: 2rem; }
 .pl5-ns { padding-left: 4rem; }
 .pl6-ns { padding-left: 8rem; }
 .pl7-ns { padding-left: 16rem; }
 .pr0-ns { padding-right: 0; }
 .pr1-ns { padding-right: .25rem; }
 .pr2-ns { padding-right: .5rem; }
 .pr3-ns { padding-right: 1rem; }
 .pr4-ns { padding-right: 2rem; }
 .pr5-ns { padding-right: 4rem; }
 .pr6-ns { padding-right: 8rem; }
 .pr7-ns { padding-right: 16rem; }
 .pb0-ns { padding-bottom: 0; }
 .pb1-ns { padding-bottom: .25rem; }
 .pb2-ns { padding-bottom: .5rem; }
 .pb3-ns { padding-bottom: 1rem; }
 .pb4-ns { padding-bottom: 2rem; }
 .pb5-ns { padding-bottom: 4rem; }
 .pb6-ns { padding-bottom: 8rem; }
 .pb7-ns { padding-bottom: 16rem; }
 .pt0-ns { padding-top: 0; }
 .pt1-ns { padding-top: .25rem; }
 .pt2-ns { padding-top: .5rem; }
 .pt3-ns { padding-top: 1rem; }
 .pt4-ns { padding-top: 2rem; }
 .pt5-ns { padding-top: 4rem; }
 .pt6-ns { padding-top: 8rem; }
 .pt7-ns { padding-top: 16rem; }
 .pv0-ns { padding-top: 0; padding-bottom: 0; }
 .pv1-ns { padding-top: .25rem; padding-bottom: .25rem; }
 .pv2-ns { padding-top: .5rem; padding-bottom: .5rem; }
 .pv3-ns { padding-top: 1rem; padding-bottom: 1rem; }
 .pv4-ns { padding-top: 2rem; padding-bottom: 2rem; }
 .pv5-ns { padding-top: 4rem; padding-bottom: 4rem; }
 .pv6-ns { padding-top: 8rem; padding-bottom: 8rem; }
 .pv7-ns { padding-top: 16rem; padding-bottom: 16rem; }
 .ph0-ns { padding-left: 0; padding-right: 0; }
 .pv1-ns { padding-left: .25rem; padding-right: .25rem; }
 .ph2-ns { padding-left: .5rem; padding-right: .5rem; }
 .ph3-ns { padding-left: 1rem; padding-right: 1rem; }
 .ph4-ns { padding-left: 2rem; padding-right: 2rem; }
 .ph5-ns { padding-left: 4rem; padding-right: 4rem; }
 .ph6-ns { padding-left: 8rem; padding-right: 8rem; }
 .ph7-ns { padding-left: 16rem; padding-right: 16rem; }
 .ma0-ns { margin: 0; }
 .ma1-ns { margin: .25rem; }
 .ma2-ns { margin: .5rem; }
 .ma3-ns { margin: 1rem; }
 .ma4-ns { margin: 2rem; }
 .ma5-ns { margin: 4rem; }
 .ma6-ns { margin: 8rem; }
 .ma7-ns { margin: 16rem; }
 .ml0-ns { margin-left: 0; }
 .ml1-ns { margin-left: .25rem; }
 .ml2-ns { margin-left: .5rem; }
 .ml3-ns { margin-left: 1rem; }
 .ml4-ns { margin-left: 2rem; }
 .ml5-ns { margin-left: 4rem; }
 .ml6-ns { margin-left: 8rem; }
 .ml7-ns { margin-left: 16rem; }
 .mr0-ns { margin-right: 0; }
 .mr1-ns { margin-right: .25rem; }
 .mr2-ns { margin-right: .5rem; }
 .mr3-ns { margin-right: 1rem; }
 .mr4-ns { margin-right: 2rem; }
 .mr5-ns { margin-right: 4rem; }
 .mr6-ns { margin-right: 8rem; }
 .mr7-ns { margin-right: 16rem; }
 .mb0-ns { margin-bottom: 0; }
 .mb1-ns { margin-bottom: .25rem; }
 .mb2-ns { margin-bottom: .5rem; }
 .mb3-ns { margin-bottom: 1rem; }
 .mb4-ns { margin-bottom: 2rem; }
 .mb5-ns { margin-bottom: 4rem; }
 .mb6-ns { margin-bottom: 8rem; }
 .mb7-ns { margin-bottom: 16rem; }
 .mt0-ns { margin-top: 0; }
 .mt1-ns { margin-top: .25rem; }
 .mt2-ns { margin-top: .5rem; }
 .mt3-ns { margin-top: 1rem; }
 .mt4-ns { margin-top: 2rem; }
 .mt5-ns { margin-top: 4rem; }
 .mt6-ns { margin-top: 8rem; }
 .mt7-ns { margin-top: 16rem; }
 .mv0-ns { margin-top: 0; margin-bottom: 0rem; }
 .mv1-ns { margin-top: .25rem; margin-bottom: .25rem; }
 .mv2-ns { margin-top: .5rem; margin-bottom: .5rem; }
 .mv3-ns { margin-top: 1rem; margin-bottom: 1rem; }
 .mv4-ns { margin-top: 2rem; margin-bottom: 2rem; }
 .mv5-ns { margin-top: 4rem; margin-bottom: 4rem; }
 .mv6-ns { margin-top: 8rem; margin-bottom: 8rem; }
 .mv7-ns { margin-top: 16rem; margin-bottom: 16rem; }
 .mh0-ns { margin-left: 0; margin-right: 0; }
 .mh2-ns { margin-left: .5rem; margin-right: .5rem; }
 .mh3-ns { margin-left: 1rem; margin-right: 1rem; }
 .mh4-ns { margin-left: 2rem; margin-right: 2rem; }
 .mh5-ns { margin-left: 4rem; margin-right: 4rem; }
 .mh6-ns { margin-left: 8rem; margin-right: 8rem; }
 .mh7-ns { margin-left: 16rem; margin-right: 16rem; }
 .strike-ns { text-decoration: line-through; }
 .underline-ns { text-decoration: underline; }
 .no-underline-ns { text-decoration: none; }
 .tl-ns { text-align: left; }
 .tr-ns { text-align: right; }
 .tc-ns { text-align: center; }
 .ttc-ns { text-transform: capitalize; }
 .ttl-ns { text-transform: lowercase; }
 .ttu-ns { text-transform: uppercase; }
 .ttn-ns { text-transform: none; }
 .f-6-ns, .f-headline-ns { font-size: 6rem; }
 .f-5-ns, .f-subheadline-ns { font-size: 5rem; }
 .f1-ns { font-size: 3rem; }
 .f2-ns { font-size: 2.25rem; }
 .f3-ns { font-size: 1.5rem; }
 .f4-ns { font-size: 1.25rem; }
 .f5-ns { font-size: 1rem; }
 .f6-ns { font-size: .875rem; }
 .measure-ns { max-width: 30em; }
 .measure-narrow-ns { max-width: 20em; }
 .indent-ns { text-indent: 1em; margin-top: 0; margin-bottom: 0; }
 .truncate-ns { white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
 .clip-ns { position: fixed !important; position: absolute !important; clip: rect( 1px 1px 1px 1px ); /* IE6, IE7 */ clip: rect( 1px, 1px, 1px, 1px ); }
 .ws-normal-ns { white-space: normal; }
 .nowrap-ns { white-space: nowrap; }
 .pre-ns { white-space: pre; }
 .v-base-ns { vertical-align: baseline; }
 .v-sub-ns { vertical-align: sub; }
 .v-sup-ns { vertical-align: super; }
 .v-txt-top-ns { vertical-align: text-top; }
 .v-txt-btm-ns { vertical-align: text-bottom; }
 .v-mid-ns { vertical-align: middle; }
 .v-top-ns { vertical-align: top; }
 .v-btm-ns { vertical-align: bottom; }
}
@media screen and (min-width: 48em) and (max-width: 64em) {
 .bg-cv-m { background-size: cover; }
 .bg-cn-m { background-size: contain; }
 .ba-m { border-style: solid; border-width: 1px; }
 .bt-m { border-top-style: solid; border-top-width: 1px; }
 .br-m { border-right-style: solid; border-right-width: 1px; }
 .bb-m { border-bottom-style: solid; border-bottom-width: 1px; }
 .bl-m { border-left-style: solid; border-left-width: 1px; }
 .brn-m { border-radius: 0; }
 .br1-m { border-radius: .125rem; }
 .br2-m { border-radius: .25rem; }
 .br3-m { border-radius: .5rem; }
 .br4-m { border-radius: 1rem; }
 .br-100-m { border-radius: 100%; }
 .b--none-m { border-style: none; }
 .b--dotted-m { border-style: dotted; }
 .b--dashed-m { border-style: dashed; }
 .b--solid-m { border-style: solid; }
 .bw0-m { border-width: 0; }
 .bw1-m { border-width: .125rem; }
 .bw2-m { border-width: .25rem; }
 .bw3-m { border-width: .5rem; }
 .bw4-m { border-width: 1rem; }
 .bw5-m { border-width: 2rem; }
 .top-0-m { top: 0; }
 .left-0-m { left: 0; }
 .right-0-m { right: 0; }
 .bottom-0-m { bottom: 0; }
 .top-1-m { top: 1rem; }
 .left-1-m { left: 1rem; }
 .right-1-m { right: 1rem; }
 .bottom-1-m { bottom: 1rem; }
 .top-2-m { top: 2rem; }
 .left-2-m { left: 2rem; }
 .right-2-m { right: 2rem; }
 .bottom-2-m { bottom: 2rem; }
 .top-4-m { top: 4rem; }
 .left-4-m { left: 4rem; }
 .right-4-m { right: 4rem; }
 .bottom-4-m { bottom: 4rem; }
 .dn-m { display: none; }
 .di-m { display: inline; }
 .db-m { display: block; }
 .dib-m { display: inline-block; }
 .dit-m { display: inline-table; }
 .dt-m { display: table; }
 .dtc-m { display: table-cell; }
 .dtcol-m { display: table-column; }
 .dtcolg-m { display: table-column-group; }
 .fl-m { float: left; display: inline; }
 .fr-m { float: right; display: inline; }
 .fn-m { float: none; }
 .i-m { font-style: italic; }
 .fsn-m { font-style: normal; }
 .normal-m { font-weight: normal; }
 .b-m { font-weight: bold; }
 .fw1-m { font-weight: 100; }
 .fw2-m { font-weight: 200; }
 .fw3-m { font-weight: 300; }
 .fw4-m { font-weight: 400; }
 .fw5-m { font-weight: 500; }
 .fw6-m { font-weight: 600; }
 .fw7-m { font-weight: 700; }
 .fw8-m { font-weight: 800; }
 .fw9-m { font-weight: 900; }
 .h1-m { height: 1rem; }
 .h2-m { height: 2rem; }
 .h3-m { height: 4rem; }
 .h4-m { height: 8rem; }
 .h5-m { height: 16rem; }
 .h-25-m { height: 25%; }
 .h-50-m { height: 50%; }
 .h-75-m { height: 75%; }
 .h-100-m { height: 100%; }
 .h-at-m { height: auto; }
 .h-i-m { height: inherit; }
 .tracked-m { letter-spacing: .16em; }
 .tracked-tight-m { letter-spacing: -.08em; }
 .tracked-mega-m { letter-spacing: .32em; }
 .lh-m { line-height: 1; }
 .lh-title-m { line-height: 1.3; }
 .lh-copy-m { line-height: 1.6; }
 .mw-100-m { max-width: 100%; }
 .mw1-m { max-width: 1rem; }
 .mw2-m { max-width: 2rem; }
 .mw3-m { max-width: 4rem; }
 .mw4-m { max-width: 8rem; }
 .mw5-m { max-width: 16rem; }
 .mw6-m { max-width: 32rem; }
 .mw7-m { max-width: 48rem; }
 .mw8-m { max-width: 64rem; }
 .mw9-m { max-width: 96rem; }
 .mw-none-m { max-width: none; }
 .w1-m { width: 1rem; }
 .w2-m { width: 2rem; }
 .w3-m { width: 4rem; }
 .w4-m { width: 8rem; }
 .w5-m { width: 16rem; }
 .w-10-m { width: 10%; }
 .w-20-m { width: 20%; }
 .w-25-m { width: 25%; }
 .w-33-m { width: 33%; }
 .w-34-m { width: 34%; }
 .w-40-m { width: 40%; }
 .w-50-m { width: 50%; }
 .w-60-m { width: 60%; }
 .w-75-m { width: 75%; }
 .w-80-m { width: 80%; }
 .w-100-m { width: 100%; }
 .w-auto-m { width: auto; }
 .overflow-visible-m { overflow: visible; }
 .overflow-hidden-m { overflow: hidden; }
 .overflow-scroll-m { overflow: scroll; }
 .overflow-auto-m { overflow: auto; }
 .overflow-x-visible-m { overflow-x: visible; }
 .overflow-x-hidden-m { overflow-x: hidden; }
 .overflow-x-scroll-m { overflow-x: scroll; }
 .overflow-x-auto-m { overflow-x: auto; }
 .overflow-y-visible-m { overflow-y: visible; }
 .overflow-y-hidden-m { overflow-y: hidden; }
 .overflow-y-scroll-m { overflow-y: scroll; }
 .overflow-y-auto-m { overflow-y: auto; }
 .static-m { position: static; }
 .relative-m { position: relative; }
 .absolute-m { position: absolute; }
 .fixed-m { position: fixed; }
 .pa0-m { padding: 0; }
 .pa1-m { padding: .25rem; }
 .pa2-m { padding: .5rem; }
 .pa3-m { padding: 1rem; }
 .pa4-m { padding: 2rem; }
 .pa5-m { padding: 4rem; }
 .pa6-m { padding: 8rem; }
 .pa7-m { padding: 16rem; }
 .pl0-m { padding-left: 0; }
 .pl1-m { padding-left: .25rem; }
 .pl2-m { padding-left: .5rem; }
 .pl3-m { padding-left: 1rem; }
 .pl4-m { padding-left: 2rem; }
 .pl5-m { padding-left: 4rem; }
 .pl6-m { padding-left: 8rem; }
 .pl7-m { padding-left: 16rem; }
 .pr0-m { padding-right: 0; }
 .pr1-m { padding-right: .25rem; }
 .pr2-m { padding-right: .5rem; }
 .pr3-m { padding-right: 1rem; }
 .pr4-m { padding-right: 2rem; }
 .pr5-m { padding-right: 4rem; }
 .pr6-m { padding-right: 8rem; }
 .pr7-m { padding-right: 16rem; }
 .pb0-m { padding-bottom: 0; }
 .pb1-m { padding-bottom: .25rem; }
 .pb2-m { padding-bottom: .5rem; }
 .pb3-m { padding-bottom: 1rem; }
 .pb4-m { padding-bottom: 2rem; }
 .pb5-m { padding-bottom: 4rem; }
 .pb6-m { padding-bottom: 8rem; }
 .pb7-m { padding-bottom: 16rem; }
 .pt0-m { padding-top: 0; }
 .pt1-m { padding-top: .25rem; }
 .pt2-m { padding-top: .5rem; }
 .pt3-m { padding-top: 1rem; }
 .pt4-m { padding-top: 2rem; }
 .pt5-m { padding-top: 4rem; }
 .pt6-m { padding-top: 8rem; }
 .pt7-m { padding-top: 16rem; }
 .pv0-m { padding-top: 0; padding-bottom: 0; }
 .pv1-m { padding-top: .25rem; padding-bottom: .25rem; }
 .pv2-m { padding-top: .5rem; padding-bottom: .5rem; }
 .pv3-m { padding-top: 1rem; padding-bottom: 1rem; }
 .pv4-m { padding-top: 2rem; padding-bottom: 2rem; }
 .pv5-m { padding-top: 4rem; padding-bottom: 4rem; }
 .pv6-m { padding-top: 8rem; padding-bottom: 8rem; }
 .pv7-m { padding-top: 16rem; padding-bottom: 16rem; }
 .ph0-m { padding-left: 0; padding-right: 0; }
 .pv1-m { padding-left: .25rem; padding-right: .25rem; }
 .ph2-m { padding-left: .5rem; padding-right: .5rem; }
 .ph3-m { padding-left: 1rem; padding-right: 1rem; }
 .ph4-m { padding-left: 2rem; padding-right: 2rem; }
 .ph5-m { padding-left: 4rem; padding-right: 4rem; }
 .ph6-m { padding-left: 8rem; padding-right: 8rem; }
 .ph7-m { padding-left: 16rem; padding-right: 16rem; }
 .ma0-m { margin: 0; }
 .ma1-m { margin: .25rem; }
 .ma2-m { margin: .5rem; }
 .ma3-m { margin: 1rem; }
 .ma4-m { margin: 2rem; }
 .ma5-m { margin: 4rem; }
 .ma6-m { margin: 8rem; }
 .ma7-m { margin: 16rem; }
 .ml0-m { margin-left: 0; }
 .ml1-m { margin-left: .25rem; }
 .ml2-m { margin-left: .5rem; }
 .ml3-m { margin-left: 1rem; }
 .ml4-m { margin-left: 2rem; }
 .ml5-m { margin-left: 4rem; }
 .ml6-m { margin-left: 8rem; }
 .ml7-m { margin-left: 16rem; }
 .mr0-m { margin-right: 0; }
 .mr1-m { margin-right: .25rem; }
 .mr2-m { margin-right: .5rem; }
 .mr3-m { margin-right: 1rem; }
 .mr4-m { margin-right: 2rem; }
 .mr5-m { margin-right: 4rem; }
 .mr6-m { margin-right: 8rem; }
 .mr7-m { margin-right: 16rem; }
 .mb0-m { margin-bottom: 0; }
 .mb1-m { margin-bottom: .25rem; }
 .mb2-m { margin-bottom: .5rem; }
 .mb3-m { margin-bottom: 1rem; }
 .mb4-m { margin-bottom: 2rem; }
 .mb5-m { margin-bottom: 4rem; }
 .mb6-m { margin-bottom: 8rem; }
 .mb7-m { margin-bottom: 16rem; }
 .mt0-m { margin-top: 0; }
 .mt1-m { margin-top: .25rem; }
 .mt2-m { margin-top: .5rem; }
 .mt3-m { margin-top: 1rem; }
 .mt4-m { margin-top: 2rem; }
 .mt5-m { margin-top: 4rem; }
 .mt6-m { margin-top: 8rem; }
 .mt7-m { margin-top: 16rem; }
 .mv0-m { margin-top: 0; margin-bottom: 0rem; }
 .mv1-m { margin-top: .25rem; margin-bottom: .25rem; }
 .mv2-m { margin-top: .5rem; margin-bottom: .5rem; }
 .mv3-m { margin-top: 1rem; margin-bottom: 1rem; }
 .mv4-m { margin-top: 2rem; margin-bottom: 2rem; }
 .mv5-m { margin-top: 4rem; margin-bottom: 4rem; }
 .mv6-m { margin-top: 8rem; margin-bottom: 8rem; }
 .mv7-m { margin-top: 16rem; margin-bottom: 16rem; }
 .mh0-m { margin-left: 0; margin-right: 0; }
 .mh1-m { margin-left: .25rem; margin-right: .25rem; }
 .mh2-m { margin-left: .5rem; margin-right: .5rem; }
 .mh3-m { margin-left: 1rem; margin-right: 1rem; }
 .mh4-m { margin-left: 2rem; margin-right: 2rem; }
 .mh5-m { margin-left: 4rem; margin-right: 4rem; }
 .mh6-m { margin-left: 8rem; margin-right: 8rem; }
 .mh7-m { margin-left: 16rem; margin-right: 16rem; }
 .strike-m { text-decoration: line-through; }
 .underline-m { text-decoration: underline; }
 .no-underline-m { text-decoration: none; }
 .tl-m { text-align: left; }
 .tr-m { text-align: right; }
 .tc-m { text-align: center; }
 .ttc-m { text-transform: capitalize; }
 .ttl-m { text-transform: lowercase; }
 .ttu-m { text-transform: uppercase; }
 .ttn-m { text-transform: none; }
 .f-6-m, .f-headline-m { font-size: 6rem; }
 .f-5-m, .f-subheadline-m { font-size: 5rem; }
 .f1-m { font-size: 3rem; }
 .f2-m { font-size: 2.25rem; }
 .f3-m { font-size: 1.5rem; }
 .f4-m { font-size: 1.25rem; }
 .f5-m { font-size: 1rem; }
 .f6-m { font-size: .875rem; }
 .measure-m { max-width: 30em; }
 .measure-narrow-m { max-width: 20em; }
 .indent-m { text-indent: 1em; margin-top: 0; margin-bottom: 0; }
 .truncate-m { white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
 .clip-m { position: fixed !important; position: absolute !important; clip: rect( 1px 1px 1px 1px ); /* IE6, IE7 */ clip: rect( 1px, 1px, 1px, 1px ); }
 .ws-normal-m { white-space: normal; }
 .nowrap-m { white-space: nowrap; }
 .pre-m { white-space: pre; }
 .v-base-m { vertical-align: baseline; }
 .v-sub-m { vertical-align: sub; }
 .v-sup-m { vertical-align: super; }
 .v-txt-top-m { vertical-align: text-top; }
 .v-txt-btm-m { vertical-align: text-bottom; }
 .v-mid-m { vertical-align: middle; }
 .v-top-m { vertical-align: top; }
 .v-btm-m { vertical-align: bottom; }
}
@media screen and (min-width: 64em) {
 .bg-cv-l { background-size: cover; }
 .bg-cn-l { background-size: contain; }
 .ba-l { border-style: solid; border-width: 1px; }
 .bt-l { border-top-style: solid; border-top-width: 1px; }
 .br-l { border-right-style: solid; border-right-width: 1px; }
 .bb-l { border-bottom-style: solid; border-bottom-width: 1px; }
 .bl-l { border-left-style: solid; border-left-width: 1px; }
 .brn-l { border-radius: 0; }
 .br1-l { border-radius: .125rem; }
 .br2-l { border-radius: .25rem; }
 .br3-l { border-radius: .5rem; }
 .br4-l { border-radius: 1rem; }
 .br-100-l { border-radius: 100%; }
 .b--none-l { border-style: none; }
 .b--dotted-l { border-style: dotted; }
 .b--dashed-l { border-style: dashed; }
 .b--solid-l { border-style: solid; }
 .bw0-l { border-width: 0; }
 .bw1-l { border-width: .125rem; }
 .bw2-l { border-width: .25rem; }
 .bw3-l { border-width: .5rem; }
 .bw4-l { border-width: 1rem; }
 .bw5-l { border-width: 2rem; }
 .top-0-l { top: 0; }
 .left-0-l { left: 0; }
 .right-0-l { right: 0; }
 .bottom-0-l { bottom: 0; }
 .top-1-l { top: 1rem; }
 .left-1-l { left: 1rem; }
 .right-1-l { right: 1rem; }
 .bottom-1-l { bottom: 1rem; }
 .top-2-l { top: 2rem; }
 .left-2-l { left: 2rem; }
 .right-2-l { right: 2rem; }
 .bottom-2-l { bottom: 2rem; }
 .top-4-l { top: 4rem; }
 .left-4-l { left: 4rem; }
 .right-4-l { right: 4rem; }
 .bottom-4-l { bottom: 4rem; }
 .dn-l { display: none; }
 .di-l { display: inline; }
 .db-l { display: block; }
 .dib-l { display: inline-block; }
 .dit-l { display: inline-table; }
 .dt-l { display: table; }
 .dtc-l { display: table-cell; }
 .dtcol-l { display: table-column; }
 .dtcolg-l { display: table-column-group; }
 .fl-l { float: left; display: inline; }
 .fr-l { float: right; display: inline; }
 .fn-l { float: none; }
 .i-l { font-style: italic; }
 .fsn-l { font-style: normal; }
 .normal-l { font-weight: normal; }
 .b-l { font-weight: bold; }
 .fw1-l { font-weight: 100; }
 .fw2-l { font-weight: 200; }
 .fw3-l { font-weight: 300; }
 .fw4-l { font-weight: 400; }
 .fw5-l { font-weight: 500; }
 .fw6-l { font-weight: 600; }
 .fw7-l { font-weight: 700; }
 .fw8-l { font-weight: 800; }
 .fw9-l { font-weight: 900; }
 .h1-l { height: 1rem; }
 .h2-l { height: 2rem; }
 .h3-l { height: 4rem; }
 .h4-l { height: 8rem; }
 .h5-l { height: 16rem; }
 .h-25-l { height: 25%; }
 .h-50-l { height: 50%; }
 .h-75-l { height: 75%; }
 .h-100-l { height: 100%; }
 .h-at-l { height: auto; }
 .h-i-l { height: inherit; }
 .tracked-l { letter-spacing: .16em; }
 .tracked-tight-l { letter-spacing: -.08em; }
 .tracked-mega-l { letter-spacing: .32em; }
 .lh-l { line-height: 1; }
 .lh-title-l { line-height: 1.3; }
 .lh-copy-l { line-height: 1.6; }
 .mw-100-l { max-width: 100%; }
 .mw1-l { max-width: 1rem; }
 .mw2-l { max-width: 2rem; }
 .mw3-l { max-width: 4rem; }
 .mw4-l { max-width: 8rem; }
 .mw5-l { max-width: 16rem; }
 .mw6-l { max-width: 32rem; }
 .mw7-l { max-width: 48rem; }
 .mw8-l { max-width: 64rem; }
 .mw9-l { max-width: 96rem; }
 .mw-none-l { max-width: none; }
 .w1-l { width: 1rem; }
 .w2-l { width: 2rem; }
 .w3-l { width: 4rem; }
 .w4-l { width: 8rem; }
 .w5-l { width: 16rem; }
 .w-10-l { width: 10%; }
 .w-20-l { width: 20%; }
 .w-25-l { width: 25%; }
 .w-33-l { width: 33%; }
 .w-34-l { width: 34%; }
 .w-40-l { width: 40%; }
 .w-50-l { width: 50%; }
 .w-60-l { width: 60%; }
 .w-75-l { width: 75%; }
 .w-80-l { width: 80%; }
 .w-100-l { width: 100%; }
 .w-auto-l { width: auto; }
 .overflow-visible-l { overflow: visible; }
 .overflow-hidden-l { overflow: hidden; }
 .overflow-scroll-l { overflow: scroll; }
 .overflow-auto-l { overflow: auto; }
 .overflow-x-visible-l { overflow-x: visible; }
 .overflow-x-hidden-l { overflow-x: hidden; }
 .overflow-x-scroll-l { overflow-x: scroll; }
 .overflow-x-auto-l { overflow-x: auto; }
 .overflow-y-visible-l { overflow-y: visible; }
 .overflow-y-hidden-l { overflow-y: hidden; }
 .overflow-y-scroll-l { overflow-y: scroll; }
 .overflow-y-auto-l { overflow-y: auto; }
 .static-l { position: static; }
 .relative-l { position: relative; }
 .absolute-l { position: absolute; }
 .fixed-l { position: fixed; }
 .pa0-l { padding: 0; }
 .pa1-l { padding: .25rem; }
 .pa2-l { padding: .5rem; }
 .pa3-l { padding: 1rem; }
 .pa4-l { padding: 2rem; }
 .pa5-l { padding: 4rem; }
 .pa6-l { padding: 8rem; }
 .pa7-l { padding: 16rem; }
 .pl0-l { padding-left: 0; }
 .pl1-l { padding-left: .25rem; }
 .pl2-l { padding-left: .5rem; }
 .pl3-l { padding-left: 1rem; }
 .pl4-l { padding-left: 2rem; }
 .pl5-l { padding-left: 4rem; }
 .pl6-l { padding-left: 8rem; }
 .pl7-l { padding-left: 16rem; }
 .pr0-l { padding-right: 0; }
 .pr1-l { padding-right: .25rem; }
 .pr2-l { padding-right: .5rem; }
 .pr3-l { padding-right: 1rem; }
 .pr4-l { padding-right: 2rem; }
 .pr5-l { padding-right: 4rem; }
 .pr6-l { padding-right: 8rem; }
 .pr7-l { padding-right: 16rem; }
 .pb0-l { padding-bottom: 0; }
 .pb1-l { padding-bottom: .25rem; }
 .pb2-l { padding-bottom: .5rem; }
 .pb3-l { padding-bottom: 1rem; }
 .pb4-l { padding-bottom: 2rem; }
 .pb5-l { padding-bottom: 4rem; }
 .pb6-l { padding-bottom: 8rem; }
 .pb7-l { padding-bottom: 16rem; }
 .pt0-l { padding-top: 0; }
 .pt1-l { padding-top: .25rem; }
 .pt2-l { padding-top: .5rem; }
 .pt3-l { padding-top: 1rem; }
 .pt4-l { padding-top: 2rem; }
 .pt5-l { padding-top: 4rem; }
 .pt6-l { padding-top: 8rem; }
 .pt7-l { padding-top: 16rem; }
 .pv0-l { padding-top: 0; padding-bottom: 0; }
 .pv1-l { padding-top: .25rem; padding-bottom: .25rem; }
 .pv2-l { padding-top: .5rem; padding-bottom: .5rem; }
 .pv3-l { padding-top: 1rem; padding-bottom: 1rem; }
 .pv4-l { padding-top: 2rem; padding-bottom: 2rem; }
 .pv5-l { padding-top: 4rem; padding-bottom: 4rem; }
 .pv6-l { padding-top: 8rem; padding-bottom: 8rem; }
 .pv7-l { padding-top: 16rem; padding-bottom: 16rem; }
 .ph0-l { padding-left: 0; padding-right: 0; }
 .ph1-l { padding-left: .25rem; padding-right: .25rem; }
 .ph2-l { padding-left: .5rem; padding-right: .5rem; }
 .ph3-l { padding-left: 1rem; padding-right: 1rem; }
 .ph4-l { padding-left: 2rem; padding-right: 2rem; }
 .ph5-l { padding-left: 4rem; padding-right: 4rem; }
 .ph6-l { padding-left: 8rem; padding-right: 8rem; }
 .ph7-l { padding-left: 16rem; padding-right: 16rem; }
 .ma0-l { margin: 0; }
 .ma1-l { margin: .25rem; }
 .ma2-l { margin: .5rem; }
 .ma3-l { margin: 1rem; }
 .ma4-l { margin: 2rem; }
 .ma5-l { margin: 4rem; }
 .ma6-l { margin: 8rem; }
 .ma7-l { margin: 16rem; }
 .mlo-l { margin-left: 0; }
 .ml1-l { margin-left: .25rem; }
 .ml2-l { margin-left: .5rem; }
 .ml3-l { margin-left: 1rem; }
 .ml4-l { margin-left: 2rem; }
 .ml5-l { margin-left: 4rem; }
 .ml6-l { margin-left: 8rem; }
 .ml7-l { margin-left: 16rem; }
 .mr0-l { margin-right: 0; }
 .mr1-l { margin-right: .25rem; }
 .mr2-l { margin-right: .5rem; }
 .mr3-l { margin-right: 1rem; }
 .mr4-l { margin-right: 2rem; }
 .mr5-l { margin-right: 4rem; }
 .mr6-l { margin-right: 8rem; }
 .mr7-l { margin-right: 16rem; }
 .mb0-l { margin-bottom: 0; }
 .mb1-l { margin-bottom: .25rem; }
 .mb2-l { margin-bottom: .5rem; }
 .mb3-l { margin-bottom: 1rem; }
 .mb4-l { margin-bottom: 2rem; }
 .mb5-l { margin-bottom: 4rem; }
 .mb6-l { margin-bottom: 8rem; }
 .mb7-l { margin-bottom: 16rem; }
 .mt0-l { margin-top: 0; }
 .mt1-l { margin-top: .25rem; }
 .mt2-l { margin-top: .5rem; }
 .mt3-l { margin-top: 1rem; }
 .mt4-l { margin-top: 2rem; }
 .mt5-l { margin-top: 4rem; }
 .mt6-l { margin-top: 8rem; }
 .mt7-l { margin-top: 16rem; }
 .mv0-l { margin-top: 0; margin-bottom: 0rem; }
 .mv1-l { margin-top: .25rem; margin-bottom: .25rem; }
 .mv2-l { margin-top: .5rem; margin-bottom: .5rem; }
 .mv3-l { margin-top: 1rem; margin-bottom: 1rem; }
 .mv4-l { margin-top: 2rem; margin-bottom: 2rem; }
 .mv5-l { margin-top: 4rem; margin-bottom: 4rem; }
 .mv6-l { margin-top: 8rem; margin-bottom: 8rem; }
 .mv7-l { margin-top: 16rem; margin-bottom: 16rem; }
 .mh0-l { margin-left: 0; margin-right: 0; }
 .mh1-l { margin-left: .25rem; margin-right: .25rem; }
 .mh2-l { margin-left: .5rem; margin-right: .5rem; }
 .mh3-l { margin-left: 1rem; margin-right: 1rem; }
 .mh4-l { margin-left: 2rem; margin-right: 2rem; }
 .mh5-l { margin-left: 4rem; margin-right: 4rem; }
 .mh6-l { margin-left: 8rem; margin-right: 8rem; }
 .mh7-l { margin-left: 16rem; margin-right: 16rem; }
 .strike-l { text-decoration: line-through; }
 .underline-l { text-decoration: underline; }
 .no-underline-l { text-decoration: none; }
 .tl-l { text-align: left; }
 .tr-l { text-align: right; }
 .tc-l { text-align: center; }
 .ttc-l { text-transform: capitalize; }
 .ttl-l { text-transform: lowercase; }
 .ttu-l { text-transform: uppercase; }
 .ttn-l { text-transform: none; }
 .f-6-l, .f-headline-l { font-size: 6rem; }
 .f-5-l, .f-subheadline-l { font-size: 5rem; }
 .f1-l { font-size: 3rem; }
 .f2-l { font-size: 2.25rem; }
 .f3-l { font-size: 1.5rem; }
 .f4-l { font-size: 1.25rem; }
 .f5-l { font-size: 1rem; }
 .f6-l { font-size: .875rem; }
 .measure-l { max-width: 30em; }
 .measure-narrow-l { max-width: 20em; }
 .indent-l { text-indent: 1em; margin-top: 0; margin-bottom: 0; }
 .truncate-l { white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
 .clip-l { position: fixed !important; position: absolute !important; clip: rect( 1px 1px 1px 1px ); /* IE6, IE7 */ clip: rect( 1px, 1px, 1px, 1px ); }
 .ws-normal-l { white-space: normal; }
 .nowrap-l { white-space: nowrap; }
 .pre-l { white-space: pre; }
 .v-base-l { vertical-align: baseline; }
 .v-sub-l { vertical-align: sub; }
 .v-sup-l { vertical-align: super; }
 .v-txt-top-l { vertical-align: text-top; }
 .v-txt-btm-l { vertical-align: text-bottom; }
 .v-mid-l { vertical-align: middle; }
 .v-top-l { vertical-align: top; }
 .v-btm-l { vertical-align: bottom; }
}
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Authors

* [mrmrs](http://mrmrs.io)
* [johno](http://johnotander.com)

## License

MIT

