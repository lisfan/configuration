```json
{
  "name": "@~lisfan/logger",
  "version": "1.3.1",
  "description": "调试日志打印器",
  "main": "src/index.js",
  "scripts": {
    "pub-pre": "git pull && npm version prerelease",
    "pub-n": "npm run pub-pre && npm publish --tag nightly && npm run pub-post",
    "pub-a": "npm run pub-pre && npm publish --tag alpha && npm run pub-post",
    "pub-b": "npm run pub-pre && npm publish --tag beta && npm run pub-post",
    "pub-rc": "npm run pub-pre && npm publish --tag rc && npm run pub-post",
    "pub-s": "npm run pub-pre && npm publish --tag stable && npm run pub-post",
    "pub-x": "npm run pub-pre && npm publish --tag next && npm run pub-post",
    "pub-l": "npm run pub-pre && npm publish && npm run pub-post",
    "pub": "git pull && npm publish && npm run pub-post",
    "pub-post": "git commit -am \"chore: publish@$npm_package_version\" && git push",
    "docs": "rm -rf docs && jsdoc -c conf/jsdoc.config.json"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/lisfan/logger.git"
  },
  "keywords": [
    "log",
    "logger",
    "debug",
    "console",
    "output"
  ],
  "author": "lisfan <goolisfan@gmail.com> (https://www.npmjs.com/~lisfan)",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/lisfan/logger/issues"
  },
  "homepage": "https://github.com/lisfan/logger#readme",
  "dependencies": {
    "@~lisfan/validation": "^1.0.0"
  },
  "devDependencies": {
    "docdash": "~0.4.0",
    "jsdoc": "~3.5.5"
  }
}
```