# imageCache: a jQuery plugin

imageCache is a simple jQuery plugin for pre-caching images.  The
plugin can be used to eliminate flashes of unstyled content (FOUC) and
improve perceived page load time.  Callbacks for load, error and abort
events are provided.

See full documentation at <a href="http://alexrabarts.github.com/jquery-cacheimage/">http://alexrabarts.github.com/jquery-cacheimage/</a>.

## Usage

Cache an image:

<pre>
  $.cacheImage('/path/to/image.png');
  // or if you have images hidden in the DOM:
  $('#myImage').cacheImage();
</pre>

Cache several images:

<pre>
  $.cacheImage(['/path/to/an/image.png', '/path/to/another/image.png'])
  // or if you have images hidden in the DOM:
  $('#myImages img').cacheImage();
</pre>

Add some callbacks:

<pre>
  $.cacheImage('/path/to/image.png', {
    load : function (e) { console.log('Loaded',  this, e); },
    error: function (e) { console.log('Error',   this, e); },
    abort: function (e) { console.log('Aborted', this, e); }
  });
</pre>

# Licensing

Licensed under the MIT:
http://www.opensource.org/licenses/mit-license.php

Copyright (c) 2008 Stateless Systems (http://statelesssystems.com)
