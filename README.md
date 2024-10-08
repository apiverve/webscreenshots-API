Website Screenshot API
============

Web Screenshots is a simple tool for capturing screenshots of web pages. It returns an image screenshot of the web page provided.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a Javascript Wrapper for the [Website Screenshot API](https://apiverve.com/marketplace/api/webscreenshots)

---

## Installation
	npm install @apiverve/webscreenshots --save

---

## Configuration

Before using the webscreenshots API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The Website Screenshot API documentation is found here: [https://docs.apiverve.com/api/webscreenshots](https://docs.apiverve.com/api/webscreenshots).  
You can find parameters, example responses, and status codes documented here.

### Setup

```
var webscreenshotsAPI = require('@apiverve/webscreenshots');
var api = new webscreenshotsAPI({
    api_key: [YOUR_API_KEY],
    secure: true //(Optional, defaults to true)
});
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var query = {
  "url": "https://ebay.com/",
  "type": "png",
  "width": 1024,
  "height": 600,
  "fullpage": false
};
```

###### Simple Request (using Callback)

```
api.execute(query, function (error, data) {
    if (error) {
        return console.error(error);
    } else {
        console.log(data);
    }
});
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "width": 1024,
    "height": 600,
    "scaleFactor": 1,
    "imageName": "78bdb087-756b-4107-83e1-82fd40171ed1.png",
    "expires": 1725356395837,
    "url": "https://ebay.com/",
    "downloadURL": "https://storage.googleapis.com/apiverve-helpers.appspot.com/webscreenshots/78bdb087-756b-4107-83e1-82fd40171ed1.png?GoogleAccessId=1089020767582-compute%40developer.gserviceaccount.com&Expires=1725356395&Signature=jqAuoBhrbsSqs61blsFdnXEU35QOanhFnL0FN2d82cDDTXAUWonuRURUjyyhmABe02dVD3sMpvQDh0V39ROFcukPFASdIhr4HdWnKl743JLx03jrW%2FJ2baK3lZCZemPkS%2F61VqcHV1YB5XsxqsDNNkQ8QL8xlzUslHUgjuVKsorDCpBL5iFPSLo0l5DO3wvZ6UudJJP11j1MAnRmWQC7%2FkUBc7AP4akQvm6N7lftFkx8z6%2FptdxBt60w1XR6Ixoy6Vl31tvd6UjyWhjmF8JbujRSRYXmh0vjTNZBp5BX7xUntQUSMXhQf%2Bj3bXq7ZcsfMAAtqonqbzC6SBZgzSu2kA%3D%3D"
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2024 APIVerve, and Evlar LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.