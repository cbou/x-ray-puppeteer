
# x-ray-puppeteer

  Chromium Puppeteer driver for [x-ray](https://github.com/lapwinglabs/x-ray).

## Why
XRay is great, but on ajax / JS-heavy pages, it needs to use a more complex driver. The best solution there is `x-ray-phantom` (which, incidentally, doesn't use `phantom` at all, but `nightmarejs`, but `nightmare` is limited in certain environments (plus, puppeteer is basically vanilla chromium, which is great). 

## Installation

This is a really simple function i whipped up ad hoc, so I haven't really set up for wider distribution yet.

For now you can either just clone this repo or copy the code in `index.js` into a file in your project

