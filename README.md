# Kira Dependencies Bot

[![wemake.services](https://img.shields.io/badge/%20-wemake.services-green.svg?label=%20&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAMAAAAoLQ9TAAAABGdBTUEAALGPC%2FxhBQAAAAFzUkdCAK7OHOkAAAAbUExURQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAP%2F%2F%2F5TvxDIAAAAIdFJOUwAjRA8xXANAL%2Bv0SAAAADNJREFUGNNjYCAIOJjRBdBFWMkVQeGzcHAwksJnAPPZGOGAASzPzAEHEGVsLExQwE7YswCb7AFZSF3bbAAAAABJRU5ErkJggg%3D%3D)](https://wemake.services)
[![kira-family](https://img.shields.io/badge/kira-family-pink.svg)](https://github.com/wemake-services/kira)

Gitlab bot to continuously update your dependency versions.
Friendly fork of [`dependabot-script`](https://github.com/dependabot/dependabot-script).
The main difference is that the script's source is adjusted to work with [`RSDP`](https://wemake.services/meta/rsdp) process.

Part of the [`@kira`](https://github.com/wemake-services/kira) bots family.

## Installation

We recommend to copy this project to your Gitlab.
And then setup individual CI schedules
for each project that you want to enable.

## Configuration

### Global

This is a global configuration that you should setup inside your CI variables.

- `KIRA_GITLAB_PERSONAL_TOKEN` - personal access token for your bot user
- `GITLAB_HOSTNAME` - (optional) Gitlab domain name, defaults to `gitlab.com`

### Per schedule

This configuration is best to be setup inside CI schedule's environment.

- `DEPENDABOT_PROJECT_PATH` - project to be updated, eg: `wemake-services/kira-dependencies`
- `DEPENDABOT_PACKAGE_MANAGER_SET` - package managers to be updated, eg: `npm pip docker`
- `DEPENDABOT_ASSIGNEE_GITLAB_ID` - (optional) Gitlab user id to assign to merge requests
- `DEPENDABOT_GITLAB_APPROVE_MERGE` - (optional) setup to `true` if you want our bot to approve your merge requests
- `DEPENDABOT_GITLAB_AUTO_MERGE` - (optional) setup to `true` if you want to auto merge this request
