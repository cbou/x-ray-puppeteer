
# x-ray-puppeteer

  Chromium Puppeteer driver for [x-ray](https://github.com/lapwinglabs/x-ray).

## Why
XRay is great, but on ajax / JS-heavy pages, it needs to use a more complex driver. The best solution there is `x-ray-phantom` (which, incidentally, doesn't use `phantom` at all, but `nightmarejs`, but `nightmare` is limited in certain environments (plus, puppeteer is basically vanilla chromium, which is great). 

## Installation

This is a really simple function i whipped up ad hoc, so I haven't really set up for wider distribution yet.

For now you can either just clone this repo or copy the code in `index.js` into a file in your project


## Usage
Driver takes 4 args. See jsdoc in index.js for details. 


```javascript
// set some options for the Puppeteer instance
const puppeteerOptions = {
    headless: true,
    // In order to persist session info, you need to designate a userDataDir. 
    // Note that this folder can get large,
    // so consider adding it to .gitignore
    userDataDir: './USER_SESSION/'
};

var x = Xray({ filters }).driver(
    puppeteerDriver(
        puppeteerOptions,
        undefined, // <- see index.js for comments, but this basically is just an override for using Puppeteer in this driver. 
        {
        // some options to pass to .goto()
            timeout: 300000
        },
        '.some-selector-to-wait-for' // <- a selector that'll be passed to .waitFor() after .goto()
    )
);

```
