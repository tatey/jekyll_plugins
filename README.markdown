# Collection of useful plugins for Jekyll

* **Sass:** Compile Sass into CSS.
* **LESS CSS:** Compile LESS CSS into CSS.
* **Growl:** Notifications before and after the build process.
* **JavaScript Minifier:** Compress JavaScript using the YUI compressor. 
* **Post Time:** Specify the time for a post in the YAML front matter, not just the date.

Plugins may be mixed and matched with other plugins. Plugins which depend on gems will tell you what to install.

## Installation

1. Create a `_plugins` directory.
1. Copy the plugins you want to include in your build.
1. Build!

If you're still not sure, take a look at [my repository](https://github.com/tatey/tatey.com).

## Sass, LESS CSS and JavaScript

Sass, LESS CSS and JavaScript are converters. You must specify an empty YAML front matter at the beginning of files you want to run through the converters.

### Example.sass

    ---
    ---

    #background
      color: black

## Migrating from Jekylless

All Jekylless users will be able to stay up to date with Jekyll while enjoying LESS CSS and Growl notifications. Jekylless users will need to copy the following plugins:

* LESS CSS
* Growl
* Post Time

The permalink tag is the only functionality which has not been implemented as a plugin. Users migrating from Jekylless will need to remove their permalink tags or wait for the permalink tag to become available as a plugin. 

## About

With the introduction of plugins, [wulfovitch](http://github.com/wulfovitch) and I realised we could convert most of the functionality from Jekylless into plugins. We'd no longer need to maintain a fork and everyone could mix and match. Unfortunately the Growl plugin would need to hook into Jekyll before and after the build process. We [submitted a patch](https://github.com/mojombo/jekyll/issues/issue/214), but it never gained any traction. Wanting to move forward, we've resorted to monkey patching a Generator to get Growl notifications happening. Enjoy!

## License

Copyright (c) 2010 Tate Johnson and Wolfgang König

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
