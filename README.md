## Tinker
[![license](http://img.shields.io/badge/license-BSD3-brightgreen.svg?style=flat)](https://github.com/Tencent/tinker/blob/master/LICENSE)
[![Release Version](https://img.shields.io/badge/release-1.9.14.23-red.svg)](https://github.com/Tencent/tinker/releases)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Tencent/tinker/pulls)
[![WeChat Approved](https://img.shields.io/badge/Wechat_Approved-1.9.14.23-red.svg)](https://github.com/Tencent/tinker/wiki)

[中文说明](https://github.com/Tencent/tinker/wiki)

Tinker is a hot-fix solution library for Android, it supports dex, library and resources update without reinstalling apk.

![tinker.png](assets/tinker.png)

## Why this fork exists
Currently tinker doesn't work if "core library desugaring" is enabled because it checks if all classes used by tinker's classloader are in the app's main dex.

the core library desugaring puts all the backported classes in a separate dex file and this prevents tinker from working normally, this fork solves this problem.
