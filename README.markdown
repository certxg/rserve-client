# rserve-client

A stateful client for Rserve, the TCP/IP server for R framework.

*NOTICE: there is a higher quality client [rserve-js](https://www.npmjs.org/package/rserve) ([github](https://github.com/cscheid/rserve-js))- and it is useful not only for websockets*

- [Overview](#overview)
- [Installation](#installation)
- [API](#api)
- [Development](#development)

## Overview

    TODO

## Installation

  Install with [npm](https://www.npmjs.org/package/rserve-client):

    $ npm install --save rserve-client

## API

    var r = require('rserve-client');
    r.connect('localhost', 6311, function(err, client) {
        client.evaluate('a<-2.7+2', function(err, ans) {
            console.log(ans);
            client.end();
        });
    });

See example directory.

### .connect(hostname, port, callback)

Connects to Rserve at hostname on port and returns the connection via callback.

### connection.evaluate(command, callback)

Evaluates the given command on Rserve and returns the result via callback.

### connection.end()

Ends the connection by closing the socket.

## Development

    TODO
