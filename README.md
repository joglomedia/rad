===================================================================
Rad: Responsive Ads jQuery Plugin (for Google Adsense)
Rad.js
===================================================================

BASIC INFO:
This plugin is meant to add responsive sizing to Google Ads.
It uses CSS3 transforms to scale the ad up/down to the proper size,
while resizing the ad's containing div as well.
This keeps a layout from breaking because of ads failing to resize.

This plugin works off the parent container of the ad div.
This means that it'll work better within divs where the children 
can comfortably expand 100% of the width.

It wraps the ad div in 1 container, `.radWrapper`, which is used 
to help retain a natural layout in the DOM.  You can style these 
individually for different layouts if need be.

QUICK DEMO:

https://primary-colored.5apps.com/


OPTIONS:
```
allowBiggerSizing   // accepts true or false, whether or not to 
                    // allow the ad to expand larger 
                    // than its original size (default false)
maxWidth    // accepts a number of pixels, will set a maximum 
            // width for the ad to display at
```

COMING SOON
```
WrapperOverrideCSS     //css to be applied after default css
WrapperAddClass         //class name to be added to default wrapper created

A throttle on the resizing...
```

EX USAGE:
```javascript
$(function(){
  $('#google-ad2').rad();
});
```
EX USAGE WITH OPTIONS:
```javascript
$(function(){
  $('#google-ad2').rad({
    allowBiggerSizing:"true", //default false
    maxWidth:"300" //default null, must be in number of pixels
  });
});
```
NOTE:
The Adsense iframes don't like plugins that wrap the body tag.
If your ads seem to be disappearing when used with rad.js, it may
be because of another plugin affecting the entire body.


===================================================================
