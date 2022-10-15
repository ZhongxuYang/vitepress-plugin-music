# vitepress-plugin-music

> music player plugin for vitepress

<p align="center">
  <img src="https://img.shields.io/npm/dm/vitepress-plugin-nprogress.svg" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vitepress-plugin-music"><img src="https://img.shields.io/npm/v/vitepress-plugin-music.svg" alt="Version"></a>
  <a href="https://github.com/vuejs/vitepress-plugin-music/blob/master/LICENSE"><img src="https://img.shields.io/npm/l/vitepress-plugin-music.svg" alt="License"></a>
</p>

## Demo
<img src="./docs/static/record.gif" />

## Install
```sh
yarn add -D vitepress-plugin-music
# OR npm install -D vitepress-plugin-music
```

## Usage
```ts
// .vitepress/theme/index.ts

import DefaultTheme from "vitepress/theme"
import vitepressMusic from 'vitepress-plugin-music'
import 'vitepress-plugin-music/lib/css/index.css'

const list = [
  {
    name: 'song1',
    author: 'author1',
    file: '/mp3/***.mp3',
  },
  {
    name: 'song2',
    author: 'author2',
    file: 'https://***.***.***/song2.mp3',
  },
]

export default {
  ...DefaultTheme,
  enhanceApp: (ctx) => {
    vitepressMusic(list)
  }
}
```

Then you can use `vitepress-plugin-music` ! 🎉