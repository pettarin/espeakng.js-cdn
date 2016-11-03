# espeakng.js-cdn

This repository contains the latest compiled and minified version of
[espeakng.js](https://github.com/espeak-ng/espeak-ng/tree/master/emscripten),
the Javascript port of 
[eSpeak-ng](https://github.com/espeak-ng/espeak-ng)
via
[emscripten](http://emscripten.org).

[espeakng.js](https://github.com/espeak-ng/espeak-ng/tree/master/emscripten)
allows client-side text-to-speech synthesis in any browser
supporting Web workers and the Web Audio API.

* Version: 1.49.0
* Date: 2016-11-03
* License: the GNU General Public License, Version 3 (GPLv3)
* Size: 3.0 MB (including all the voices)

## Download

The following compiled and minified files:

* `js/espeakng.js`
* `js/espeakng.min.js` (see `Notes` below)
* `js/espeakng.min.js.map` (see `Notes` below)
* `js/espeakng.worker.js`
* `js/espeakng.worker.data`

are available through the [jsdelivr CDN](http://www.jsdelivr.com/).

To use `espeakng.js` in your project, you will need to get (at least):

```
# Get latest version
https://cdn.jsdelivr.net/espeakng.js/latest/espeakng.min.js
https://cdn.jsdelivr.net/espeakng.js/latest/espeakng.worker.js
https://cdn.jsdelivr.net/espeakng.js/latest/espeakng.worker.data

# Get specific version
https://cdn.jsdelivr.net/espeakng.js/1.49.0/espeakng.min.js
https://cdn.jsdelivr.net/espeakng.js/1.49.0/espeakng.worker.js
https://cdn.jsdelivr.net/espeakng.js/1.49.0/espeakng.worker.data
```

## Upload A New Version

Since auto-updating is enabled,
to make a new version available on jsdeliver,
just do (in this repository) the following:

1. copy the new JS/data files from the [eSpeak-ng](https://github.com/espeak-ng/espeak-ng/tree/master/emscripten) project in the `js/` directory;
2. create a new [release](https://github.com/pettarin/espeakng.js-cdn/releases), following semver.

The configuration settings for jsdeliver are
[here](https://github.com/jsdelivr/jsdelivr/tree/master/files/espeakng.js).

## Demo Files

The files:

* `demo.html`
* `demo.min.html`
* `js/demo.js`

are not uploaded to jsdeliver.
They are present in this repository
for testing/debugging purposes only.

## Notes

Currently `js/espeakng.min.js` is a copy of `js/espeakng.js`,
and `js/espeakng.min.js.map` is empty,
but they are included to make things
easier for jsdelivr in the future.

(I was unable to minify `js/espeakng.js` with `UglifyJS 2`
since it complained about the use of the `of` operator,
it looks like an issue with ECMAScript-something support.)
