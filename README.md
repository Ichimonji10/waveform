# waveform

![](http://i.imgur.com/oNy41Cr.png)

## Command Line Usage:

    waveform [options] audiofile pngfile

    Available options with their defaults:
    --width 256                 width of the image
    --height 64                 height of the image
    --color-bg 00000000         bg color, rrggbbaa
    --color-center 000000ff     gradient center color, rrggbbaa
    --color-outer 000000ff      gradient outer color, rrggbbaa
    --scan                      duration scan (default off)

    Substitute '-' for a filename to use stdio.

## Node.js Usage:

```js
var generateWaveform = require('waveform');
generateWaveform(audiofile, pngfile, {
    width: 256,                // width of the image
    height: 64,                // height of the image
    'color-bg': '00000000',    // bg color, rrggbbaa
    'color-center': '000000ff',// gradient center color, rrggbbaa
    'color-outer': '000000ff', // gradient outer color, rrggbbaa
    'scan': false,             // whether to do a pass to detect duration
}, function(err) {
    // done generating waveform
});
```

## Dependencies:

 * [libgroove](https://github.com/andrewrk/libgroove)
 * libpng
 * zlib

## Compile:

    make

## Related Projects

 * [PHP Wrapper Script](https://github.com/polem/WaveformGenerator)
 * [Native Interface for Go](https://github.com/dz0ny/podcaster/blob/master/utils/waveform.go)

