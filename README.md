scss-super-layout
=================

Super simple but clever responsive layout for sass-based apps

Only caveat is the layout breaks a bit on firefox and requires the following code for Firefox broswers:

```
var contentWrapper = $('.content_wrapper');

$(window).resize(function() {
  var windowHeight = $(window).height();
  contentWrapper.innerHeight(windowHeight);
});
```

You can use a custom Modernizr test to look for Firefox. For example:

```
Modernizr.addTest('firefox', function () {
 return !!navigator.userAgent.match(/firefox/i);
});
```

Then use `if (Modernizr.firefox) { // Hack here }` or something along those lines.
