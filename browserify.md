# Browserify guide

To build this library for browser you should install following dependencies:

```
npm install -g uglify-es browserify
```

After that clone and install library from this repository.

```
git clone https://github.com/volbil/bitcoinjs-lib.git
cd bitcoinjs-lib
npm install
```

And once everything is ready, do the magic :D

```
browserify -r . --standalone bitcoin | uglifyjs -c --mangle reserved=['BigInteger','ECPair','Point'] -o bitcoinjs.min.js
```

Based on this [discussion](https://github.com/bitcoinjs/bitcoinjs-lib/issues/965).
