# Personal site

Automatically built by Travis-CI [![Build Status](https://travis-ci.org/caesar0301/caesar0301.github.io.svg?branch=site-source)](https://travis-ci.org/caesar0301/caesar0301.github.io)

## Build
We perform manully building due to [error of hexo plugin](https://travis-ci.org/github/caesar0301/caesar0301.github.io/builds/730526132).

```bash
# Dependencies
git clone https://github.com/klugjo/hexo-theme-alpha-dust themes/alpha-dust
cp themes/alpha-dust_config.yml themes/alpha-dust/_config.yml
npm install
# Generate posts
npm run generate
# Deploy to master
npm run deploy
```