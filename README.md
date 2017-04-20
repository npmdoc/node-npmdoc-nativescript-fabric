# npmdoc-nativescript-fabric

#### api documentation for  nativescript-fabric (v0.3.1)  [![npm package](https://img.shields.io/npm/v/npmdoc-nativescript-fabric.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nativescript-fabric) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nativescript-fabric.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nativescript-fabric)

#### A NativeScript Plugin for fabric.io

[![NPM](https://nodei.co/npm/nativescript-fabric.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/nativescript-fabric)

- [https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "nativescript-fabric",
    "version": "0.3.1",
    "description": "A NativeScript Plugin for fabric.io",
    "scripts": {
        "preclean": "npm i rimraf",
        "clean": "rimraf node_modules target",
        "postclean": "npm i",
        "build": "tsc",
        "test": "npm run build",
        "pree2e": "cd test/e2e && npm i && npm i ../.. && tns prepare ios && tns prepare android",
        "e2e": "npm run e2e:ios && npm run e2e:android",
        "e2e:ios": "cd test/e2e && tns test ios --emulator --justlaunch",
        "e2e:android": "cd test/e2e && tns test android --emulator --justlaunch",
        "postinstall": "node postinstall.js",
        "preuninstall": "node preuninstall.js",
        "changelog": "conventional-changelog -p angular -i CHANGELOG.md -s -r 0",
        "changelog:add": "git add CHANGELOG.md && git commit -m 'updated CHANGELOG.md'",
        "release:pre": "npm run clean && npm run test",
        "release:post": "npm run changelog && npm run changelog:add",
        "release:major": "npm run release:pre && npm version major && npm run release:post && git push origin && git push origin --tags && npm run version-and-push",
        "release:minor": "npm run release:pre && npm version minor && npm run release:post && git push origin && git push origin --tags && npm run version-and-push",
        "release:patch": "npm run release:pre && npm version patch && npm run release:post && git push origin && git push origin --tags && npm run version-and-push",
        "version-and-push": "git push origin && git push origin --tags && npm run publish-and-merge",
        "publish-and-merge": "git checkout master && git merge develop && git push && git checkout develop && npm publish",
        "prepublish": "npm run build"
    },
    "main": "fabric",
    "typings": "index.d.ts",
    "dependencies": {
        "format": "0.2.2",
        "fs-extra": "2.1.2",
        "nativescript-hook": "^0.2.1",
        "simple-plist": "0.2.1",
        "xcode": "0.9.1",
        "xmldom": "0.1.22"
    },
    "peerDependencies": {},
    "devDependencies": {
        "@types/fs-extra": "2.0.0",
        "@types/jasmine": "2.5.47",
        "conventional-changelog-cli": "1.3.1",
        "plist": "1.2.0",
        "rimraf": "2.6.1",
        "tns-core-modules": "2.5.2",
        "tns-platform-declarations": "2.5.2",
        "typescript": "2.2.2"
    },
    "nativescript": {
        "platforms": {
            "android": "2.3.0",
            "ios": "2.3.0"
        },
        "hooks": [
            {
                "type": "after-prepare",
                "script": "lib/after-prepare.js",
                "inject": true
            }
        ]
    },
    "keywords": [
        "fabric",
        "crashlytics",
        "Android"
    ],
    "author": "Martin Reinhardt <contact@martinreinhardt-online.de> (https://github.com/hypery2k)",
    "repository": {
        "type": "git",
        "url": "https://github.com/hypery2k/nativescript-fabric.git"
    },
    "bugs": {
        "url": "https://github.com/hypery2k/nativescript-fabric/issues"
    },
    "license": "MIT"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
