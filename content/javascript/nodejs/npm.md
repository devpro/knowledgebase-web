---
title: "NPM"
date: 2019-09-23T22:53:44+02:00
draft: false
---

[npmjs.com](https://www.npmjs.com/)

## Install & update

```bash
npm cache clean -f
npm install -g npm
npm -v
npm update -g
```

## Configuration

- List registries: `npm config list registry`
- Reset to the default registry: `npm config set registry https://registry.npmjs.org/`
- See peer dependencies: `npm view tsickle@0.34.3 peerDependencies`

### Working with MyGet

- [MyGet NPM support](https://docs.myget.org/docs/reference/myget-npm-support)
- Add another registry on MyGet: `npm config set @mycompany:registry https://www.myget.org/F/mycompany/npm/`
  - `npm install @mycopmpany/mypackage@1.0.1`
- Or add directly the zip url:

```json
{
  "dependencies": {
    "mypackage": "https://www.myget.org/F/mycompany/npm/mypackage/-/mypackage-1.0.0.tgz"
  }
}
```
