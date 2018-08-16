# Bitcoin Cash Message Verification and Signing for Bitcore

@bookmoons/bitcore-message-cash adds support for verifying and signing bitcoin cash messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore repo](https://github.com/bitpay/bitcore) for more information.

## Getting Started

```sh
npm install @bookmoons/bitcore-message-cash
```

```sh
bower install @bookmoons/bitcore-message-cash
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-cash');
var Message = require('@bookmoons/bitcore-message-cash');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).
