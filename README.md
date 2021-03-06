⛔️ DEPRECATED: libp2p-ping is now included in [js-libp2p](https://github.com/libp2p/js-libp2p)
=====

libp2p-ping JavaScript Implementation
=====================================

[![](https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat-square)](http://protocol.ai)
[![](https://img.shields.io/badge/project-libp2p-yellow.svg?style=flat-square)](http://libp2p.io/)
[![](https://img.shields.io/badge/freenode-%23libp2p-yellow.svg?style=flat-square)](http://webchat.freenode.net/?channels=%23libp2p)
[![Discourse posts](https://img.shields.io/discourse/https/discuss.libp2p.io/posts.svg)](https://discuss.libp2p.io)
[![Coverage Status](https://coveralls.io/repos/github/libp2p/js-libp2p-ping/badge.svg?branch=master)](https://coveralls.io/github/libp2p/js-libp2p-ping?branch=master)
[![Dependency Status](https://david-dm.org/libp2p/js-libp2p-ping.svg?style=flat-square)](https://david-dm.org/libp2p/js-libp2p-ping)
[![Travis CI](https://travis-ci.org/libp2p/js-libp2p-ping.svg?branch=master)](https://travis-ci.org/libp2p/js-libp2p-ping)
[![Circle CI](https://circleci.com/gh/libp2p/js-libp2p-ping.svg?style=svg)](https://circleci.com/gh/libp2p/js-libp2p-ping)

> IPFS ping protocol JavaScript implementation

## Lead Maintainer

[Jacob Heun](https://github.com/jacobheun/)

## Usage

```javascript
var Ping = require('libp2p-ping')

Ping.mount(swarm) // Enable this peer to echo Ping requests

var p = new Ping(swarm, peerDst) // Ping peerDst, peerDst must be a peer-info object

p.on('ping', function (time) {
  console.log(time + 'ms')
  p.stop() // stop sending pings
})

p.start()
```
