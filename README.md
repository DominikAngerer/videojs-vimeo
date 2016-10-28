# Vimeo Playback Technology<br />for [Video.js](https://github.com/videojs/video.js)

## Install
You can use bower (`bower install videojs-vimeo`), npm (`npm install videojs-vimeo`) or the source and build it using `npm run build`. Then, the only file you need is dist/Vimeo.min.js.

## Version Note
Use branch `vjs4` if you still using old VideoJS `v4.x`.

## Example
```html
<!DOCTYPE html>
<html>
<head>
  <link type="text/css" rel="stylesheet" href="../node_modules/video.js/dist/video-js.min.css" />
</head>
<body>
  <video
    id="vid1"
    class="video-js vjs-default-skin"
    controls
    autoplay
    width="640" height="264"
    data-setup='{ "techOrder": ["vimeo"], "sources": [{ "type": "video/vimeo", "src": "https://vimeo.com/153979733"}] }'
  >
  </video>

  <script src="../node_modules/video.js/dist/video.min.js"></script>
  <script src="../dist/Vimeo.min.js"></script>
</body>
</html>
```

See the examples folder for more

## How does it work?
Including the script Vimeo.min.js will add the Vimeo as a tech. You just have to add it to your techOrder option. Then, you add the option src with your Vimeo URL.

It supports:
- vimeo.com as well as youtu.be
- Regular URLs: https://vimeo.com/153979733

## Options
It supports every regular Video.js options. Additionally, you can change any [Vimeo parameter](https://developers.google.com/vimeo/player_parameters?hl=en#Parameters). Here is an example of setting the `iv_load_policy` parameter to `1`.

```html
<video
  id="vid1"
  class="video-js vjs-default-skin"
  controls
  autoplay
  width="640" height="264"
  data-setup='{ "techOrder": ["vimeo"], "sources": [{ "type": "video/vimeo", "src": "https://vimeo.com/153979733"}], "vimeo": { "iv_load_policy": 1 } }'
>
</video>
```

### Vimeo controls
Because `controls` is already a Video.js option, to use the Vimeo controls, you must set the `ytControls` parameter.

```html
<video
  id="vid1"
  class="video-js vjs-default-skin"
  controls
  autoplay
  width="640" height="264"
  data-setup='{ "techOrder": ["vimeo"], "sources": [{ "type": "video/vimeo", "src": "https://vimeo.com/153979733"}], "vimeo": { "ytControls": 2 } }'
>
</video>
```

##Special Thank You
Thanks to Steve Heffernan for the amazing Video.js and to John Hurliman for the original version of the Vimeo tech

## License
The MIT License (MIT)

Copyright (c) 2014-2015 Benoit Tremblay <trembl.ben@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
