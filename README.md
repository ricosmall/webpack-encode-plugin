# Webpack Encode Plugin

A useful plugin to encode your file to another encoding from the one of your source code.

## Usage

1. Install

```bash
npm install -save-dev webpack-encode-plugin
```

2. Example

```javascript
var EncodePlugin = require('webpack-encode-plugin')

module.exports = {
    ...
    plugins: [
        ...
        new EncodePlugin({
            encoding: 'gbk'
        })
    ]
}
```

if you want to encode your file to `UTF-* with BOM`, you can setting like below:

```javascript
var EncodePlugin = require('webpack-encode-plugin')

module.exports = {
    ...
    plugins: [
        ...
        new EncodePlugin({
            encoding: 'utf-8',
            config: {
                addBOM: true
            }
        })
    ]
}
```

3. Others

The encoding module is [iconv-lite](https://github.com/ashtuchkin/iconv-lite), here is [supported Content-type list](https://github.com/ashtuchkin/iconv-lite/wiki/Supported-Encodings).
