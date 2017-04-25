# npmdoc-nativescript-fabric

#### basic api documentation for  [nativescript-fabric (v0.3.1)](https://github.com/hypery2k/nativescript-fabric#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-nativescript-fabric.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nativescript-fabric) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nativescript-fabric.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nativescript-fabric)

#### A NativeScript Plugin for fabric.io

[![NPM](https://nodei.co/npm/nativescript-fabric.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/nativescript-fabric)

- [https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nativescript-fabric/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Martin Reinhardt",
        "url": "https://github.com/hypery2k"
    },
    "bugs": {
        "url": "https://github.com/hypery2k/nativescript-fabric/issues"
    },
    "dependencies": {
        "format": "0.2.2",
        "fs-extra": "2.1.2",
        "nativescript-hook": "^0.2.1",
        "simple-plist": "0.2.1",
        "xcode": "0.9.1",
        "xmldom": "0.1.22"
    },
    "description": "A NativeScript Plugin for fabric.io",
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
    "directories": {},
    "dist": {
        "shasum": "343740db5fd201845731a53bb704379827f99256",
        "tarball": "https://registry.npmjs.org/nativescript-fabric/-/nativescript-fabric-0.3.1.tgz"
    },
    "gitHead": "7b66413aef772e39e8f326963795b92138690870",
    "homepage": "https://github.com/hypery2k/nativescript-fabric#readme",
    "keywords": [
        "fabric",
        "crashlytics",
        "Android"
    ],
    "license": "MIT",
    "main": "fabric",
    "maintainers": [
        {
            "name": "hypery2k"
        }
    ],
    "name": "nativescript-fabric",
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
    "optionalDependencies": {},
    "peerDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/hypery2k/nativescript-fabric.git"
    },
    "scripts": {
        "build": "tsc",
        "changelog": "conventional-changelog -p angular -i CHANGELOG.md -s -r 0",
        "changelog:add": "git add CHANGELOG.md && git commit -m 'updated CHANGELOG.md'",
        "clean": "rimraf node_modules target",
        "e2e": "npm run e2e:ios && npm run e2e:android",
        "e2e:android": "cd test/e2e && tns test android --emulator --justlaunch",
        "e2e:ios": "cd test/e2e && tns test ios --emulator --justlaunch",
        "postclean": "npm i",
        "postinstall": "node postinstall.js",
        "preclean": "npm i rimraf",
        "pree2e": "cd test/e2e && npm i && npm i ../.. && tns prepare ios && tns prepare android",
        "prepublish": "npm run build",
        "preuninstall": "node preuninstall.js",
        "publish-and-merge": "git checkout master && git merge develop && git push && git checkout develop && npm publish",
        "release:major": "npm run release:pre && npm version major && npm run release:post && git push origin && git push origin --tags && npm run version-and-push",
        "release:minor": "npm run release:pre && npm version minor && npm run release:post && git push origin && git push origin --tags && npm run version-and-push",
        "release:patch": "npm run release:pre && npm version patch && npm run release:post && git push origin && git push origin --tags && npm run version-and-push",
        "release:post": "npm run changelog && npm run changelog:add",
        "release:pre": "npm run clean && npm run test",
        "test": "npm run build",
        "version-and-push": "git push origin && git push origin --tags && npm run publish-and-merge"
    },
    "typings": "index.d.ts",
    "version": "0.3.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
