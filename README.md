nedb-lite
==============
standalone, single-script version of [nedb](https://www.npmjs.com/package/nedb) that runs in both browser and nodejs, with zero npm-dependencies

[![NPM](https://img.shields.io/npm/v/nedb-lite.svg?style=flat-square)](https://www.npmjs.com/package/nedb-lite) [![NPM](https://img.shields.io/npm/dm/nedb-lite.svg?style=flat-square)](https://www.npmjs.com/package/nedb-lite)



# todo
- none



# change since efb3057b
- npm publish 2016.1.2
- add cdn file-download link
- add nodejs win32 support
- add simple github test-server
- rename index.js to nedb-lite.js
- none



# cdn download
- [http://kaizhu256.github.io/node-nedb-lite/build/app/nedb-lite.js](http://kaizhu256.github.io/node-nedb-lite/build/app/nedb-lite.js)
- [http://kaizhu256.github.io/node-nedb-lite/build/app/nedb-lite.min.js](http://kaizhu256.github.io/node-nedb-lite/build/app/nedb-lite.min.js)

[![github.com cdn-download](https://kaizhu256.github.io/node-nedb-lite/build/screen-capture.githubDeploy.browser._2Fnode-nedb-lite_2Fbuild..alpha..travis-ci.org_2Fapp_2Fnedb-lite.js.png)](http://kaizhu256.github.io/node-nedb-lite/build/app/nedb-lite.js)



# build-status [![travis-ci.org build-status](https://api.travis-ci.org/kaizhu256/node-nedb-lite.svg)](https://travis-ci.org/kaizhu256/node-nedb-lite)
[![build commit status](https://kaizhu256.github.io/node-nedb-lite/build/build.badge.svg)](https://travis-ci.org/kaizhu256/node-nedb-lite)

| git-branch : | [master](https://github.com/kaizhu256/node-nedb-lite/tree/master) | [beta](https://github.com/kaizhu256/node-nedb-lite/tree/beta) | [alpha](https://github.com/kaizhu256/node-nedb-lite/tree/alpha)|
|--:|:--|:--|:--|
| test-server : | [![github.com test-server](https://kaizhu256.github.io/node-nedb-lite/GitHub-Mark-32px.png)](https://kaizhu256.github.io/node-nedb-lite/build..master..travis-ci.org/app/index.html) | [![github.com test-server](https://kaizhu256.github.io/node-nedb-lite/GitHub-Mark-32px.png)](https://kaizhu256.github.io/node-nedb-lite/build..beta..travis-ci.org/app/index.html) | [![github.com test-server](https://kaizhu256.github.io/node-nedb-lite/GitHub-Mark-32px.png)](https://kaizhu256.github.io/node-nedb-lite/build..alpha..travis-ci.org/app/index.html)|
| build-artifacts : | [![build-artifacts](https://kaizhu256.github.io/node-nedb-lite/glyphicons_144_folder_open.png)](https://github.com/kaizhu256/node-nedb-lite/tree/gh-pages/build..master..travis-ci.org) | [![build-artifacts](https://kaizhu256.github.io/node-nedb-lite/glyphicons_144_folder_open.png)](https://github.com/kaizhu256/node-nedb-lite/tree/gh-pages/build..beta..travis-ci.org) | [![build-artifacts](https://kaizhu256.github.io/node-nedb-lite/glyphicons_144_folder_open.png)](https://github.com/kaizhu256/node-nedb-lite/tree/gh-pages/build..alpha..travis-ci.org)|

#### master branch
- stable branch
- HEAD should be tagged, npm-published package

#### beta branch
- semi-stable branch
- HEAD should be latest, npm-published package

#### alpha branch
- unstable branch
- HEAD is arbitrary
- commit history may be rewritten



# documentation
#### this package is derived from
- [nedb @ 1.8.0](https://www.npmjs.com/package/nedb)

#### api-doc
- [https://kaizhu256.github.io/node-nedb-lite/build/doc.api.html](https://kaizhu256.github.io/node-nedb-lite/build/doc.api.html)

[![api-doc](https://kaizhu256.github.io/node-nedb-lite/build/screen-capture.docApiCreate.browser._2Fhome_2Ftravis_2Fbuild_2Fkaizhu256_2Fnode-nedb-lite_2Ftmp_2Fbuild_2Fdoc.api.html.png)](https://kaizhu256.github.io/node-nedb-lite/build/doc.api.html)



# npm-dependencies
- none



# package-listing
[![screen-capture](https://kaizhu256.github.io/node-nedb-lite/build/screen-capture.gitLsTree.svg)](https://github.com/kaizhu256/node-nedb-lite)



# package.json
```json
{
    "author": "kai zhu <kaizhu256@gmail.com>",
    "description": "standalone, single-script version of nedb \
that runs in both browser and nodejs, with zero npm-dependencies",
    "devDependencies": {
        "electron-lite": "2015.12.4",
        "utility2": "2016.1.5"
    },
    "engines": { "node": ">=4.2" },
    "keywords": [
        "browser",
        "db",
        "embed", "embedded",
        "lite", "lightweight",
        "minimal", "mongo", "mongodb",
        "nedb",
        "standalone"
    ],
    "license": "MIT",
    "main": "nedb-lite.js",
    "name": "nedb-lite",
    "os": ["darwin", "linux"],
    "repository": {
        "type": "git",
        "url": "https://github.com/kaizhu256/node-nedb-lite.git"
    },
    "scripts": {
        "build-ci": "utility2 shRun shReadmeBuild",
        "build-doc": "MODE_LINENO=0 \
utility2 shRun shReadmeExportFile package.json package.json && \
utility2 shRun shDocApiCreate \"module.exports={ \
exampleFileList:['README.md','test.js','nedb-lite.js'], \
moduleDict:{ \
Nedb:{exports:require('./nedb-lite.js')}, \
'Nedb.prototype':{aliasList:['collection'], \
exports:require('./nedb-lite.js').prototype} \
} \
}\"",
        "test": "export MODE_LINENO=0 && \
export NODE_ENV=test && \
utility2 shRun shReadmeExportFile package.json package.json && \
export PORT=$(utility2 shServerPortRandom) && \
utility2 test node test.js"
    },
    "version": "2016.1.2"
}
```



# changelog of last 50 commits
[![screen-capture](https://kaizhu256.github.io/node-nedb-lite/build/screen-capture.gitLog.svg)](https://github.com/kaizhu256/node-nedb-lite/commits)



# internal build-script
- build.sh

```shell
# build.sh

# this shell script will run the build for this package

shBuild() {(set -e
# this function will run the main build
    # init env
    . node_modules/.bin/utility2 && shInit

    (set -e
    # run npm-test on published package
    (export npm_config_mode_coverage=1 &&
        shNpmTestPublished)

    # run npm-test
    (export MODE_BUILD=npmTest &&
        shRunScreenCapture npm test --mode-coverage)

    # create api-doc
    npm run-script build-doc

    # if running legacy-node, then do not continue
    [ "$(node --version)" \< "v5.0" ] && exit || true

    if [ "$CI_BRANCH" = alpha ] ||
        [ "$CI_BRANCH" = beta ] ||
        [ "$CI_BRANCH" = master ]
    then
        TEST_URL="https://$(printf "$GITHUB_REPO" | \
            sed 's/\//.github.io\//')/build..$CI_BRANCH..travis-ci.org/app/nedb-lite.js"
        # deploy app to gh-pages
        (export npm_config_file_test_report_merge="$npm_config_dir_build/test-report.json" &&
            shGithubDeploy)
    fi
    )

    # save exit-code
    EXIT_CODE=$?

    # create package-listing
    (export MODE_BUILD=gitLsTree &&
        shRunScreenCapture shGitLsTree)

    # create recent changelog of last 50 commits
    (export MODE_BUILD=gitLog &&
        shRunScreenCapture git log -50 --pretty="%ai\u000a%B")

    # if running legacy-node, then do not continue
    [ "$(node --version)" \< "v5.0" ] && exit || true

    # cleanup remote build dir
    # export BUILD_GITHUB_UPLOAD_PRE_SH="rm -fr build"

    # upload build-artifacts to github, and if number of commits > 16, then squash older commits
    (export COMMIT_LIMIT=16 &&
        export MODE_BUILD=githubUpload &&
        shBuildGithubUpload)

    # exit exit-code
    exit "$EXIT_CODE"
)}
shBuild
```
