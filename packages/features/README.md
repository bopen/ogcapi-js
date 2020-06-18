# @ogcapi-js/features

A lightweight JavaScript client library for [OGCAPI - Features](https://github.com/opengeospatial/ogcapi-features).

This library works with endpoints defined at:
* [OGC API - Features - Part 1: Core](http://docs.opengeospatial.org/DRAFTS/17-069r2.html)

See more details at the [documentation](https://haoliangyu.github.io/ogcapi-js).

## Installation

```
npm install @ogcapi-js/features
```

## Usage

### Node.js

This library uses the global [fetch](https://fetch.spec.whatwg.org/) function for HTTP requests. Please consider using [isomorphic-fetch](https://www.npmjs.com/package/isomorphic-fetch) for polyfill.


``` javascript
require('isomorphic-fetch');

const { Service } = require('@ogcapi-js/features');

// create a new service client
const service = new Service({
  baseUrl: 'https://ogcapi.service.com'
});

// get all collections from the service
const collections = await services.getCollections();
```

### Browser

Modern browsers already support the global `fetch` function so there is no need to polyfill.

``` javascript
import { Service } from `@ogcapi-js/features`;

// create a new service client
const service = new Service({
  baseUrl: 'https://ogcapi.service.com'
});

// get all collections from the service
const collections = await services.getCollections();
```