[![license](https://img.shields.io/github/license/micro-os-plus/template-xpack)](https://github.com/micro-os-plus/template-xpack/blob/xpack/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/micro-os-plus/template-xpack.svg)](https://github.com/micro-os-plus/template-xpack/issues)
[![GitHub pulls](https://img.shields.io/github/issues-pr/micro-os-plus/template-xpack.svg)](https://github.com/micro-os-plus/template-xpack/pulls)

# Maintainer info

## Project repository

The project is hosted on GitHub:

- https://github.com/micro-os-plus/template-xpack.git

To clone it:

```
git clone https://github.com/micro-os-plus/template-xpack.git template-xpack.git
```

## Prerequisites

A recent [xpm](https://xpack.github.io/xpm/), which is a portable
[Node.js](https://nodejs.org/) command line application.

## Publish to npmjs.com

- select the `develop` branch
- commit all changes
- update `CHANGELOG.md`; commit with a message like _CHANGELOG: prepare v0.1.2_
- `npm pack` and check the content of the archive; possibly adjust `.npmignore`
- `npm version patch`, `npm version minor`, `npm version major`
- push the develop branch to GitHub
- `npm publish --tag next` (use `--access public` when publishing for
  the first time)

The version is visible at:

- https://www.npmjs.com/package/@micro-os-plus/template?activeTab=versions

## Test

Test the package.

## Update the repo

When the package is considered stable:

- with Sourcetree
- merge `develop` into `xpack`
- push to GitHub

## Tag the npm package as `latest`

When the release is considered stable, promote it as `latest`:

- `npm dist-tag ls @micro-os-plus/template`
- `npm dist-tag add @micro-os-plus/template@1.2.3 latest`
- `npm dist-tag ls @xpack-dev-tools/template`

## Announce to the community

Post an announcement to the forum or on Twitter.
