# Thermoscope

A web browser with no external navigation using a Web Bluetooth implementation to connect to Thermoscope devices.

Based on [WebBLE](https://www.greenparksoftware.co.uk/projects/webble/1.1.4) by Green Park Software

[Thermoscope](https://github.com/concord-consortium/thermoscope-bluefruit) devices use an Adafruit Bluefruit MO board connected to two thermistors.


## Building for iOS

A local folder needs to exist with the Thermoscope directory called "dist" and contain the current version of the Thermoscope application files. 

Explicit paths must be used in all hrefs in the Thermoscope html code including the html page name to prevent errors, for example:
```<a href="./thermoscope/index.html">```
  
Note that the `ios-offline` branch of [Thermoscope](https://github.com/concord-consortium/thermoscope) was designed to download and cache all resources - if the `dist` folder comes from that branch, then any offline cache files or references (look for `offline.appcache` file or `<html manifest="../offline.appcache">` should be removed, along with `applicationCache` event listeners in the main `index.html`. 

Remove any references to `rollbar.js` from any html files since this is unnecessary for local operation.
