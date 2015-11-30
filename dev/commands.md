00 Install npm

´´´
$ npm install npm -g
´´´

01 Dev Environment

´´´
$ mkdir dev && cd dev
´´´

02 Login

´´´
$ npm whoami

$ npm adduser
´´´

03 Start A Project

´´´
$ npm init --scope=ackuser

´´´

04 Install A Module && 05 Listing Dependencies

´´´
$ npm install @linclark/pkg --save
´´´

06 npm Test

´´´
$ nano test.js

adding in package.json

"scripts": {
  "test": "node test.js"
},
´´´

07 Package Niceties

´´´
$ cp ../README.md .
edit with few words
´´´

08 Publish

´´´
$ npm publish
´´´

09 Version

Example

    1.2.3
    ^ ^ ^
    | | `-- Patch version. Update for every change.
    | `---- Minor version. Update for API additions.
    `------ Major version. Update for breaking API changes.

´´´
$ npm version
´´´

exit ->

{ '@ackuser/dev': '1.0.0',
  npm: '3.5.0',
  http_parser: '2.3',
  modules: '14',
  node: '0.12.7',
  openssl: '1.0.1p',
  uv: '1.6.1',
  v8: '3.28.71.19',
  zlib: '1.2.8' }

´´´
$ npm version 1.1.1
´´´

10 Publish Again

´´´
$ npm version 1.1.2

$ npm publish
´´´

+ @ackuser/dev@1.1.2

11 Dist Tag

´´´
$ npm dist-tag add @ackuser/dev@1.0.0 test

$ npm dist-tag add @ackuser/dev@1.1.2 latest
´´´

12 Dist Tag Removal

´´´
$ npm dist-tag add @ackuser/dev@1.1.2 stable

$ npm dist-tag add @ackuser/dev@1.1.4 latest

$ npm dist-tag ls

$ npm dist-tag rm @ackuser/dev stable
-stable: @ackuser/dev@1.1.2

$ npm dist-tag rm @ackuser/dev test
-test: @ackuser/dev@1.0.0

$ npm dist-tag ls
´´´

13 Outdated

´´´
$ npm dist-tag ls

$ how-to-npm verify @linclark/pkg
´´´

14 Update

´´´
$ npm update
´´´

15 Rm

´´´
npm rm @linclark/pkg --save
´´´

16 Finale

´´´
how-to-npm verify
´´´
