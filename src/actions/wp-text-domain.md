---
path: '/wp-text-domain'
title: 'WP Text Domain - Github Action'
github_url: 'https://github.com/wpapps/wp-text-domain'
author: 'Varun Sridharan'
tags: ['wordpress']
subtitle: 'Add Text Domain To Your WordPress Plugin / Themes On The Fly'
---

<p align="center">
<img src="https://user-images.githubusercontent.com/1039236/51209809-253a8a80-1937-11e9-9dc1-0267bcb74390.png" />
</p>

<p align="center">
<a href="https://github.com/wpapps/wp-text-domain"><img src="https://img.shields.io/github/license/wpapps/wp-text-domain.svg" alt="Licence"></a>
<a href="https://github.com/wpapps/wp-text-domain"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs"></a>
</p>

# WP Text Domain - ***Github Action***
This Action Adds TextDomain To your wordpress Plugin / Theme based on the content inside Github Repo

## Configuration
* `DOMAIN` - Slug of your WordPress Theme / Plugin Slug  **Required**
* `GITHUB_TOKEN` - you do not need to generate one but you do have to explicitly make it available to the Action

## Example Workflow File
```
workflow "Deploy" {
resolves = ["WP Text Domain"]
on = "push"
}

action "WP Text Domain" {
uses = "wpapps/wp-text-domain@master"
env = {
DOMAIN = "your-textdomain"
}
secrets = ["GITHUB_TOKEN"]
}
```
