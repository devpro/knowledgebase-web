# Knowledge Base

## Contribute

This website has been built thanks to [Hugo](https://gohugo.io/).

### Prerequisite

- [Git client](https://git-scm.com/downloads)
- [Hugo client](https://gohugo.io/getting-started/installing)

### Local run

- Get the source code through `git clone --recurse-submodules`
- Run locally with `hugo server -D`

### Known issues

- If Git is saying one theme submodule is in dirty state run `git submodule foreach --recursive git checkout .` (see [the discussion on stackoverflow](https://stackoverflow.com/questions/4873980/git-diff-says-subproject-is-dirty))

## Deploy

The website [knowledge-base-bertrand-thomas.cfapps.io](https://knowledge-base-bertrand-thomas.cfapps.io/) is hosted freely by [Pivotal Web Service PWS](https://run.pivotal.io/).

### Deployment procedure

- Create the static content by running `HUGO_ENV=production hugo` (only not draft posts will be published!)
- Deploy very easily through Cloud Foundry CLI by running `cf push`
