scss-super-layout
=================

Super simple but clever responsive layout for sass-based apps. Automatically enables:
- Sidebar
- Scalable content
- Stacked nav bar
- Sticky footer
- Full-size centering of hero units/modals

Layout is in `layout.scss` and some useful helpers you may want to use in your app are in `placeholders.scss`.

Only caveat is the layout breaks a bit on firefox and requires the following code for Firefox browsers:

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
