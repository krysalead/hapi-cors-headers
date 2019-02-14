# hapi-cors-headers

> hapi extension to enable CORS

[![Build Status](https://travis-ci.org/gr2m/hapi-cors-headers.svg?branch=master)](https://travis-ci.org/gr2m/hapi-cors-headers)
[![Coverage Status](https://coveralls.io/repos/gr2m/hapi-cors-headers/badge.svg?branch=master)](https://coveralls.io/r/gr2m/hapi-cors-headers?branch=master)
[![Greenkeeper badge](https://badges.greenkeeper.io/gr2m/hapi-cors-headers.svg)](https://greenkeeper.io/)

Enables [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS) on
all server response, securely from all origins, with `access-control-allow-credentials: true`.

## Example

```js
var Hapi = require('hapi');
const corsHeaders = require('hapi-cors-headers')('localhost:8888', logger);

var server = new Hapi.Server();
// setup routes etc ...

server.ext('onPreResponse', corsHeaders);
```

logger is option if not specified it will be console. The first arguments tells to cors-header to allow only on localhost:8888

## Install

```bash
npm install --save hapi-cors-headers
```

## Test

[![devDependency Status](https://david-dm.org/gr2m/hapi-cors-headers/dev-status.svg)](https://david-dm.org/gr2m/hapi-cors-headers#info=devDependencies)

```bash
npm test
```

## License

[MIT](LICENSE.md)
