# Website Screenshot API

Web Screenshots is a simple tool for capturing screenshots of web pages. It returns an image screenshot of the web page provided.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)
[![npm version](https://img.shields.io/npm/v/@apiverve/webscreenshots.svg)](https://www.npmjs.com/package/@apiverve/webscreenshots)

This is a Javascript Wrapper for the [Website Screenshot API](https://webscreenshots.apiverve.com?utm_source=npm&utm_medium=readme)

---

## Installation

Using npm:
```shell
npm install @apiverve/webscreenshots
```

Using yarn:
```shell
yarn add @apiverve/webscreenshots
```

---

## Configuration

Before using the Website Screenshot API client, you have to setup your account and obtain your API Key.
You can get it by signing up at [https://apiverve.com](https://apiverve.com?utm_source=npm&utm_medium=readme)

---

## Quick Start

[Get started with the Quick Start Guide](https://docs.apiverve.com/quickstart?utm_source=npm&utm_medium=readme)

The Website Screenshot API documentation is found here: [https://docs.apiverve.com/ref/webscreenshots](https://docs.apiverve.com/ref/webscreenshots?utm_source=npm&utm_medium=readme).
You can find parameters, example responses, and status codes documented here.

### Setup

```javascript
const webscreenshotsAPI = require('@apiverve/webscreenshots');
const api = new webscreenshotsAPI({
    api_key: '[YOUR_API_KEY]'
});
```

---

## Usage

---

### Perform Request

Using the API is simple. All you have to do is make a request. The API will return a response with the data you requested.

```javascript
var query = {
  "url": "https://ebay.com/",
  "type": "png",
  "width": 1024,
  "height": 600,
  "fullpage": false
};

api.execute(query, function (error, data) {
    if (error) {
        return console.error(error);
    } else {
        console.log(data);
    }
});
```

---

### Using Promises

You can also use promises to make requests. The API returns a promise that you can use to handle the response.

```javascript
var query = {
  "url": "https://ebay.com/",
  "type": "png",
  "width": 1024,
  "height": 600,
  "fullpage": false
};

api.execute(query)
    .then(data => {
        console.log(data);
    })
    .catch(error => {
        console.error(error);
    });
```

---

### Using Async/Await

You can also use async/await to make requests. The API returns a promise that you can use to handle the response.

```javascript
async function makeRequest() {
    var query = {
  "url": "https://ebay.com/",
  "type": "png",
  "width": 1024,
  "height": 600,
  "fullpage": false
};

    try {
        const data = await api.execute(query);
        console.log(data);
    } catch (error) {
        console.error(error);
    }
}
```

---

## Example Response

```json
{
  "status": "ok",
  "error": null,
  "data": {
    "width": 1024,
    "height": 600,
    "scaleFactor": 1,
    "imageName": "77072426-6af8-45c2-93dd-d7013d2c765e.png",
    "expires": 1766097105719,
    "url": "https://ebay.com/",
    "downloadURL": "https://storage.googleapis.com/apiverve-helpers.appspot.com/webscreenshots/77072426-6af8-45c2-93dd-d7013d2c765e.png?GoogleAccessId=1089020767582-compute%40developer.gserviceaccount.com&Expires=1766097105&Signature=uZKa777XpeVnlwOZG7Uhjs%2BNkPzkEuiV4Wug2%2B%2BAHcPovRZ3iVjZEX%2FZhp7gnADXI6au5q0ggPwweoOFJeMCdk9zod6aZo4hlUDe1DsJf0oao4rh3tGUl5wPeudXLp7Y%2F3zVflup9Mp255LY6%2B2JdU0auOHdPnEYLDCvf705X9C%2BflmWQZKh7QKi74gvU8pqsP6Zc7SfJJsv5kmhP8SkO7TBZKBU6pAr2mNHKpKgB5mtfCRLbyPYcxawSGlTuyIyRXffWbkfHdDl6pquPX9J%2Fp5uGYM4jTrqrrrR1MPAOfkD7d9V5juqe5A7VvWmhiAyCMGDO%2BeqUO%2BSe6t9php0vA%3D%3D"
  }
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact?utm_source=npm&utm_medium=readme).

---

## Updates

Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms?utm_source=npm&utm_medium=readme), [Privacy Policy](https://apiverve.com/privacy?utm_source=npm&utm_medium=readme), and [Refund Policy](https://apiverve.com/refund?utm_source=npm&utm_medium=readme).

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2026 APIVerve, and EvlarSoft LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
