# haproxy-stats
[![npm version](https://badge.fury.io/js/haproxy-stats.svg)](https://badge.fury.io/js/haproxy-stats)
[![Build Status](https://travis-ci.org/sohje/haproxy-stats.svg?branch=master)](https://travis-ci.org/sohje/haproxy-stats)

Get HAProxy statistics in JSON format via HTTP request.  
Check [docs](http://www.haproxy.org/#docs) for more info.


## Install

```
$ npm install --save haproxy-stats
```


### Usage

```js
var haStats = require('haproxy-stats');
haStats('http://localhost:1337/stats;csv;norefresh', function(err, data) {
    console.log(data)
    // => { 'ws': {'ws1': {qcur: 12, qmax: 0, scur: 355 ...}, 'ws2': {qcur: 0, qmax: 0, scur: 301 ...} } }
})
```

## License

MIT © [Nikolay Spiridonov](https://github.com/sohje)
