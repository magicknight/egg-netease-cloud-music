# egg-netease-cloud-music

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][codecov-image]][codecov-url]
[![David deps][david-image]][david-url]
[![Known Vulnerabilities][snyk-image]][snyk-url]
[![npm download][download-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/egg-netease-cloud-music.svg?style=flat-square
[npm-url]: https://npmjs.org/package/egg-netease-cloud-music
[travis-image]: https://img.shields.io/travis/eggjs/egg-netease-cloud-music.svg?style=flat-square
[travis-url]: https://travis-ci.org/eggjs/egg-netease-cloud-music
[codecov-image]: https://img.shields.io/codecov/c/github/eggjs/egg-netease-cloud-music.svg?style=flat-square
[codecov-url]: https://codecov.io/github/eggjs/egg-netease-cloud-music?branch=master
[david-image]: https://img.shields.io/david/eggjs/egg-netease-cloud-music.svg?style=flat-square
[david-url]: https://david-dm.org/eggjs/egg-netease-cloud-music
[snyk-image]: https://snyk.io/test/npm/egg-netease-cloud-music/badge.svg?style=flat-square
[snyk-url]: https://snyk.io/test/npm/egg-netease-cloud-music
[download-image]: https://img.shields.io/npm/dm/egg-netease-cloud-music.svg?style=flat-square
[download-url]: https://npmjs.org/package/egg-netease-cloud-music

<!--
Description here.
-->
egg for [neteaseCloudMusicApi](https://github.com/Binaryify/NeteaseCloudMusicApi)

## Install
1. build a server with [neteaseCloudMusicApi](https://github.com/Binaryify/NeteaseCloudMusicApi)

2. install this plugin
```bash
$ npm i egg-netease-cloud-music --save
```

## Usage

```js
// {app_root}/config/plugin.js
exports.neteaseCloudMusic = {
  enable: true,
  package: 'egg-netease-cloud-music',
};
```

## Configuration

```js
// {app_root}/config/config.default.js
exports.neteaseCloudMusic = {
};
```

see [config/config.default.js](config/config.default.js) for more detail.

## Example

```js
// search music by keyword
const musicList = await this.app.neteaseCloudMusic.searchMusic('天使的翅膀')

// get music url by netease id
const musicUrl = await this.app.neteaseCloudMusic.getMusicUrl(27747330)

// download music to local location
const musicDownload = await this.app.neteaseCloudMusic.downloadMusic(27747330, '/test.mp3')
```

## Questions & Suggestions

Please open an issue [here](https://github.com/eggjs/egg/issues).

## License

[MIT](LICENSE)
