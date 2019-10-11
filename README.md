# Weixin Jssdk

[![NPM version][npm-image]][npm-url]
[![David deps][david-image]][david-url]
[![devDependencies Status][david-dev-image]][david-dev-url]
[![npm download][download-image]][download-url]
[![npm license][license-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/weixinjssdk.svg?style=flat-square
[npm-url]: https://npmjs.org/package/weixinjssdk
[david-image]: https://img.shields.io/david/cycdpo/weixinjssdk.svg?style=flat-square
[david-url]: https://david-dm.org/cycdpo/weixinjssdk
[david-dev-image]: https://david-dm.org/cycdpo/weixinjssdk/dev-status.svg?style=flat-square
[david-dev-url]: https://david-dm.org/cycdpo/weixinjssdk?type=dev
[download-image]: https://img.shields.io/npm/dm/weixinjssdk.svg?style=flat-square
[download-url]: https://npmjs.org/package/weixinjssdk
[license-image]: https://img.shields.io/npm/l/weixinjssdk.svg?style=flat-square

## This package has been deprecated
[new-url]: https://github.com/cycjimmy/weixin-jssdk

**This package has been migrated to [@cycjimmy/weixin-jssdk][new-url] for scoped NPM package. Please switch to [@cycjimmy/weixin-jssdk][new-url] to stay up to date.**

## Install
```shell
# via npm
$ npm install weixinjssdk --save

# or via yarn
$ yarn add weixinjssdk
```

## Use
```javascript
const WxJssdk = require('weixinjssdk');

const wxJssdk = new WxJssdk()
  .setWxConfig({
    appid: 'your appid',
    secret: 'your secret',
  })
  [.setHook({
    getAccessTokenSuccess: new Promise...,
    getAccessTokenFromCustom: new Promise...,
  })];

wxJssdk.wxshare({
   url: 'whole url'
})
.then(data => {
  // Do something
  // ...
});
```

## More
* `wxJssdk.setHook`: [Object] Set Hook Functions.
  * `getAccessTokenSuccess`: [Promise] Run Hook when get Access_Token success. Please resolve Access_Token.
  * `getAccessTokenFromCustom`: [Promise] Run custom task Before get Access_Token from wechat. Please resolve Access_Token.

