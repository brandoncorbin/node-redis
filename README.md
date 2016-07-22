node-redis
==========

A redis client.

Usage
-----

    var redis = require('node-redis')

    var client = redis.createClient(port, host, auth)

    client.get('key', function (error, buffer) { ... })

    client.multi()
    client.lrange('key', 0, -1)
    client.lrange('key', [0, -1])
    client.exec(function (error, result) { result[0]; result[1] })

    client.subscribe('channel')
    client.on('message', function (buffer) { ... })
    client.on('message:channel', function (buffer) { ... })
    client.unsubscribe('channel')

    client.end()
