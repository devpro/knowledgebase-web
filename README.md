# Knowledge Base

[![CircleCI](https://circleci.com/gh/devpro/knowledgebase-web.svg?style=svg)](https://circleci.com/gh/devpro/knowledgebase-web)

This is the source code of the website [knowledge-base-bertrand-thomas.cfapps.io](https://knowledge-base-bertrand-thomas.cfapps.io/).

## Contribute

You are more than welcome to create pull requests to update the source code.

This website is based on [Hugo](https://gohugo.io/).

### Prerequisite

The following tools are needed:

- [Git client](https://git-scm.com/downloads)
- [Hugo client](https://gohugo.io/getting-started/installing)

### Local run

To have the website running locally, with automatic reload, follow the steps:

- Get the source code through `git clone --recurse-submodules`
- Run locally with `hugo server -D`

### Add content

- Create a new page with the command `hugo new path/to/new/file.md`
- Look at [fontawesome.com](https://fontawesome.com/icons?d=gallery) for ideas of menu icons

### Known issues

- If Git is saying one theme submodule is in dirty state run `git submodule foreach --recursive git checkout .` (see [the discussion on stackoverflow](https://stackoverflow.com/questions/4873980/git-diff-says-subproject-is-dirty))
- Folders starting with a dot (".") will not be served by nginx (available from static folders for instance)

## Deploy

### Hosting

The website [knowledge-base-bertrand-thomas.cfapps.io](https://knowledge-base-bertrand-thomas.cfapps.io/) is running on [Pivotal Web Service PWS](https://run.pivotal.io/).

### Deployment procedure

- Create the static content by running `HUGO_ENV=production hugo` (only not draft posts will be published!)
- Deploy very easily through Cloud Foundry CLI by running `cf push` (once logged in with `cf login -a "https://api.run.pivotal.io" -u "myusername" -p "mypassword" -o "myorg" -s "myspace"`)
- You can look at what is deployed with `cf ssh` (see [docs.cloudfoundry.org](https://docs.cloudfoundry.org/devguide/deploy-apps/ssh-apps.html))
