# http-gzip-maybe [![stability][0]][1]
[![npm version][2]][3] [![build status][4]][5]
[![downloads][8]][9] [![js-standard-style][10]][11]

Compress an HTTP response if the client has headers that allow it

## Usage
```js
var gzipMaybe = require('http-gzip-maybe')
var http = require('http')
var pump = require('pump')

http.createServer(function (req, res) {
  var gzip = gzipMaybe(req, res)
  pump(req, gzip, res)
}).listen(8080)
```

## API
### `stream = gzipMaybe(req, res)`
Create a transform stream that conditionally compresses the outgoing data.

## License
[MIT](https://tldrlegal.com/license/mit-license)

[0]: https://img.shields.io/badge/stability-experimental-orange.svg?style=flat-square
[1]: https://nodejs.org/api/documentation.html#documentation_stability_index
[2]: https://img.shields.io/npm/v/http-gzip-maybe.svg?style=flat-square
[3]: https://npmjs.org/package/http-gzip-maybe
[4]: https://img.shields.io/travis/yoshuawuyts/http-gzip-maybe/master.svg?style=flat-square
[5]: https://travis-ci.org/yoshuawuyts/http-gzip-maybe
[6]: https://img.shields.io/codecov/c/github/yoshuawuyts/http-gzip-maybe/master.svg?style=flat-square
[7]: https://codecov.io/github/yoshuawuyts/http-gzip-maybe
[8]: http://img.shields.io/npm/dm/http-gzip-maybe.svg?style=flat-square
[9]: https://npmjs.org/package/http-gzip-maybe
[10]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[11]: https://github.com/feross/standard
