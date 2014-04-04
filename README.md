prerender-parse
===============

A parse.com adaptor for utilizing the [prerender.io](https://prerender.io) service.

Installation
============

To get it running, go through the [Parse Docs](https://parse.com/docs/hosting_guide#started) through [Dynamic Websites](https://parse.com/docs/hosting_guide#webapp)

Download both prerenderio.js and prerender-parse.js and include within your /cloud/ directory.

Inject the prerender middleware into your express server similar to:

````javascript
var express = require('express');
var app = express();

var parseAdaptor = require('cloud/prerender-parse.js');

app.use(require('cloud/prerenderio.js').setAdaptor(parseAdaptor(Parse)).set('prerenderToken','YOUR_TOKEN'));

````

You'll get your prerender token from the prerender.io site.
