> Include and combine SVG files into your HTML to reference them as SVG templates


## Getting Started

If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide, as it explains how to create a [gruntfile][Getting Started] as well as install and use grunt plugins. Once you're familiar with that process, install this plugin with this command:

```shell
npm install --save-dev grunt-svgtemplater
```

[grunt]: http://gruntjs.com
[Getting Started]: https://github.com/gruntjs/grunt/blob/devel/docs/getting_started.md


## Overview

This task looks through your projects image directory for SVG files, extracts their content, wraps it into individual SVG groups with `id="svg-[filename]"` and writes these new groups into your HTML file so you can reference them as templates throughout your site like this:

```html
<svg viewBox="0 0 1024 1024">
  <use xlink:href="#svg-[filename]">
</svg>
```

Chris Coyier explains this mechanism nicely on his blog [CSS-Tricks](http://css-tricks.com/svg-tabs-using-svg-shape-template/)


### Example Task

```js
grunt.initConfig({
    mytask: {
      src: 'img/**/*.{svg}',
      dest: 'index.html'
    }
  }
});
```

## License

[Apache2](http://www.apache.org/licenses/LICENSE-2.0.html)
