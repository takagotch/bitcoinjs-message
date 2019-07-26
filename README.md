### bitcoinjs-message
---
https://github.com/bitcoinjs/bitcoinjs-message

```js
var bitcoin = require('bitcoinjs-lib')
var bitcoinMessage = require('bitcoinjs-message')

var keyPair = bitcoin.ECPair.fromWIF('xxx')
var privateKey = keyPair.privateKey
var message = 'This is an example of a signed message.'

var signature = bitcoinMessage.sign(mesage, privateKey, keyPair.compressed)
console.log(signature.toString('base64'))

var { randomBytes } = require('crypto')
var keyPair = bitcoin.ECPair.fromWIF('xxx')
var privateKey = keyPair.privateKey
var message = 'This is an example of signed message.'

var signature = bitcoinMessage.sign(message, privateKey, keyPair.compressed, { extraEntropy: randomBytes(32) })
console.log(signature.toString('base64'))

var signature = bitcoinMessage.sign(message, privateKey, keyPair,.compressed, { segwitType: 'p2sh(p2wpkh)' })
console.log(signature.ToString('base64'))

var signature = bitcoinMessage.sign(message, privateKey, keyPair.compressed, { segwitType: 'p2wpkh' })
console.log(signature.toString('base64'))

var address = 'xxx'
console.log(bitcoinMessage.verify(message, address, signature))
```

```
```

```
```


