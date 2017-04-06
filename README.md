# api documentation for  [coap (v0.21.0)](https://github.com/mcollina/node-coap#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-coap.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-coap) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-coap.svg)](https://travis-ci.org/npmdoc/node-npmdoc-coap)
#### A CoAP library for node modelled after 'http'

[![NPM](https://nodei.co/npm/coap.png?downloads=true)](https://www.npmjs.com/package/coap)

[![apidoc](https://npmdoc.github.io/node-npmdoc-coap/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-coap_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-coap/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-coap/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-coap/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matteo Collina",
        "email": "hello@matteocollina.com"
    },
    "bugs": {
        "url": "https://github.com/mcollina/node-coap/issues"
    },
    "dependencies": {
        "bl": "^1.0.0",
        "capitalize": "^1.0.0",
        "coap-packet": "^0.1.12",
        "debug": "^2.2.0",
        "fastseries": "^1.7.0",
        "lru-cache": "^4.0.0",
        "readable-stream": "^2.2.2"
    },
    "description": "A CoAP library for node modelled after 'http'",
    "devDependencies": {
        "chai": "^3.4.1",
        "mocha": "^3.2.0",
        "pre-commit": "1.1.3",
        "sinon": "~1.7.3",
        "timekeeper": "^1.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "ce96f3a80628b2ab543a4a9a64a10679be38261b",
        "tarball": "https://registry.npmjs.org/coap/-/coap-0.21.0.tgz"
    },
    "gitHead": "29f20af1b493e5d296d4d8cf1e6ff406cbd01278",
    "homepage": "https://github.com/mcollina/node-coap#readme",
    "keywords": [
        "coap",
        "m2m",
        "iot",
        "client",
        "server",
        "udp",
        "observe",
        "internet of things",
        "messaging"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "boneskull",
            "email": "boneskull@boneskull.com"
        },
        {
            "name": "giedrius",
            "email": "giedrius@8devices.com"
        },
        {
            "name": "matteo.collina",
            "email": "hello@matteocollina.com"
        }
    ],
    "name": "coap",
    "optionalDependencies": {},
    "pre-commit": [
        "test"
    ],
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/mcollina/node-coap.git"
    },
    "scripts": {
        "test": "mocha --bail --reporter spec 2>&1",
        "testnobail": "mocha --reporter spec 2>&1"
    },
    "version": "0.21.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module coap](#apidoc.module.coap)
1.  [function <span class="apidocSignatureSpan">coap.</span>Agent (opts)](#apidoc.element.coap.Agent)
1.  [function <span class="apidocSignatureSpan">coap.</span>createServer (options, listener)](#apidoc.element.coap.createServer)
1.  [function <span class="apidocSignatureSpan">coap.</span>defaultTiming ()](#apidoc.element.coap.defaultTiming)
1.  [function <span class="apidocSignatureSpan">coap.</span>ignoreOption (name)](#apidoc.element.coap.ignoreOption)
1.  [function <span class="apidocSignatureSpan">coap.</span>incoming_message (packet, rsinfo, outSocket)](#apidoc.element.coap.incoming_message)
1.  [function <span class="apidocSignatureSpan">coap.</span>observe_read_stream (packet, rsinfo, outSocket)](#apidoc.element.coap.observe_read_stream)
1.  [function <span class="apidocSignatureSpan">coap.</span>observe_write_stream (request, send)](#apidoc.element.coap.observe_write_stream)
1.  [function <span class="apidocSignatureSpan">coap.</span>outgoing_message (request, send)](#apidoc.element.coap.outgoing_message)
1.  [function <span class="apidocSignatureSpan">coap.</span>registerFormat (name, value)](#apidoc.element.coap.registerFormat)
1.  [function <span class="apidocSignatureSpan">coap.</span>registerOption (name, toBinary, fromBinary)](#apidoc.element.coap.registerOption)
1.  [function <span class="apidocSignatureSpan">coap.</span>request (url)](#apidoc.element.coap.request)
1.  [function <span class="apidocSignatureSpan">coap.</span>retry_send (sock, port, host)](#apidoc.element.coap.retry_send)
1.  [function <span class="apidocSignatureSpan">coap.</span>updateTiming (values)](#apidoc.element.coap.updateTiming)
1.  object <span class="apidocSignatureSpan">coap.</span>Agent.prototype
1.  object <span class="apidocSignatureSpan">coap.</span>createServer.prototype
1.  object <span class="apidocSignatureSpan">coap.</span>globalAgent
1.  object <span class="apidocSignatureSpan">coap.</span>globalAgentIPv6
1.  object <span class="apidocSignatureSpan">coap.</span>helpers
1.  object <span class="apidocSignatureSpan">coap.</span>incoming_message.prototype
1.  object <span class="apidocSignatureSpan">coap.</span>middlewares
1.  object <span class="apidocSignatureSpan">coap.</span>observe_read_stream.prototype
1.  object <span class="apidocSignatureSpan">coap.</span>observe_write_stream.prototype
1.  object <span class="apidocSignatureSpan">coap.</span>option_converter
1.  object <span class="apidocSignatureSpan">coap.</span>outgoing_message.prototype
1.  object <span class="apidocSignatureSpan">coap.</span>parameters
1.  object <span class="apidocSignatureSpan">coap.</span>polyfill
1.  object <span class="apidocSignatureSpan">coap.</span>retry_send.prototype

#### [module coap.Agent](#apidoc.module.coap.Agent)
1.  [function <span class="apidocSignatureSpan">coap.</span>Agent (opts)](#apidoc.element.coap.Agent.Agent)
1.  [function <span class="apidocSignatureSpan">coap.Agent.</span>super_ ()](#apidoc.element.coap.Agent.super_)

#### [module coap.Agent.prototype](#apidoc.module.coap.Agent.prototype)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_cleanUp ()](#apidoc.element.coap.Agent.prototype._cleanUp)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_doClose ()](#apidoc.element.coap.Agent.prototype._doClose)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_handle (msg, rsinfo, outSocket)](#apidoc.element.coap.Agent.prototype._handle)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_init (socket)](#apidoc.element.coap.Agent.prototype._init)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_nextMessageId ()](#apidoc.element.coap.Agent.prototype._nextMessageId)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_nextToken ()](#apidoc.element.coap.Agent.prototype._nextToken)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>abort (req)](#apidoc.element.coap.Agent.prototype.abort)
1.  [function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>request (url)](#apidoc.element.coap.Agent.prototype.request)

#### [module coap.createServer](#apidoc.module.coap.createServer)
1.  [function <span class="apidocSignatureSpan">coap.</span>createServer (options, listener)](#apidoc.element.coap.createServer.createServer)
1.  [function <span class="apidocSignatureSpan">coap.createServer.</span>super_ ()](#apidoc.element.coap.createServer.super_)

#### [module coap.createServer.prototype](#apidoc.module.coap.createServer.prototype)
1.  [function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_handle (packet, rsinfo)](#apidoc.element.coap.createServer.prototype._handle)
1.  [function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_sendError (payload, rsinfo, packet)](#apidoc.element.coap.createServer.prototype._sendError)
1.  [function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_sendProxied (packet, proxyUri, callback)](#apidoc.element.coap.createServer.prototype._sendProxied)
1.  [function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_sendReverseProxied (packet, rsinfo, callback)](#apidoc.element.coap.createServer.prototype._sendReverseProxied)
1.  [function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>close (done)](#apidoc.element.coap.createServer.prototype.close)
1.  [function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>listen (port, address, done)](#apidoc.element.coap.createServer.prototype.listen)

#### [module coap.helpers](#apidoc.module.coap.helpers)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>addSetOption (klass)](#apidoc.element.coap.helpers.addSetOption)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>createBlock2 (requestedBlock)](#apidoc.element.coap.helpers.createBlock2)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>genAck (request)](#apidoc.element.coap.helpers.genAck)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>getOption (options, name)](#apidoc.element.coap.helpers.getOption)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>isBoolean (n)](#apidoc.element.coap.helpers.isBoolean)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>isNumeric (n)](#apidoc.element.coap.helpers.isNumeric)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>isOption (optionName)](#apidoc.element.coap.helpers.isOption)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>or (previous, current)](#apidoc.element.coap.helpers.or)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>packetToMessage (dest, packet)](#apidoc.element.coap.helpers.packetToMessage)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>parseBlock2 (block2Value)](#apidoc.element.coap.helpers.parseBlock2)
1.  [function <span class="apidocSignatureSpan">coap.helpers.</span>toCode (code)](#apidoc.element.coap.helpers.toCode)

#### [module coap.incoming_message](#apidoc.module.coap.incoming_message)
1.  [function <span class="apidocSignatureSpan">coap.</span>incoming_message (packet, rsinfo, outSocket)](#apidoc.element.coap.incoming_message.incoming_message)
1.  [function <span class="apidocSignatureSpan">coap.incoming_message.</span>super_ (options)](#apidoc.element.coap.incoming_message.super_)

#### [module coap.incoming_message.prototype](#apidoc.module.coap.incoming_message.prototype)
1.  [function <span class="apidocSignatureSpan">coap.incoming_message.prototype.</span>_read (size)](#apidoc.element.coap.incoming_message.prototype._read)

#### [module coap.middlewares](#apidoc.module.coap.middlewares)
1.  [function <span class="apidocSignatureSpan">coap.middlewares.</span>handleProxyResponse (request, next)](#apidoc.element.coap.middlewares.handleProxyResponse)
1.  [function <span class="apidocSignatureSpan">coap.middlewares.</span>handleServerRequest (request, next)](#apidoc.element.coap.middlewares.handleServerRequest)
1.  [function <span class="apidocSignatureSpan">coap.middlewares.</span>parseRequest (request, next)](#apidoc.element.coap.middlewares.parseRequest)
1.  [function <span class="apidocSignatureSpan">coap.middlewares.</span>proxyRequest (request, next)](#apidoc.element.coap.middlewares.proxyRequest)

#### [module coap.observe_read_stream](#apidoc.module.coap.observe_read_stream)
1.  [function <span class="apidocSignatureSpan">coap.</span>observe_read_stream (packet, rsinfo, outSocket)](#apidoc.element.coap.observe_read_stream.observe_read_stream)
1.  [function <span class="apidocSignatureSpan">coap.observe_read_stream.</span>super_ (options)](#apidoc.element.coap.observe_read_stream.super_)

#### [module coap.observe_read_stream.prototype](#apidoc.module.coap.observe_read_stream.prototype)
1.  [function <span class="apidocSignatureSpan">coap.observe_read_stream.prototype.</span>_read ()](#apidoc.element.coap.observe_read_stream.prototype._read)
1.  [function <span class="apidocSignatureSpan">coap.observe_read_stream.prototype.</span>append (packet)](#apidoc.element.coap.observe_read_stream.prototype.append)
1.  [function <span class="apidocSignatureSpan">coap.observe_read_stream.prototype.</span>close ()](#apidoc.element.coap.observe_read_stream.prototype.close)

#### [module coap.observe_write_stream](#apidoc.module.coap.observe_write_stream)
1.  [function <span class="apidocSignatureSpan">coap.</span>observe_write_stream (request, send)](#apidoc.element.coap.observe_write_stream.observe_write_stream)
1.  [function <span class="apidocSignatureSpan">coap.observe_write_stream.</span>super_ (options)](#apidoc.element.coap.observe_write_stream.super_)

#### [module coap.observe_write_stream.prototype](#apidoc.module.coap.observe_write_stream.prototype)
1.  [function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>_doSend (data)](#apidoc.element.coap.observe_write_stream.prototype._doSend)
1.  [function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>_write (data, encoding, done)](#apidoc.element.coap.observe_write_stream.prototype._write)
1.  [function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>reset ()](#apidoc.element.coap.observe_write_stream.prototype.reset)
1.  [function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>setHeader (name, values)](#apidoc.element.coap.observe_write_stream.prototype.setHeader)
1.  [function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>setOption (name, values)](#apidoc.element.coap.observe_write_stream.prototype.setOption)

#### [module coap.option_converter](#apidoc.module.coap.option_converter)
1.  [function <span class="apidocSignatureSpan">coap.option_converter.</span>fromBinary (name, value)](#apidoc.element.coap.option_converter.fromBinary)
1.  [function <span class="apidocSignatureSpan">coap.option_converter.</span>ignoreOption (name)](#apidoc.element.coap.option_converter.ignoreOption)
1.  [function <span class="apidocSignatureSpan">coap.option_converter.</span>isIgnored (name)](#apidoc.element.coap.option_converter.isIgnored)
1.  [function <span class="apidocSignatureSpan">coap.option_converter.</span>registerFormat (name, value)](#apidoc.element.coap.option_converter.registerFormat)
1.  [function <span class="apidocSignatureSpan">coap.option_converter.</span>registerOption (name, toBinary, fromBinary)](#apidoc.element.coap.option_converter.registerOption)
1.  [function <span class="apidocSignatureSpan">coap.option_converter.</span>toBinary (name, value)](#apidoc.element.coap.option_converter.toBinary)

#### [module coap.outgoing_message](#apidoc.module.coap.outgoing_message)
1.  [function <span class="apidocSignatureSpan">coap.</span>outgoing_message (request, send)](#apidoc.element.coap.outgoing_message.outgoing_message)
1.  [function <span class="apidocSignatureSpan">coap.outgoing_message.</span>super_ (callback)](#apidoc.element.coap.outgoing_message.super_)

#### [module coap.outgoing_message.prototype](#apidoc.module.coap.outgoing_message.prototype)
1.  [function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>end (a, b)](#apidoc.element.coap.outgoing_message.prototype.end)
1.  [function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>reset ()](#apidoc.element.coap.outgoing_message.prototype.reset)
1.  [function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>setHeader (name, values)](#apidoc.element.coap.outgoing_message.prototype.setHeader)
1.  [function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>setOption (name, values)](#apidoc.element.coap.outgoing_message.prototype.setOption)
1.  [function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>writeHead (code, headers)](#apidoc.element.coap.outgoing_message.prototype.writeHead)

#### [module coap.parameters](#apidoc.module.coap.parameters)
1.  boolean <span class="apidocSignatureSpan">coap.parameters.</span>sendAcksForNonConfirmablePackets
1.  [function <span class="apidocSignatureSpan">coap.parameters.</span>defaultTiming ()](#apidoc.element.coap.parameters.defaultTiming)
1.  [function <span class="apidocSignatureSpan">coap.parameters.</span>refreshTiming (values)](#apidoc.element.coap.parameters.refreshTiming)
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>ackRandomFactor
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>ackTimeout
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>coapPort
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>exchangeLifetime
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>maxLatency
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>maxPacketSize
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>maxRTT
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>maxRetransmit
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>maxTransmitSpan
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>maxTransmitWait
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>piggybackReplyMs
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>processingDelay
1.  number <span class="apidocSignatureSpan">coap.parameters.</span>pruneTimerPeriod

#### [module coap.polyfill](#apidoc.module.coap.polyfill)
1.  [function <span class="apidocSignatureSpan">coap.polyfill.</span>compareBuffers (buf1, buf2)](#apidoc.element.coap.polyfill.compareBuffers)

#### [module coap.retry_send](#apidoc.module.coap.retry_send)
1.  [function <span class="apidocSignatureSpan">coap.</span>retry_send (sock, port, host)](#apidoc.element.coap.retry_send.retry_send)
1.  [function <span class="apidocSignatureSpan">coap.retry_send.</span>super_ ()](#apidoc.element.coap.retry_send.super_)

#### [module coap.retry_send.prototype](#apidoc.module.coap.retry_send.prototype)
1.  [function <span class="apidocSignatureSpan">coap.retry_send.prototype.</span>_send (avoidBackoff)](#apidoc.element.coap.retry_send.prototype._send)
1.  [function <span class="apidocSignatureSpan">coap.retry_send.prototype.</span>reset ()](#apidoc.element.coap.retry_send.prototype.reset)
1.  [function <span class="apidocSignatureSpan">coap.retry_send.prototype.</span>send (message, avoidBackoff)](#apidoc.element.coap.retry_send.prototype.send)



# <a name="apidoc.module.coap"></a>[module coap](#apidoc.module.coap)

#### <a name="apidoc.element.coap.Agent"></a>[function <span class="apidocSignatureSpan">coap.</span>Agent (opts)](#apidoc.element.coap.Agent)
- description and source-code
```javascript
function Agent(opts) {
  if (!(this instanceof Agent))
    return new Agent()

  if (!opts)
    opts = {}

  if (!opts.type)
    opts.type = 'udp4'

  if (opts.socket) {
    delete opts.port
  }

  this._opts = opts

  this._init(opts.socket)
}
```
- example usage
```shell
...
registerFormat('application/octet-stream', 42)
registerFormat('application/exi', 47)
registerFormat('application/json', 50)
'''

-------------------------------------------------------
<a name="agent"></a>
### coap.Agent([opts])

An Agent encapsulate an UDP Socket. It uses a combination of 'messageId'
and 'token' to distinguish between the different exchanges.
The socket will auto-close itself when no more exchange are in place.

By default, no UDP socket are open, and it is opened on demand to send
the messages.
...
```

#### <a name="apidoc.element.coap.createServer"></a>[function <span class="apidocSignatureSpan">coap.</span>createServer (options, listener)](#apidoc.element.coap.createServer)
- description and source-code
```javascript
function CoAPServer(options, listener) {
  if (!(this instanceof CoAPServer)) {
    return new CoAPServer(options, listener)
  }

  if (typeof options === 'function') {
    listener = options
    options = null
  }

  if (!options)
    options = {}

  this._options = options
  this._proxiedRequests = {}

  this._middlewares = [
    middlewares.parseRequest
  ]

  if (options.proxy) {
    this._middlewares.push(middlewares.proxyRequest)
    this._middlewares.push(middlewares.handleProxyResponse)
  }

  if (!this._options.piggybackReplyMs || !isNumeric(this._options.piggybackReplyMs)) {
    this._options.piggybackReplyMs = parameters.piggybackReplyMs
  }

  if (!isBoolean(this._options.sendAcksForNonConfirmablePackets)) {
    this._options.sendAcksForNonConfirmablePackets = parameters.sendAcksForNonConfirmablePackets
  }
  this._middlewares.push(middlewares.handleServerRequest)

  // Multicast settings
  this._multicastAddress = options.multicastAddress ? options.multicastAddress : null
  this._multicastInterface = options.multicastInterface ? options.multicastInterface : null

  // We use an LRU cache for the responses to avoid
  // DDOS problems.
  // max packet size is 1280
  // 32 MB / 1280 = 26214
  // The max lifetime is roughly 200s per packet.
  // Which gave us 131 packets/second guarantee
  this._lru = LRU({
      max: options.cacheSize || (32768 * 1024)
    , length: function(n) { return n.buffer.byteLength }
    , maxAge: (parameters.exchangeLifetime * 1000)
    , dispose:  function(key, value) {
                  if (value.sender)
                    value.sender.reset()
                }
  })

  this._series = series()
  this._block2Cache = {}

  if (listener)
    this.on('request', listener)
  debug('initialized');
}
```
- example usage
```shell
...
## Basic Example

The following example opens a UDP server and sends a
CoAP message to it:

'''js
var coap        = require('coap')
  , server      = coap.createServer()

server.on('request', function(req, res) {
  res.end('Hello ' + req.url.split('/')[1] + '\n')
})

// the default CoAP port is 5683
server.listen(function() {
...
```

#### <a name="apidoc.element.coap.defaultTiming"></a>[function <span class="apidocSignatureSpan">coap.</span>defaultTiming ()](#apidoc.element.coap.defaultTiming)
- description and source-code
```javascript
defaultTiming = function () {
  p.refreshTiming(defaultTiming)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.ignoreOption"></a>[function <span class="apidocSignatureSpan">coap.</span>ignoreOption (name)](#apidoc.element.coap.ignoreOption)
- description and source-code
```javascript
ignoreOption = function (name) {
  ignoredOptions[name] = true;
}
```
- example usage
```shell
...
Register a new option to be converted to string and added to the
'message.headers'.
'toBinary' is a function that accept a string and returns a 'Buffer'.
'toString' is a function that accept a 'Buffer' and returns a 'String'.

-------------------------------------------------------
<a name="ignoreOption"></a>
### coap.ignoreOption(name)

Explicitly ignore an option; useful for compatibility with 'http'-based
modules.

-------------------------------------------------------
<a name="registerFormat"></a>
### coap.registerFormat(name, value)
...
```

#### <a name="apidoc.element.coap.incoming_message"></a>[function <span class="apidocSignatureSpan">coap.</span>incoming_message (packet, rsinfo, outSocket)](#apidoc.element.coap.incoming_message)
- description and source-code
```javascript
function IncomingMessage(packet, rsinfo, outSocket) {
  Readable.call(this)

  pktToMsg(this, packet)

  this.rsinfo = rsinfo
  this.outSocket = outSocket

  this._packet = packet
  this._payloadIndex = 0
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_read_stream"></a>[function <span class="apidocSignatureSpan">coap.</span>observe_read_stream (packet, rsinfo, outSocket)](#apidoc.element.coap.observe_read_stream)
- description and source-code
```javascript
function ObserveReadStream(packet, rsinfo, outSocket) {
  Readable.call(this, { objectMode: true })

  this.rsinfo = rsinfo
  this.outSocket = outSocket

  this._lastId = 0
  this.append(packet)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_write_stream"></a>[function <span class="apidocSignatureSpan">coap.</span>observe_write_stream (request, send)](#apidoc.element.coap.observe_write_stream)
- description and source-code
```javascript
function ObserveWriteStream(request, send) {
  Writable.call(this)

  this._packet = {
      token: request.token
    , messageId: request.messageId
    , options: []
    , confirmable: false
    , ack: request.confirmable
    , reset: false
  }

  this._request = request
  this._send = send
  this.statusCode = ''

  this._counter = 0

  var that = this
  this.on('finish', function() {
    if (that._counter === 0) { // we have sent no messages
      that._doSend(null)
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.outgoing_message"></a>[function <span class="apidocSignatureSpan">coap.</span>outgoing_message (request, send)](#apidoc.element.coap.outgoing_message)
- description and source-code
```javascript
function OutgoingMessage(request, send) {
  BufferList.call(this)

  this._packet = {
      messageId: request.messageId
    , token: request.token
    , options: []
    , confirmable: false
    , ack: false
    , reset: false
  }

  var that = this

  if (request.confirmable) {
    // replying in piggyback
    this._packet.ack = true

    this._ackTimer = setTimeout(function() {

      send(that, helpers.genAck(request))

      // we are no more in piggyback
      that._packet.confirmable = true
      that._packet.ack = false

      // we need a new messageId for the CON
      // reply
      delete that._packet.messageId

      that._ackTimer = null

    }, request.piggybackReplyMs)
  }

  this._send = send

  this.statusCode = ''
  this.code = ''
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.registerFormat"></a>[function <span class="apidocSignatureSpan">coap.</span>registerFormat (name, value)](#apidoc.element.coap.registerFormat)
- description and source-code
```javascript
registerFormat = function (name, value) {
  var bytes;

  if (value > 255) {
    bytes = new Buffer(2);
    bytes.writeUInt16BE(value, 0);
  } else {
    bytes = new Buffer([value])
  }

  formatsString[name] = bytes
  formatsBinaries[value] = name
}
```
- example usage
```shell
...
### coap.ignoreOption(name)

Explicitly ignore an option; useful for compatibility with 'http'-based
modules.

-------------------------------------------------------
<a name="registerFormat"></a>
### coap.registerFormat(name, value)

Register a new format to be interpreted and sent in CoAP
'Content-Format' option.
Each format is identified by a number, see the [Content-Format
registry](http://tools.ietf.org/html/draft-ietf-core-coap-18#section-12.3).

These are the defaults formats:
...
```

#### <a name="apidoc.element.coap.registerOption"></a>[function <span class="apidocSignatureSpan">coap.</span>registerOption (name, toBinary, fromBinary)](#apidoc.element.coap.registerOption)
- description and source-code
```javascript
registerOption = function (name, toBinary, fromBinary) {
  optionFromBinaryFunctions[name] = fromBinary
  optionToBinaryFunctions[name] = toBinary
}
```
- example usage
```shell
...

#### reset()
Returns a Reset COAP Message to the sender. The RST message will appear as an empty message with code '0.00' and the
reset flag set to 'true' to the caller. This action ends the interaction with the caller.

-------------------------------------------------------
<a name="registerOption"></a>
### coap.registerOption(name, toBinary, toString)

Register a new option to be converted to string and added to the
'message.headers'.
'toBinary' is a function that accept a string and returns a 'Buffer'.
'toString' is a function that accept a 'Buffer' and returns a 'String'.

-------------------------------------------------------
...
```

#### <a name="apidoc.element.coap.request"></a>[function <span class="apidocSignatureSpan">coap.</span>request (url)](#apidoc.element.coap.request)
- description and source-code
```javascript
request = function (url) {
  var agent, req, ipv6

  if (typeof url === 'string')
    url = URL.parse(url)

  ipv6 = net.isIPv6(url.hostname || url.host)

  if (url.agent)
    agent = url.agent
  else if (url.agent === false && !ipv6)
    agent = new Agent({ type: 'udp4' })
  else if (url.agent === false && ipv6)
    agent = new Agent({ type: 'udp6' })
  else if (ipv6)
    agent = exports.globalAgentIPv6
  else
    agent = exports.globalAgent

  return agent.request(url)
}
```
- example usage
```shell
...

server.on('request', function(req, res) {
res.end('Hello ' + req.url.split('/')[1] + '\n')
})

// the default CoAP port is 5683
server.listen(function() {
var req = coap.request('coap://localhost/Matteo')

req.on('response', function(res) {
  res.pipe(process.stdout)
  res.on('end', function() {
    process.exit(0)
  })
})
...
```

#### <a name="apidoc.element.coap.retry_send"></a>[function <span class="apidocSignatureSpan">coap.</span>retry_send (sock, port, host)](#apidoc.element.coap.retry_send)
- description and source-code
```javascript
function RetrySend(sock, port, host) {
  if (!(this instanceof RetrySend))
    return new RetrySend(port, host)

  var that    = this

  this._sock  = sock

  this._port  = port || parameters.coapPort

  this._host  = host

  this._sendAttemp = 0
  this._lastMessageId = -1
  this._currentTime = parameters.ackTimeout * (1 + (parameters.ackRandomFactor - 1) * Math.random()) * 1000

  this._bOff  = function() {
    that._currentTime = that._currentTime * 2
    that._send()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.updateTiming"></a>[function <span class="apidocSignatureSpan">coap.</span>updateTiming (values)](#apidoc.element.coap.updateTiming)
- description and source-code
```javascript
updateTiming = function (values) {
  for (var key in values){
    if (p[key]) {
      p[key] = values[key]
    }
  }

  // MAX_TRANSMIT_SPAN is the maximum time from the first transmission
  // of a Confirmable message to its last retransmission.
  p.maxTransmitSpan = p.ackTimeout * ((Math.pow(2, p.maxRetransmit)) - 1) * p.ackRandomFactor

  // MAX_TRANSMIT_WAIT is the maximum time from the first transmission
  // of a Confirmable message to the time when the sender gives up on
  // receiving an acknowledgement or reset.
  p.maxTransmitWait = p.ackTimeout * (Math.pow(2, p.maxRetransmit + 1) - 1) * p.ackRandomFactor

  // PROCESSING_DELAY is the time a node takes to turn around a
  // Confirmable message into an acknowledgement.
  p.processingDelay = p.ackTimeout

  // MAX_RTT is the maximum round-trip time
  p.maxRTT = 2 * p.maxLatency + p.processingDelay

  //  EXCHANGE_LIFETIME is the time from starting to send a Confirmable
  //  message to the time when an acknowledgement is no longer expected,
  //  i.e.  message layer information about the message exchange can be
  //  purged
  p.exchangeLifetime = p.maxTransmitSpan + p.maxRTT

  // LRU prune timer period.
  // In order to reduce unnecessary heap usage on low-traffic servers the
  // LRU cache is periodically pruned to remove old, expired packets. This
  // is a fairly low-intensity task, but the period can be altered here
  // or the timer disabled by setting the value to zero.
  // By default the value is set to 0.5 x exchangeLifetime (~120s)
  if (values && (typeof(values.pruneTimerPeriod)==="number")) {
    p.pruneTimerPeriod = values.pruneTimerPeriod
  } else {
    p.pruneTimerPeriod =  (0.5 * p.exchangeLifetime)
  }
}
```
- example usage
```shell
...
var coapTiming = {
  ackTimeout:0.25,
  ackRandomFactor: 1.0,
  maxRetransmit: 3,
  maxLatency: 2,
  piggybackReplyMs: 10
};
coap.updateTiming(coapTiming);
'''

-------------------------------------------------------
<a name="defaultTiming"></a>
### coap.defaultTiming

Reset the CoAP timings to the default values
...
```



# <a name="apidoc.module.coap.Agent"></a>[module coap.Agent](#apidoc.module.coap.Agent)

#### <a name="apidoc.element.coap.Agent.Agent"></a>[function <span class="apidocSignatureSpan">coap.</span>Agent (opts)](#apidoc.element.coap.Agent.Agent)
- description and source-code
```javascript
function Agent(opts) {
  if (!(this instanceof Agent))
    return new Agent()

  if (!opts)
    opts = {}

  if (!opts.type)
    opts.type = 'udp4'

  if (opts.socket) {
    delete opts.port
  }

  this._opts = opts

  this._init(opts.socket)
}
```
- example usage
```shell
...
registerFormat('application/octet-stream', 42)
registerFormat('application/exi', 47)
registerFormat('application/json', 50)
'''

-------------------------------------------------------
<a name="agent"></a>
### coap.Agent([opts])

An Agent encapsulate an UDP Socket. It uses a combination of 'messageId'
and 'token' to distinguish between the different exchanges.
The socket will auto-close itself when no more exchange are in place.

By default, no UDP socket are open, and it is opened on demand to send
the messages.
...
```

#### <a name="apidoc.element.coap.Agent.super_"></a>[function <span class="apidocSignatureSpan">coap.Agent.</span>super_ ()](#apidoc.element.coap.Agent.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.Agent.prototype"></a>[module coap.Agent.prototype](#apidoc.module.coap.Agent.prototype)

#### <a name="apidoc.element.coap.Agent.prototype._cleanUp"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_cleanUp ()](#apidoc.element.coap.Agent.prototype._cleanUp)
- description and source-code
```javascript
function cleanUp() {
  if (--this._requests !== 0)
    return

  this._closing = true

  if (this._msgInFlight !== 0)
    return

  this._doClose()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.Agent.prototype._doClose"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_doClose ()](#apidoc.element.coap.Agent.prototype._doClose)
- description and source-code
```javascript
_doClose = function () {
  for (var k in this._msgIdToReq)
    this._msgIdToReq[k].sender.reset()

  if (this._opts.socket)
    return

  this._sock.close()
  this._sock = null
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.Agent.prototype._handle"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_handle (msg, rsinfo, outSocket)](#apidoc.element.coap.Agent.prototype._handle)
- description and source-code
```javascript
function handle(msg, rsinfo, outSocket) {
  var packet = parse(msg)
    , buf
    , response
    , that = this
    , req = this._msgIdToReq[packet.messageId]
    , ackSent = function(err) {
        if (err && req)
          req.emit('error', err)

        that._msgInFlight--
        if (that._closing && that._msgInFlight === 0) {
          that._doClose()
        }
      }

  if (!req) {
    if (packet.token.length == 4) {
      req = this._tkToReq[packet.token.readUInt32BE(0)]
    }

    if (packet.ack && !req) {
      // nothing to do, somehow there was
      // a duplicate ack
      return
    }

    if (!req) {
      buf = generate({
          code: '0.00'
        , reset: true
        , messageId: packet.messageId
      })

      this._msgInFlight++
      this._sock.send(buf, 0, buf.length, rsinfo.port, rsinfo.address, ackSent)
      return
    }
  }

  if (packet.confirmable) {
    buf = generate({
        code: '0.00'
      , ack: true
      , messageId: packet.messageId
    })

    this._msgInFlight++
    this._sock.send(buf, 0, buf.length, rsinfo.port, rsinfo.address, ackSent)
  }

  if (packet.code != '0.00' && (req._packet.token.length != packet.token.length || pf.compareBuffers(req._packet.token, packet.token
) != 0)) {
    // The tokens don't match, ignore the message since it is a malformed response
    return
  }

  if (!packet.confirmable && !req.multicast) {
    delete this._msgIdToReq[packet.messageId]
  }

  req.sender.reset()

  if (packet.code == '0.00')
    return

  var block2Buff = getOption(packet.options, 'Block2')
  var block2
  // if we got blockwise (2) response
  if (block2Buff) {
    block2 = parseBlock2(block2Buff)
    // check for error
    if (!block2) {
      req.sender.reset()
      return req.emit('error', new Error('failed to parse block2'))
    }
  }
  if (block2) {
    // accumulate payload
    req._totalPayload = Buffer.concat([req._totalPayload, packet.payload])

    if (block2.moreBlock2) {
      // increase message id for next request
      delete this._msgIdToReq[req._packet.messageId]
      req._packet.messageId = that._nextMessageId()
      this._msgIdToReq[req._packet.messageId] = req

      // next block2 request
      var block2Val = createBlock2({
        moreBlock2: false,
        num: block2.num+1,
        size: block2.size
      })
      if (!block2Val) {
        req.sender.reset()
        return req.emit('error', new Error('failed to create block2'))
      }
      req.setOption('Block2', block2Val)
      req.sender.send(generate(req._packet))

      return
    }
    else {
      // get full payload
      packet.payload = req._totalPayload
      // clear the payload incase of block2
      req._totalPayload = new Buffer(0)
    }
  }

  if (req.response) {
    if (req.response.append) {
      // it is an observe request
      // and we are already streaming
      return req.response.append(packet)
    } else {
      // TODO There is a previous response but is not an ObserveStream !
      return
    }

  }
  else if (block2) {
    delete that._tkToReq[req._packet.token.readUInt32BE(0)]
  }
  else if (!req.url.observe && packet.token.length > 0) {
    // it is not, so delete the token
    delete that._tkToReq[packet.token.readUInt32BE(0)]
  }

  if (req.url.observe && packet.code !== '4.04') {
    response = new ObserveStream(packet, rsinfo, outSocket)
    response.on('close', function() {
      delete that._tkToReq[packet.token.readUInt32BE(0)]
      that._cleanUp()
    })
  } else {
    response = new IncomingMessage(packet, rsinfo, outSocket)
  }

  if (!req.multicast) {
    req.response = response
  }

  req.emit('response', response)
}
```
- example usage
```shell
...
}

function handleServerRequest(request, next) {
  if (request.proxy) {
    return next();
  }
  try {
    request.server._handle(request.packet, request.rsinfo)
    next(null)
  } catch (err) {
    next(err)
  }
}

function proxyRequest(request, next) {
...
```

#### <a name="apidoc.element.coap.Agent.prototype._init"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_init (socket)](#apidoc.element.coap.Agent.prototype._init)
- description and source-code
```javascript
function initSock(socket) {
  if (this._sock) {
    return
  }

  var that = this
  this._sock = socket || dgram.createSocket(this._opts.type)
  this._sock.on('message', function(msg, rsinfo) {
    var packet
      , message
      , outSocket

    try {
      packet = parse(msg)
    } catch(err) {
      message = generate({ code: '5.00', payload: new Buffer('Unable to parse packet') })
      that._sock.send(message, 0, message.length,
                      rsinfo.port, rsinfo.address)
      return
    }

    if (packet.code[0] === '0' && packet.code !== '0.00') {
      // ignore this packet since it's not a response.
      return
    }

    outSocket = that._sock.address();
    that._handle(msg, rsinfo, outSocket)
  })

  if(this._opts.port){
    this._sock.bind( this._opts.port );
  };

  this._sock.on('error', function(err) {
    // we are skipping DNS errors
    if(!hasDNSbug || err.code !== 'ENOTFOUND')
      that.emit('error', err)
  })

  this._msgIdToReq = {}
  this._tkToReq = {}

  this._lastToken = Math.floor(Math.random() * (maxToken - 1))
  this._lastMessageId = Math.floor(Math.random() * (maxMessageId - 1))

  this._closing = false
  this._msgInFlight = 0
  this._requests = 0
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.Agent.prototype._nextMessageId"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_nextMessageId ()](#apidoc.element.coap.Agent.prototype._nextMessageId)
- description and source-code
```javascript
function nextToken() {
  if (++this._lastMessageId === maxMessageId)
    this._lastMessageId = 1

  return this._lastMessageId
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.Agent.prototype._nextToken"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>_nextToken ()](#apidoc.element.coap.Agent.prototype._nextToken)
- description and source-code
```javascript
function nextToken() {
  var buf = new Buffer(4)

  if (++this._lastToken === maxToken)
    this._lastToken = 0

  buf.writeUInt32BE(this._lastToken, 0)

  return buf;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.Agent.prototype.abort"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>abort (req)](#apidoc.element.coap.Agent.prototype.abort)
- description and source-code
```javascript
abort = function (req) {
  req.sender.removeAllListeners()
  req.sender.reset()
  this._cleanUp()
  delete this._msgIdToReq[req._packet.messageId]
  delete this._tkToReq[req._packet.token.readUInt32BE(0)]
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.Agent.prototype.request"></a>[function <span class="apidocSignatureSpan">coap.Agent.prototype.</span>request (url)](#apidoc.element.coap.Agent.prototype.request)
- description and source-code
```javascript
function request(url) {
  this._init()

  var req
    , response
    , options = url.options || url.headers
    , option
    , that = this
    , multicastTimeout = url.multicastTimeout !== undefined ? parseInt(url.multicastTimeout) : 20000

  req = new OutgoingMessage({}, function(req, packet) {
    var buf

    if (url.confirmable !== false) {
      packet.confirmable = true
    }

    // multicast message should be forced non-confirmable
    if (url.multicast === true) {
      req.multicast = true
      packet.confirmable = false
    }

    if (!(packet.ack || packet.reset)) {
      packet.messageId = that._nextMessageId()
      packet.token = that._nextToken()
    }

    try {
      buf = generate(packet)
    } catch(err) {
      req.sender.reset()
      return req.emit('error', err)
    }

    that._msgIdToReq[packet.messageId] = req
    that._tkToReq[that._lastToken] = req

    req.sender.send(buf, !packet.confirmable)
  })

  req.sender = new RetrySend(this._sock, url.port, url.hostname || url.host)

  req.url = url

  req.statusCode = url.method || 'GET'

  urlPropertyToPacketOption(url, req, 'pathname', 'Uri-Path', '/')
  urlPropertyToPacketOption(url, req, 'query', 'Uri-Query', '&')

  if (options) {
    for (option in options) {
      if (options.hasOwnProperty(option)) {
        req.setOption(option, options[option])
      }
    }
  }

  if (url.proxyUri) {
    req.setOption('Proxy-Uri', url.proxyUri)
  }

  req.sender.on('error', req.emit.bind(req, 'error'))

  req.sender.on('sending', function() {
    that._msgInFlight++
  })

  req.sender.on('timeout', function (err) {
    req.emit('timeout', err)
    that.abort(req)
  })

  req.sender.on('sent', function() {
    if (req.multicast) return;

    that._msgInFlight--
    if (that._closing && that._msgInFlight === 0) {
      that._doClose()
    }
  })

  // Start multicast monitoring timer in case of multicast request
  if (url.multicast === true) {
    req.multicastTimer = setTimeout(function() {
      that._msgInFlight--
      if (that._msgInFlight === 0) {
        that._doClose()
      }
    }, multicastTimeout)
  }

  if (url.observe)
    req.setOption('Observe', null)
  else
    req.on('response', this._cleanUp.bind(this))

  this._requests++

  req._totalPayload = new Buffer(0)

  return req
}
```
- example usage
```shell
...

server.on('request', function(req, res) {
res.end('Hello ' + req.url.split('/')[1] + '\n')
})

// the default CoAP port is 5683
server.listen(function() {
var req = coap.request('coap://localhost/Matteo')

req.on('response', function(res) {
  res.pipe(process.stdout)
  res.on('end', function() {
    process.exit(0)
  })
})
...
```



# <a name="apidoc.module.coap.createServer"></a>[module coap.createServer](#apidoc.module.coap.createServer)

#### <a name="apidoc.element.coap.createServer.createServer"></a>[function <span class="apidocSignatureSpan">coap.</span>createServer (options, listener)](#apidoc.element.coap.createServer.createServer)
- description and source-code
```javascript
function CoAPServer(options, listener) {
  if (!(this instanceof CoAPServer)) {
    return new CoAPServer(options, listener)
  }

  if (typeof options === 'function') {
    listener = options
    options = null
  }

  if (!options)
    options = {}

  this._options = options
  this._proxiedRequests = {}

  this._middlewares = [
    middlewares.parseRequest
  ]

  if (options.proxy) {
    this._middlewares.push(middlewares.proxyRequest)
    this._middlewares.push(middlewares.handleProxyResponse)
  }

  if (!this._options.piggybackReplyMs || !isNumeric(this._options.piggybackReplyMs)) {
    this._options.piggybackReplyMs = parameters.piggybackReplyMs
  }

  if (!isBoolean(this._options.sendAcksForNonConfirmablePackets)) {
    this._options.sendAcksForNonConfirmablePackets = parameters.sendAcksForNonConfirmablePackets
  }
  this._middlewares.push(middlewares.handleServerRequest)

  // Multicast settings
  this._multicastAddress = options.multicastAddress ? options.multicastAddress : null
  this._multicastInterface = options.multicastInterface ? options.multicastInterface : null

  // We use an LRU cache for the responses to avoid
  // DDOS problems.
  // max packet size is 1280
  // 32 MB / 1280 = 26214
  // The max lifetime is roughly 200s per packet.
  // Which gave us 131 packets/second guarantee
  this._lru = LRU({
      max: options.cacheSize || (32768 * 1024)
    , length: function(n) { return n.buffer.byteLength }
    , maxAge: (parameters.exchangeLifetime * 1000)
    , dispose:  function(key, value) {
                  if (value.sender)
                    value.sender.reset()
                }
  })

  this._series = series()
  this._block2Cache = {}

  if (listener)
    this.on('request', listener)
  debug('initialized');
}
```
- example usage
```shell
...
## Basic Example

The following example opens a UDP server and sends a
CoAP message to it:

'''js
var coap        = require('coap')
  , server      = coap.createServer()

server.on('request', function(req, res) {
  res.end('Hello ' + req.url.split('/')[1] + '\n')
})

// the default CoAP port is 5683
server.listen(function() {
...
```

#### <a name="apidoc.element.coap.createServer.super_"></a>[function <span class="apidocSignatureSpan">coap.createServer.</span>super_ ()](#apidoc.element.coap.createServer.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.createServer.prototype"></a>[module coap.createServer.prototype](#apidoc.module.coap.createServer.prototype)

#### <a name="apidoc.element.coap.createServer.prototype._handle"></a>[function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_handle (packet, rsinfo)](#apidoc.element.coap.createServer.prototype._handle)
- description and source-code
```javascript
_handle = function (packet, rsinfo) {

  if (packet.code[0] !== '0') {
    // According to RFC7252 Section 4.2 receiving a confirmable messages
    // that can't be processed, should be rejected by ignoring it AND
    // sending a reset. In this case confirmable response message would
    // be silently ignored, which is not exactly as stated in the standard.
    // However, sending a reset would interfere with a coap client which is
    // re-using a socket (see pull-request #131).
    return
  }

  var sock      = this._sock
    , lru       = this._lru
    , acks      = this._acks
    , cached    = lru.peek(toKey(rsinfo.address, rsinfo.port, packet, true))
    , Message   = OutMessage
    , that = this
    , request
    , response

  if (cached && !packet.ack && !packet.reset) {
    return sock.send(cached, 0, cached.length, rsinfo.port, rsinfo.address)
  } else if (cached && (packet.ack || packet.reset)) {
    if (cached.response && packet.reset) {
      cached.response.end()
    }
    return lru.del(toKey(rsinfo.address, rsinfo.port, packet, false))
  }
  else if (packet.ack || packet.reset) {
    return // nothing to do, ignoring silently
  }

  request = new IncomingMessage(packet, rsinfo)

  if (request.headers['Observe'] === 0) {
    Message = ObserveStream
    if (packet.code !== '0.01')
      // it is not a GET
      return this._sendError(new Buffer('Observe can only be present with a GET'), rsinfo)
  }

  packet.piggybackReplyMs = this._options.piggybackReplyMs;
  response = new Message(packet, function(response, packet) {
    var buf
      , sender = new RetrySend(sock, rsinfo.port, rsinfo.address)

    try {
      buf = generate(packet)
    } catch(err) {
      return response.emit('error', err)
    }

    if (Message === OutMessage) {
      sender.on('error', response.emit.bind(response, 'error'))
    } else {
      buf.response = response
      sender.on('error', function() {
        response.end()
      })
    }

    var key = toKey(rsinfo.address, rsinfo.port,
        packet, packet.ack || !packet.confirmable)
    lru.set(key, buf)
    buf.sender = sender

    if (that._options.sendAcksForNonConfirmablePackets || packet.confirmable){
      sender.send(buf, packet.ack || packet.reset || packet.confirmable === false)
    } else {
      debug('OMIT ACK PACKAGE')
    }
  })

  request.rsinfo = rsinfo
  response.statusCode = '2.05'
  response._request = request._packet
  response._cachekey = toCacheKey(rsinfo.address, rsinfo.port, packet)

  var block2cache = this._block2Cache
  //inject this function so the response can add an entry to the cache
  response._addCacheEntry = function(key, payload) {
    if (block2cache.hasOwnProperty(key)) {
      debug('reuse old cache entry, key:', key)
      clearTimeout(block2cache[key].timeoutId) // cancel old expiry timer
      block2cache[key].payload = payload
    } else {
      debug('add payload to cache, key:', key)
      block2cache[key] = {payload: payload}
    }
    // setup new expiry timer
    block2cache[key].timeoutId = setTimeout(expiry, parameters.exchangeLifetime * 1000, block2cache, key)
  }

  //return cached value for blockwise requests
  var cachedResponseSend = false
  if (packet.token && packet.token.length > 0) {
    // return cached value only if this request is not the first block request
    var block2Buff = getOption(response._request.options, 'Block2')
    var requestedBlockOption
    if (block2Buff) {
      requestedBlockOption = parseBlock2(block2Buff)
    }
    if (!requestedBlockOption) {
      requestedBlockOption = {num: 0}
    }

    if (requestedBlockOption.num < 1) {
      if (this._block2Cache.hasOwnProperty(response._cachekey)) {
        debug('first block2 request, remove old entry from cache, key:', response._cachekey)
        clearTimeout(this._block2Cache[response._cachekey].timeoutId)
        delete this._block2Cache[response._cachekey]
      }
    } else {
      debug('check if packet token is in cache, key:', response._cachekey)
      if (this._block2Cache.hasOwnProperty(response._cachekey)) {
        debug('found cached payload, key:' ...
```
- example usage
```shell
...
}

function handleServerRequest(request, next) {
  if (request.proxy) {
    return next();
  }
  try {
    request.server._handle(request.packet, request.rsinfo)
    next(null)
  } catch (err) {
    next(err)
  }
}

function proxyRequest(request, next) {
...
```

#### <a name="apidoc.element.coap.createServer.prototype._sendError"></a>[function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_sendError (payload, rsinfo, packet)](#apidoc.element.coap.createServer.prototype._sendError)
- description and source-code
```javascript
_sendError = function (payload, rsinfo, packet) {
  var message = generate({
    code: '5.00',
    payload: payload,
    messageId: (packet)?packet.messageId:undefined,
    token: (packet)?packet.token:undefined
  })

  this._sock.send(message, 0, message.length, rsinfo.port)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.createServer.prototype._sendProxied"></a>[function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_sendProxied (packet, proxyUri, callback)](#apidoc.element.coap.createServer.prototype._sendProxied)
- description and source-code
```javascript
_sendProxied = function (packet, proxyUri, callback) {
  var url = require('url').parse(proxyUri)
    , host = url.hostname
    , port = url.port
    , message = generate(removeProxyOptions(packet))

  this._sock.send(message, 0, message.length, port, host, callback)
}
```
- example usage
```shell
...

if (request.proxy) {
  if (request.packet.token.length === 0) {
    request.packet.token = crypto.randomBytes(8);
  }

  request.server._proxiedRequests[request.packet.token.toString('hex')] = request
  request.server._sendProxied(request.packet, request.proxy, next)
} else {
  next(null)
}
}

function isObserve(packet) {
return packet.options.map(isOption('Observe')).reduce(or, false);
...
```

#### <a name="apidoc.element.coap.createServer.prototype._sendReverseProxied"></a>[function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>_sendReverseProxied (packet, rsinfo, callback)](#apidoc.element.coap.createServer.prototype._sendReverseProxied)
- description and source-code
```javascript
_sendReverseProxied = function (packet, rsinfo, callback) {
  var host = rsinfo.address
    , port = rsinfo.port
    , message = generate(packet)

  this._sock.send(message, 0, message.length, port, host, callback)
}
```
- example usage
```shell
...
function handleProxyResponse(request, next) {
if (request.proxy) {
  return next(null)
}

var originalProxiedRequest = request.server._proxiedRequests[request.packet.token.toString('hex')]
if ( originalProxiedRequest ) {
  request.server._sendReverseProxied(request.packet, originalProxiedRequest.rsinfo)

  if (!isObserve(request.packet))
    delete request.server._proxiedRequests[request.packet.token.toString('hex')]

  next(null)
} else {
  next()
...
```

#### <a name="apidoc.element.coap.createServer.prototype.close"></a>[function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>close (done)](#apidoc.element.coap.createServer.prototype.close)
- description and source-code
```javascript
close = function (done) {
  if (done) {
    setImmediate(done)
  }

  if (this._lru.pruneTimer) {
    clearInterval(this._lru.pruneTimer)
  }

  if (this._sock) {
    this._sock.close()
    this._lru.reset()
    this._sock = null
    this.emit('close')
  } else {
    this._lru.reset()
  }

  // cancel cache entry expiry timers
  for (var k in this._block2Cache) {
    if (this._block2Cache.hasOwnProperty(k)) {
      debug('clean-up cache expiry timer, key:', k)
      clearTimeout(this._block2Cache[k].timeoutId)
      delete this._block2Cache[k]
    }
  }

  return this
}
```
- example usage
```shell
...
hostname is omitted, the server will accept connections directed to any
IPv4 or IPv6 address by passing 'null' as the address to the underlining socket.

To listen to a unix socket, supply a filename instead of port and hostname.

This function is asynchronous.

#### server.close([callback])

Closes the server.

This function is synchronous, but it provides an asynchronous callback
for convenience.

-------------------------------------------------------
...
```

#### <a name="apidoc.element.coap.createServer.prototype.listen"></a>[function <span class="apidocSignatureSpan">coap.createServer.prototype.</span>listen (port, address, done)](#apidoc.element.coap.createServer.prototype.listen)
- description and source-code
```javascript
listen = function (port, address, done) {
  var that = this

  if (port == undefined) {
    port = parameters.coapPort
  }

  if (typeof port === 'function') {
    done = port
    port = parameters.coapPort
  }

  if (typeof address === 'function') {
    done = address
    address = null
  }

  if (this._sock) {
    if (done)
      done(new Error('Already listening'))
    else
      throw new Error('Already listening')

    return this
  }

  if (address && net.isIPv6(address))
    this._options.type = 'udp6'

  if (!this._options.type)
    this._options.type = 'udp4'

  this._sock = dgram.createSocket({type: this._options.type, reuseAddr : true}, handleRequest(this))

  this._sock.on('error', function(error) {
    that.emit('error', error)
  })

  this._sock.bind(port, address || null, function () {
    if (that._multicastAddress) {
      that._sock.setMulticastLoopback(true)

      if (that._multicastInterface) {
        that._sock.addMembership(that._multicastAddress, that._multicastInterface)
      } else {
        allAddresses(that._options.type).forEach(function(interface) {
            that._sock.addMembership(that._multicastAddress, interface)
        })
      }
    }
    if (done) done()
  })
  this._port = port
  this._address = address

  if (parameters.pruneTimerPeriod) {
    // Start LRU pruning timer
    this._lru.pruneTimer = setInterval(function () {
      that._lru.prune()
    }, parameters.pruneTimerPeriod*1000)
    if (this._lru.pruneTimer.unref) {
      this._lru.pruneTimer.unref()
    }
  }

  return this
}
```
- example usage
```shell
...
, server      = coap.createServer()

server.on('request', function(req, res) {
res.end('Hello ' + req.url.split('/')[1] + '\n')
})

// the default CoAP port is 5683
server.listen(function() {
var req = coap.request('coap://localhost/Matteo')

req.on('response', function(res) {
  res.pipe(process.stdout)
  res.on('end', function() {
    process.exit(0)
  })
...
```



# <a name="apidoc.module.coap.helpers"></a>[module coap.helpers](#apidoc.module.coap.helpers)

#### <a name="apidoc.element.coap.helpers.addSetOption"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>addSetOption (klass)](#apidoc.element.coap.helpers.addSetOption)
- description and source-code
```javascript
addSetOption = function (klass) {
  var proto = klass.prototype
  proto.setOption = setOption
  proto.setHeader = setOption
}
```
- example usage
```shell
...
  if (that._counter === 0) { // we have sent no messages
    that._doSend(null)
  }
})
}

util.inherits(ObserveWriteStream, Writable)
helpers.addSetOption(ObserveWriteStream)

ObserveWriteStream.prototype._write = function write(data, encoding, done) {
this.setOption('Observe', ++this._counter)

if (this._counter === 16777215)
  this._counter = 1
...
```

#### <a name="apidoc.element.coap.helpers.createBlock2"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>createBlock2 (requestedBlock)](#apidoc.element.coap.helpers.createBlock2)
- description and source-code
```javascript
function createBlock2(requestedBlock) {
  var byte
  var szx = Math.log(requestedBlock.size)/Math.log(2) - 4
  var m = ((requestedBlock.moreBlock2==true)?0:1)
  var num = requestedBlock.num
  var extraNum

  byte = 0
  byte |= szx
  byte |= m << 3
  byte |= (num&0xf) <<4

  // total num occupy up to 5 octets
  // num share the higher octet of first byte, and (may) take more 2 bytes for the rest 4 octets
  if (num <= 0xf) {
    extraNum = null
  }
  else if (num <=0xfff) {
    extraNum = new Buffer([num/16])
  }
  else if (num <=0xfffff) {
    extraNum = new Buffer(2)
    extraNum.writeUInt16BE(num>>4,0)
  }
  else {
    // too big block2 number
    return null
  }
  return (extraNum)? Buffer.concat([extraNum, new Buffer([byte])]):new Buffer([byte])
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.genAck"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>genAck (request)](#apidoc.element.coap.helpers.genAck)
- description and source-code
```javascript
genAck = function (request) {
  return {
      messageId: request.messageId
    , code: '0.00'
    , options: []
    , confirmable: false
    , ack: true
    , reset: false
  }
}
```
- example usage
```shell
...

  if (request.confirmable) {
    // replying in piggyback
    this._packet.ack = true

    this._ackTimer = setTimeout(function() {

send(that, helpers.genAck(request))

// we are no more in piggyback
that._packet.confirmable = true
that._packet.ack = false

// we need a new messageId for the CON
// reply
...
```

#### <a name="apidoc.element.coap.helpers.getOption"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>getOption (options, name)](#apidoc.element.coap.helpers.getOption)
- description and source-code
```javascript
function getOption(options, name) {
  for (var i in options)
    if (options[i].name == name)
      return options[i].value
  return null
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.isBoolean"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>isBoolean (n)](#apidoc.element.coap.helpers.isBoolean)
- description and source-code
```javascript
function isBoolean(n) {
  return typeof(n) === 'boolean';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.isNumeric"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>isNumeric (n)](#apidoc.element.coap.helpers.isNumeric)
- description and source-code
```javascript
function isNumeric(n) {
  return !isNaN(parseFloat(n)) && isFinite(n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.isOption"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>isOption (optionName)](#apidoc.element.coap.helpers.isOption)
- description and source-code
```javascript
function isOption(optionName) {
  return function(option) {
    return option.name === optionName;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.or"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>or (previous, current)](#apidoc.element.coap.helpers.or)
- description and source-code
```javascript
function or(previous, current) {
    return previous || current;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.packetToMessage"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>packetToMessage (dest, packet)](#apidoc.element.coap.helpers.packetToMessage)
- description and source-code
```javascript
function packetToMessage(dest, packet) {

  var i
    , options = packet.options
    , option
    , paths   = []
    , queries = []
    , query   = ''

  dest.payload = packet.payload
  dest.options = packet.options
  dest.code    = packet.code
  dest.method  = codes[packet.code]
  dest.headers = {}

  for (i=0; i < options.length; i++) {
    option = options[i]

    if (option.name === 'Uri-Path') {
      paths.push(option.value)
    }

    if (option.name === 'Uri-Query') {
      queries.push(option.value)
    }

    option.value = fromBinary(option.name, option.value)

    if (!Buffer.isBuffer(option.value))
      dest.headers[option.name] = option.value
  }

  if (dest.headers['Content-Format'])
    dest.headers['Content-Type'] = dest.headers['Content-Format']

  query = queries.join('&')
  dest.url = '/' + paths.join('/')
  if (query) {
    dest.url += '?' + query
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.parseBlock2"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>parseBlock2 (block2Value)](#apidoc.element.coap.helpers.parseBlock2)
- description and source-code
```javascript
function parseBlock2(block2Value) {
  var num
  switch (block2Value.length) {
    case 1:
    num = block2Value[0] >> 4
    break
    case 2:
    num = (block2Value[0]*256 + block2Value[1]) >> 4
    break
    case 3:
    num = (block2Value[0]*256*256 + block2Value[1]*256 + block2Value[2]) >>4
    break
    default:
    // Block2 is more than 3 bytes
    return null
  }
  // limit value of size is 1024 (2**(6+4))
  if (block2Value.slice(-1)[0] == 7) {
    // Block size is bigger than 1024
    return null
  }
  return {
    moreBlock2: (block2Value.slice(-1)[0] & (0x01<<3))? true:false,
    num: num,
    size: Math.pow(2, (block2Value.slice(-1)[0] & 0x07)+4)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.helpers.toCode"></a>[function <span class="apidocSignatureSpan">coap.helpers.</span>toCode (code)](#apidoc.element.coap.helpers.toCode)
- description and source-code
```javascript
function toCode(code) {
  if (typeof code === 'string')
    return code

  var first  = Math.floor(code / 100)
    , second = code - first * 100
    , result = ''

  result += first + '.'

  if (second < 10)
    result += '0'

  result += second

  return result
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.incoming_message"></a>[module coap.incoming_message](#apidoc.module.coap.incoming_message)

#### <a name="apidoc.element.coap.incoming_message.incoming_message"></a>[function <span class="apidocSignatureSpan">coap.</span>incoming_message (packet, rsinfo, outSocket)](#apidoc.element.coap.incoming_message.incoming_message)
- description and source-code
```javascript
function IncomingMessage(packet, rsinfo, outSocket) {
  Readable.call(this)

  pktToMsg(this, packet)

  this.rsinfo = rsinfo
  this.outSocket = outSocket

  this._packet = packet
  this._payloadIndex = 0
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.incoming_message.super_"></a>[function <span class="apidocSignatureSpan">coap.incoming_message.</span>super_ (options)](#apidoc.element.coap.incoming_message.super_)
- description and source-code
```javascript
function Readable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  if (!(this instanceof Readable)) return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function') this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.incoming_message.prototype"></a>[module coap.incoming_message.prototype](#apidoc.module.coap.incoming_message.prototype)

#### <a name="apidoc.element.coap.incoming_message.prototype._read"></a>[function <span class="apidocSignatureSpan">coap.incoming_message.prototype.</span>_read (size)](#apidoc.element.coap.incoming_message.prototype._read)
- description and source-code
```javascript
_read = function (size) {
  var end     = this._payloadIndex + size
    , start   = this._payloadIndex
    , payload = this._packet.payload
    , buf     = null

  if (start < payload.length)
    buf = payload.slice(start, end)

  this._payloadIndex = end
  this.push(buf)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.middlewares"></a>[module coap.middlewares](#apidoc.module.coap.middlewares)

#### <a name="apidoc.element.coap.middlewares.handleProxyResponse"></a>[function <span class="apidocSignatureSpan">coap.middlewares.</span>handleProxyResponse (request, next)](#apidoc.element.coap.middlewares.handleProxyResponse)
- description and source-code
```javascript
function handleProxyResponse(request, next) {
  if (request.proxy) {
    return next(null)
  }

  var originalProxiedRequest = request.server._proxiedRequests[request.packet.token.toString('hex')]
  if ( originalProxiedRequest ) {
    request.server._sendReverseProxied(request.packet, originalProxiedRequest.rsinfo)

    if (!isObserve(request.packet))
      delete request.server._proxiedRequests[request.packet.token.toString('hex')]

    next(null)
  } else {
    next()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.middlewares.handleServerRequest"></a>[function <span class="apidocSignatureSpan">coap.middlewares.</span>handleServerRequest (request, next)](#apidoc.element.coap.middlewares.handleServerRequest)
- description and source-code
```javascript
function handleServerRequest(request, next) {
  if (request.proxy) {
    return next();
  }
  try {
    request.server._handle(request.packet, request.rsinfo)
    next(null)
  } catch (err) {
    next(err)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.middlewares.parseRequest"></a>[function <span class="apidocSignatureSpan">coap.middlewares.</span>parseRequest (request, next)](#apidoc.element.coap.middlewares.parseRequest)
- description and source-code
```javascript
function parseRequest(request, next) {
  try {
    request.packet = parse(request.raw)
    next(null)
  } catch (err) {
    next(err)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.middlewares.proxyRequest"></a>[function <span class="apidocSignatureSpan">coap.middlewares.</span>proxyRequest (request, next)](#apidoc.element.coap.middlewares.proxyRequest)
- description and source-code
```javascript
function proxyRequest(request, next) {
  for (var i = 0; i < request.packet.options.length; i++) {
    if (request.packet.options[i].name.toLowerCase() === 'proxy-uri') {
      request.proxy = request.packet.options[i].value.toString()
    }
  }

  if (request.proxy) {
    if (request.packet.token.length === 0) {
      request.packet.token = crypto.randomBytes(8);
    }

    request.server._proxiedRequests[request.packet.token.toString('hex')] = request
    request.server._sendProxied(request.packet, request.proxy, next)
  } else {
    next(null)
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.observe_read_stream"></a>[module coap.observe_read_stream](#apidoc.module.coap.observe_read_stream)

#### <a name="apidoc.element.coap.observe_read_stream.observe_read_stream"></a>[function <span class="apidocSignatureSpan">coap.</span>observe_read_stream (packet, rsinfo, outSocket)](#apidoc.element.coap.observe_read_stream.observe_read_stream)
- description and source-code
```javascript
function ObserveReadStream(packet, rsinfo, outSocket) {
  Readable.call(this, { objectMode: true })

  this.rsinfo = rsinfo
  this.outSocket = outSocket

  this._lastId = 0
  this.append(packet)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_read_stream.super_"></a>[function <span class="apidocSignatureSpan">coap.observe_read_stream.</span>super_ (options)](#apidoc.element.coap.observe_read_stream.super_)
- description and source-code
```javascript
function Readable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  if (!(this instanceof Readable)) return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function') this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.observe_read_stream.prototype"></a>[module coap.observe_read_stream.prototype](#apidoc.module.coap.observe_read_stream.prototype)

#### <a name="apidoc.element.coap.observe_read_stream.prototype._read"></a>[function <span class="apidocSignatureSpan">coap.observe_read_stream.prototype.</span>_read ()](#apidoc.element.coap.observe_read_stream.prototype._read)
- description and source-code
```javascript
_read = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_read_stream.prototype.append"></a>[function <span class="apidocSignatureSpan">coap.observe_read_stream.prototype.</span>append (packet)](#apidoc.element.coap.observe_read_stream.prototype.append)
- description and source-code
```javascript
append = function (packet) {
  if (!this.readable)
    return

  pktToMsg(this, packet)
  if (this.headers['Observe'] > this._lastId) {
    this._lastId = this.headers['Observe']
    this.push(packet.payload)
  }
}
```
- example usage
```shell
...
function ObserveReadStream(packet, rsinfo, outSocket) {
Readable.call(this, { objectMode: true })

this.rsinfo = rsinfo
this.outSocket = outSocket

this._lastId = 0
this.append(packet)
}

util.inherits(ObserveReadStream, Readable)

ObserveReadStream.prototype.append = function(packet) {
if (!this.readable)
  return
...
```

#### <a name="apidoc.element.coap.observe_read_stream.prototype.close"></a>[function <span class="apidocSignatureSpan">coap.observe_read_stream.prototype.</span>close ()](#apidoc.element.coap.observe_read_stream.prototype.close)
- description and source-code
```javascript
close = function () {
  this.push(null)
  this.emit('close')
}
```
- example usage
```shell
...
hostname is omitted, the server will accept connections directed to any
IPv4 or IPv6 address by passing 'null' as the address to the underlining socket.

To listen to a unix socket, supply a filename instead of port and hostname.

This function is asynchronous.

#### server.close([callback])

Closes the server.

This function is synchronous, but it provides an asynchronous callback
for convenience.

-------------------------------------------------------
...
```



# <a name="apidoc.module.coap.observe_write_stream"></a>[module coap.observe_write_stream](#apidoc.module.coap.observe_write_stream)

#### <a name="apidoc.element.coap.observe_write_stream.observe_write_stream"></a>[function <span class="apidocSignatureSpan">coap.</span>observe_write_stream (request, send)](#apidoc.element.coap.observe_write_stream.observe_write_stream)
- description and source-code
```javascript
function ObserveWriteStream(request, send) {
  Writable.call(this)

  this._packet = {
      token: request.token
    , messageId: request.messageId
    , options: []
    , confirmable: false
    , ack: request.confirmable
    , reset: false
  }

  this._request = request
  this._send = send
  this.statusCode = ''

  this._counter = 0

  var that = this
  this.on('finish', function() {
    if (that._counter === 0) { // we have sent no messages
      that._doSend(null)
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_write_stream.super_"></a>[function <span class="apidocSignatureSpan">coap.observe_write_stream.</span>super_ (options)](#apidoc.element.coap.observe_write_stream.super_)
- description and source-code
```javascript
function Writable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  // Writable ctor is applied to Duplexes, too.
  // 'realHasInstance' is necessary because using plain 'instanceof'
  // would return false, as no '_writableState' property is attached.

  // Trying to use the custom 'instanceof' for Writable here will also break the
  // Node.js LazyTransform implementation, which has a non-trivial getter for
  // '_writableState' that would lead to infinite recursion.
  if (!realHasInstance.call(Writable, this) && !(this instanceof Duplex)) {
    return new Writable(options);
  }

  this._writableState = new WritableState(options, this);

  // legacy.
  this.writable = true;

  if (options) {
    if (typeof options.write === 'function') this._write = options.write;

    if (typeof options.writev === 'function') this._writev = options.writev;
  }

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.observe_write_stream.prototype"></a>[module coap.observe_write_stream.prototype](#apidoc.module.coap.observe_write_stream.prototype)

#### <a name="apidoc.element.coap.observe_write_stream.prototype._doSend"></a>[function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>_doSend (data)](#apidoc.element.coap.observe_write_stream.prototype._doSend)
- description and source-code
```javascript
function doSend(data) {
  var packet = this._packet
  packet.code = this.statusCode
  packet.payload = data
  this._send(this, packet)

  this._packet.confirmable = this._request.confirmable
  this._packet.ack = !this._request.confirmable
  delete this._packet.messageId
  delete this._packet.payload
}
```
- example usage
```shell
...
  this.statusCode = ''

  this._counter = 0

  var that = this
  this.on('finish', function() {
    if (that._counter === 0) { // we have sent no messages
      that._doSend(null)
    }
  })
}

util.inherits(ObserveWriteStream, Writable)
helpers.addSetOption(ObserveWriteStream)
...
```

#### <a name="apidoc.element.coap.observe_write_stream.prototype._write"></a>[function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>_write (data, encoding, done)](#apidoc.element.coap.observe_write_stream.prototype._write)
- description and source-code
```javascript
function write(data, encoding, done) {
  this.setOption('Observe', ++this._counter)

  if (this._counter === 16777215)
    this._counter = 1

  this._doSend(data)

  done()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_write_stream.prototype.reset"></a>[function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>reset ()](#apidoc.element.coap.observe_write_stream.prototype.reset)
- description and source-code
```javascript
function reset() {
  var packet = this._packet
  packet.code = '0.00'
  packet.payload = ''
  packet.reset = true;
  packet.ack = false
  packet.token = new Buffer(0);

  this._send(this, packet)

  this._packet.confirmable = this._request.confirmable
  delete this._packet.messageId
  delete this._packet.payload
}
```
- example usage
```shell
...
them by adding a 'req.setOption('Block2', new Buffer([0x2]))' to the
output of [request](#request).

See the
[spec](http://tools.ietf.org/html/draft-ietf-core-coap-18#section-5.4)
for all the possible options.

#### message.reset()
Returns a Reset COAP Message to the sender. The RST message will appear as an empty message with code '0.00' and the
reset flag set to 'true' to the caller. This action ends the interaction with the caller.

#### message.writeHead(code, headers)
Functions somewhat like 'http''s 'writeHead()' function.  If 'code' is does not match the CoAP code mask of '#.##', it is coerced
 into this mask.  'headers' is an object with keys being the header names, and values being the header values.

-------------------------------------------------------
...
```

#### <a name="apidoc.element.coap.observe_write_stream.prototype.setHeader"></a>[function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>setHeader (name, values)](#apidoc.element.coap.observe_write_stream.prototype.setHeader)
- description and source-code
```javascript
function setOption(name, values) {
  var i

  name = capitalize.words(name)
  name = optionAliases[name] || name

  if (isIgnored(name)) {
    return this
  }

  this._packet.options = this._packet.options.filter(function(option) {
    return option.name !== name
  })

  if (!Array.isArray(values))
    values = [values]

  for (i = 0; i < values.length; i++) {
    this._packet.options.push({
        name: name
      , value: toBinary(name, values[i])
    })
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.observe_write_stream.prototype.setOption"></a>[function <span class="apidocSignatureSpan">coap.observe_write_stream.prototype.</span>setOption (name, values)](#apidoc.element.coap.observe_write_stream.prototype.setOption)
- description and source-code
```javascript
function setOption(name, values) {
  var i

  name = capitalize.words(name)
  name = optionAliases[name] || name

  if (isIgnored(name)) {
    return this
  }

  this._packet.options = this._packet.options.filter(function(option) {
    return option.name !== name
  })

  if (!Array.isArray(values))
    values = [values]

  for (i = 0; i < values.length; i++) {
    this._packet.options.push({
        name: name
      , value: toBinary(name, values[i])
    })
  }

  return this
}
```
- example usage
```shell
...
It is HTTP-compatible, as it can be passed '404'.

#### message.statusCode

(same as message.code)

<a name="setOption"></a>
#### message.setOption(name, value)

Sets a single option value.
All the options are in binary format, except for
''Content-Format'', ''Accept'', ''Max-Age'' and ''ETag''.
See <a href='#registerOption'><code>registerOption</code></a>
to know how to register more.
...
```



# <a name="apidoc.module.coap.option_converter"></a>[module coap.option_converter](#apidoc.module.coap.option_converter)

#### <a name="apidoc.element.coap.option_converter.fromBinary"></a>[function <span class="apidocSignatureSpan">coap.option_converter.</span>fromBinary (name, value)](#apidoc.element.coap.option_converter.fromBinary)
- description and source-code
```javascript
fromBinary = function (name, value) {
  var convert = optionFromBinaryFunctions[name]

  if (!convert)
    return value

  return convert(value)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.option_converter.ignoreOption"></a>[function <span class="apidocSignatureSpan">coap.option_converter.</span>ignoreOption (name)](#apidoc.element.coap.option_converter.ignoreOption)
- description and source-code
```javascript
ignoreOption = function (name) {
  ignoredOptions[name] = true;
}
```
- example usage
```shell
...
Register a new option to be converted to string and added to the
'message.headers'.
'toBinary' is a function that accept a string and returns a 'Buffer'.
'toString' is a function that accept a 'Buffer' and returns a 'String'.

-------------------------------------------------------
<a name="ignoreOption"></a>
### coap.ignoreOption(name)

Explicitly ignore an option; useful for compatibility with 'http'-based
modules.

-------------------------------------------------------
<a name="registerFormat"></a>
### coap.registerFormat(name, value)
...
```

#### <a name="apidoc.element.coap.option_converter.isIgnored"></a>[function <span class="apidocSignatureSpan">coap.option_converter.</span>isIgnored (name)](#apidoc.element.coap.option_converter.isIgnored)
- description and source-code
```javascript
isIgnored = function (name) {
  return !!ignoredOptions[name]
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.option_converter.registerFormat"></a>[function <span class="apidocSignatureSpan">coap.option_converter.</span>registerFormat (name, value)](#apidoc.element.coap.option_converter.registerFormat)
- description and source-code
```javascript
registerFormat = function (name, value) {
  var bytes;

  if (value > 255) {
    bytes = new Buffer(2);
    bytes.writeUInt16BE(value, 0);
  } else {
    bytes = new Buffer([value])
  }

  formatsString[name] = bytes
  formatsBinaries[value] = name
}
```
- example usage
```shell
...
### coap.ignoreOption(name)

Explicitly ignore an option; useful for compatibility with 'http'-based
modules.

-------------------------------------------------------
<a name="registerFormat"></a>
### coap.registerFormat(name, value)

Register a new format to be interpreted and sent in CoAP
'Content-Format' option.
Each format is identified by a number, see the [Content-Format
registry](http://tools.ietf.org/html/draft-ietf-core-coap-18#section-12.3).

These are the defaults formats:
...
```

#### <a name="apidoc.element.coap.option_converter.registerOption"></a>[function <span class="apidocSignatureSpan">coap.option_converter.</span>registerOption (name, toBinary, fromBinary)](#apidoc.element.coap.option_converter.registerOption)
- description and source-code
```javascript
registerOption = function (name, toBinary, fromBinary) {
  optionFromBinaryFunctions[name] = fromBinary
  optionToBinaryFunctions[name] = toBinary
}
```
- example usage
```shell
...

#### reset()
Returns a Reset COAP Message to the sender. The RST message will appear as an empty message with code '0.00' and the
reset flag set to 'true' to the caller. This action ends the interaction with the caller.

-------------------------------------------------------
<a name="registerOption"></a>
### coap.registerOption(name, toBinary, toString)

Register a new option to be converted to string and added to the
'message.headers'.
'toBinary' is a function that accept a string and returns a 'Buffer'.
'toString' is a function that accept a 'Buffer' and returns a 'String'.

-------------------------------------------------------
...
```

#### <a name="apidoc.element.coap.option_converter.toBinary"></a>[function <span class="apidocSignatureSpan">coap.option_converter.</span>toBinary (name, value)](#apidoc.element.coap.option_converter.toBinary)
- description and source-code
```javascript
toBinary = function (name, value) {
  if (Buffer.isBuffer(value))
    return value

  if (!optionToBinaryFunctions[name])
    throw new Error('Unknown string to Buffer converter for option: ' + name)

  return optionToBinaryFunctions[name](value)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.outgoing_message"></a>[module coap.outgoing_message](#apidoc.module.coap.outgoing_message)

#### <a name="apidoc.element.coap.outgoing_message.outgoing_message"></a>[function <span class="apidocSignatureSpan">coap.</span>outgoing_message (request, send)](#apidoc.element.coap.outgoing_message.outgoing_message)
- description and source-code
```javascript
function OutgoingMessage(request, send) {
  BufferList.call(this)

  this._packet = {
      messageId: request.messageId
    , token: request.token
    , options: []
    , confirmable: false
    , ack: false
    , reset: false
  }

  var that = this

  if (request.confirmable) {
    // replying in piggyback
    this._packet.ack = true

    this._ackTimer = setTimeout(function() {

      send(that, helpers.genAck(request))

      // we are no more in piggyback
      that._packet.confirmable = true
      that._packet.ack = false

      // we need a new messageId for the CON
      // reply
      delete that._packet.messageId

      that._ackTimer = null

    }, request.piggybackReplyMs)
  }

  this._send = send

  this.statusCode = ''
  this.code = ''
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.outgoing_message.super_"></a>[function <span class="apidocSignatureSpan">coap.outgoing_message.</span>super_ (callback)](#apidoc.element.coap.outgoing_message.super_)
- description and source-code
```javascript
function BufferList(callback) {
  if (!(this instanceof BufferList))
    return new BufferList(callback)

  this._bufs  = []
  this.length = 0

  if (typeof callback == 'function') {
    this._callback = callback

    var piper = function piper (err) {
      if (this._callback) {
        this._callback(err)
        this._callback = null
      }
    }.bind(this)

    this.on('pipe', function onPipe (src) {
      src.on('error', piper)
    })
    this.on('unpipe', function onUnpipe (src) {
      src.removeListener('error', piper)
    })
  } else {
    this.append(callback)
  }

  DuplexStream.call(this)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.outgoing_message.prototype"></a>[module coap.outgoing_message.prototype](#apidoc.module.coap.outgoing_message.prototype)

#### <a name="apidoc.element.coap.outgoing_message.prototype.end"></a>[function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>end (a, b)](#apidoc.element.coap.outgoing_message.prototype.end)
- description and source-code
```javascript
end = function (a, b) {
  BufferList.prototype.end.call(this, a, b)

  var packet = this._packet
    , message
    , that = this

  packet.code = toCode(this.code || this.statusCode)
  packet.payload = this
  this._send(this, packet)

  // easy clean up after generating the packet
  delete this._packet.payload

  if (this._ackTimer)
    clearTimeout(this._ackTimer)

  return this
}
```
- example usage
```shell
...
CoAP message to it:

'''js
var coap        = require('coap')
, server      = coap.createServer()

server.on('request', function(req, res) {
res.end('Hello ' + req.url.split('/')[1] + '\n')
})

// the default CoAP port is 5683
server.listen(function() {
var req = coap.request('coap://localhost/Matteo')

req.on('response', function(res) {
...
```

#### <a name="apidoc.element.coap.outgoing_message.prototype.reset"></a>[function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>reset ()](#apidoc.element.coap.outgoing_message.prototype.reset)
- description and source-code
```javascript
reset = function () {
  BufferList.prototype.end.call(this)

  var packet = this._packet
    , message
    , that = this

  packet.code = '0.00'
  packet.payload = ''
  packet.reset = true;
  packet.ack = false

  this._send(this, packet)

  // easy clean up after generating the packet
  delete this._packet.payload

  if (this._ackTimer)
    clearTimeout(this._ackTimer)

  return this
}
```
- example usage
```shell
...
them by adding a 'req.setOption('Block2', new Buffer([0x2]))' to the
output of [request](#request).

See the
[spec](http://tools.ietf.org/html/draft-ietf-core-coap-18#section-5.4)
for all the possible options.

#### message.reset()
Returns a Reset COAP Message to the sender. The RST message will appear as an empty message with code '0.00' and the
reset flag set to 'true' to the caller. This action ends the interaction with the caller.

#### message.writeHead(code, headers)
Functions somewhat like 'http''s 'writeHead()' function.  If 'code' is does not match the CoAP code mask of '#.##', it is coerced
 into this mask.  'headers' is an object with keys being the header names, and values being the header values.

-------------------------------------------------------
...
```

#### <a name="apidoc.element.coap.outgoing_message.prototype.setHeader"></a>[function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>setHeader (name, values)](#apidoc.element.coap.outgoing_message.prototype.setHeader)
- description and source-code
```javascript
function setOption(name, values) {
  var i

  name = capitalize.words(name)
  name = optionAliases[name] || name

  if (isIgnored(name)) {
    return this
  }

  this._packet.options = this._packet.options.filter(function(option) {
    return option.name !== name
  })

  if (!Array.isArray(values))
    values = [values]

  for (i = 0; i < values.length; i++) {
    this._packet.options.push({
        name: name
      , value: toBinary(name, values[i])
    })
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.outgoing_message.prototype.setOption"></a>[function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>setOption (name, values)](#apidoc.element.coap.outgoing_message.prototype.setOption)
- description and source-code
```javascript
function setOption(name, values) {
  var i

  name = capitalize.words(name)
  name = optionAliases[name] || name

  if (isIgnored(name)) {
    return this
  }

  this._packet.options = this._packet.options.filter(function(option) {
    return option.name !== name
  })

  if (!Array.isArray(values))
    values = [values]

  for (i = 0; i < values.length; i++) {
    this._packet.options.push({
        name: name
      , value: toBinary(name, values[i])
    })
  }

  return this
}
```
- example usage
```shell
...
It is HTTP-compatible, as it can be passed '404'.

#### message.statusCode

(same as message.code)

<a name="setOption"></a>
#### message.setOption(name, value)

Sets a single option value.
All the options are in binary format, except for
''Content-Format'', ''Accept'', ''Max-Age'' and ''ETag''.
See <a href='#registerOption'><code>registerOption</code></a>
to know how to register more.
...
```

#### <a name="apidoc.element.coap.outgoing_message.prototype.writeHead"></a>[function <span class="apidocSignatureSpan">coap.outgoing_message.prototype.</span>writeHead (code, headers)](#apidoc.element.coap.outgoing_message.prototype.writeHead)
- description and source-code
```javascript
writeHead = function (code, headers) {
  var packet = this._packet
  var header
  packet.code = String(code).replace(/(^\d[^.])/, '$1.')
  for (header in headers) {
    if (headers.hasOwnProperty(header)) {
      this.setOption(header, headers[header])
    }
  }
}
```
- example usage
```shell
...
[spec](http://tools.ietf.org/html/draft-ietf-core-coap-18#section-5.4)
for all the possible options.

#### message.reset()
Returns a Reset COAP Message to the sender. The RST message will appear as an empty message with code '0.00' and the
reset flag set to 'true' to the caller. This action ends the interaction with the caller.

#### message.writeHead(code, headers)
Functions somewhat like 'http''s 'writeHead()' function.  If 'code' is does not match the CoAP code mask of '#.##', it is coerced
 into this mask.  'headers' is an object with keys being the header names, and values being the header values.

-------------------------------------------------------
<a name="incoming"></a>
### IncomingMessage

An 'IncomingMessage' object is created by 'coap.createServer' or
...
```



# <a name="apidoc.module.coap.parameters"></a>[module coap.parameters](#apidoc.module.coap.parameters)

#### <a name="apidoc.element.coap.parameters.defaultTiming"></a>[function <span class="apidocSignatureSpan">coap.parameters.</span>defaultTiming ()](#apidoc.element.coap.parameters.defaultTiming)
- description and source-code
```javascript
defaultTiming = function () {
  p.refreshTiming(defaultTiming)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.parameters.refreshTiming"></a>[function <span class="apidocSignatureSpan">coap.parameters.</span>refreshTiming (values)](#apidoc.element.coap.parameters.refreshTiming)
- description and source-code
```javascript
refreshTiming = function (values) {
  for (var key in values){
    if (p[key]) {
      p[key] = values[key]
    }
  }

  // MAX_TRANSMIT_SPAN is the maximum time from the first transmission
  // of a Confirmable message to its last retransmission.
  p.maxTransmitSpan = p.ackTimeout * ((Math.pow(2, p.maxRetransmit)) - 1) * p.ackRandomFactor

  // MAX_TRANSMIT_WAIT is the maximum time from the first transmission
  // of a Confirmable message to the time when the sender gives up on
  // receiving an acknowledgement or reset.
  p.maxTransmitWait = p.ackTimeout * (Math.pow(2, p.maxRetransmit + 1) - 1) * p.ackRandomFactor

  // PROCESSING_DELAY is the time a node takes to turn around a
  // Confirmable message into an acknowledgement.
  p.processingDelay = p.ackTimeout

  // MAX_RTT is the maximum round-trip time
  p.maxRTT = 2 * p.maxLatency + p.processingDelay

  //  EXCHANGE_LIFETIME is the time from starting to send a Confirmable
  //  message to the time when an acknowledgement is no longer expected,
  //  i.e.  message layer information about the message exchange can be
  //  purged
  p.exchangeLifetime = p.maxTransmitSpan + p.maxRTT

  // LRU prune timer period.
  // In order to reduce unnecessary heap usage on low-traffic servers the
  // LRU cache is periodically pruned to remove old, expired packets. This
  // is a fairly low-intensity task, but the period can be altered here
  // or the timer disabled by setting the value to zero.
  // By default the value is set to 0.5 x exchangeLifetime (~120s)
  if (values && (typeof(values.pruneTimerPeriod)==="number")) {
    p.pruneTimerPeriod = values.pruneTimerPeriod
  } else {
    p.pruneTimerPeriod =  (0.5 * p.exchangeLifetime)
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.polyfill"></a>[module coap.polyfill](#apidoc.module.coap.polyfill)

#### <a name="apidoc.element.coap.polyfill.compareBuffers"></a>[function <span class="apidocSignatureSpan">coap.polyfill.</span>compareBuffers (buf1, buf2)](#apidoc.element.coap.polyfill.compareBuffers)
- description and source-code
```javascript
compareBuffers = function (buf1, buf2) {
  if (Buffer.compare)
    return Buffer.compare(buf1, buf2)
  else {
    if (buf1.length != buf2.length) return -1
    for (var i = 0; i < buf1.length; i++) {
      if (buf1[i] != buf2[i]) return -1
    }
    return 0
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.retry_send"></a>[module coap.retry_send](#apidoc.module.coap.retry_send)

#### <a name="apidoc.element.coap.retry_send.retry_send"></a>[function <span class="apidocSignatureSpan">coap.</span>retry_send (sock, port, host)](#apidoc.element.coap.retry_send.retry_send)
- description and source-code
```javascript
function RetrySend(sock, port, host) {
  if (!(this instanceof RetrySend))
    return new RetrySend(port, host)

  var that    = this

  this._sock  = sock

  this._port  = port || parameters.coapPort

  this._host  = host

  this._sendAttemp = 0
  this._lastMessageId = -1
  this._currentTime = parameters.ackTimeout * (1 + (parameters.ackRandomFactor - 1) * Math.random()) * 1000

  this._bOff  = function() {
    that._currentTime = that._currentTime * 2
    that._send()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.coap.retry_send.super_"></a>[function <span class="apidocSignatureSpan">coap.retry_send.</span>super_ ()](#apidoc.element.coap.retry_send.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.coap.retry_send.prototype"></a>[module coap.retry_send.prototype](#apidoc.module.coap.retry_send.prototype)

#### <a name="apidoc.element.coap.retry_send.prototype._send"></a>[function <span class="apidocSignatureSpan">coap.retry_send.prototype.</span>_send (avoidBackoff)](#apidoc.element.coap.retry_send.prototype._send)
- description and source-code
```javascript
_send = function (avoidBackoff) {
  var that = this

  this._sock.send(this._message, 0, this._message.length,
                  this._port, this._host, function(err, bytes) {
                    that.emit('sent', err, bytes)
                    if (err) {
                      that.emit('error', err)
                    }
                  })

  var messageId = parse(this._message).messageId
  if (messageId != this._lastMessageId) {
    this._lastMessageId = messageId
    this._sendAttemp = 0
  }

  if (!avoidBackoff && ++this._sendAttemp <= parameters.maxRetransmit)
    this._bOffTimer = setTimeout(this._bOff, this._currentTime)

  this.emit('sending', this._message)
}
```
- example usage
```shell
...
  done()
}

ObserveWriteStream.prototype._doSend = function doSend(data) {
  var packet = this._packet
  packet.code = this.statusCode
  packet.payload = data
  this._send(this, packet)

  this._packet.confirmable = this._request.confirmable
  this._packet.ack = !this._request.confirmable
  delete this._packet.messageId
  delete this._packet.payload
}
...
```

#### <a name="apidoc.element.coap.retry_send.prototype.reset"></a>[function <span class="apidocSignatureSpan">coap.retry_send.prototype.</span>reset ()](#apidoc.element.coap.retry_send.prototype.reset)
- description and source-code
```javascript
reset = function () {
  clearTimeout(this._timer)
  clearTimeout(this._bOffTimer)
}
```
- example usage
```shell
...
them by adding a 'req.setOption('Block2', new Buffer([0x2]))' to the
output of [request](#request).

See the
[spec](http://tools.ietf.org/html/draft-ietf-core-coap-18#section-5.4)
for all the possible options.

#### message.reset()
Returns a Reset COAP Message to the sender. The RST message will appear as an empty message with code '0.00' and the
reset flag set to 'true' to the caller. This action ends the interaction with the caller.

#### message.writeHead(code, headers)
Functions somewhat like 'http''s 'writeHead()' function.  If 'code' is does not match the CoAP code mask of '#.##', it is coerced
 into this mask.  'headers' is an object with keys being the header names, and values being the header values.

-------------------------------------------------------
...
```

#### <a name="apidoc.element.coap.retry_send.prototype.send"></a>[function <span class="apidocSignatureSpan">coap.retry_send.prototype.</span>send (message, avoidBackoff)](#apidoc.element.coap.retry_send.prototype.send)
- description and source-code
```javascript
send = function (message, avoidBackoff) {
  var that = this
    , timeout

  this._message = message
  this._send(avoidBackoff)

  timeout = avoidBackoff ? parameters.maxRTT : parameters.exchangeLifetime
  this._timer = setTimeout(function() {
    var err  = new Error('No reply in ' + timeout + 's')
    err.retransmitTimeout = timeout;
    if (!avoidBackoff)
      that.emit('error', err)
    that.emit('timeout', err)
  }, timeout * 1000)
}
```
- example usage
```shell
...
}

util.inherits(RetrySend, EventEmitter)

RetrySend.prototype._send = function(avoidBackoff) {
var that = this

this._sock.send(this._message, 0, this._message.length,
                this._port, this._host, function(err, bytes) {
                  that.emit('sent', err, bytes)
                  if (err) {
                    that.emit('error', err)
                  }
                })
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
