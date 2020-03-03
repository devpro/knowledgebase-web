---
title: "Artifacts"
date: 2020-03-03T18:37:46+01:00
draft: false 
---

## Recipes

### Permissions

By default, it won't work, you need to click on "..." in the permission pane of your feed and click on "Allow project-scoped builds".

[Secure and share packages using feed permissions](https://docs.microsoft.com/en-us/azure/devops/artifacts/feeds/feed-permissions)

### Yaml

[Publish to NuGet feeds](https://docs.microsoft.com/en-us/azure/devops/pipelines/artifacts/nuget)

```yaml
- task: NuGetAuthenticate@0
  displayName: 'Authenticate to NuGet feed'
- task: NuGetCommand@2
  displayName: 'Push NuGet packages'
  inputs:
    command: 'push'
    packagesToPush: '$(Build.ArtifactStagingDirectory)/**/*.nupkg;!$(Build.ArtifactStagingDirectory)/**/*.symbols.nupkg'
    nuGetFeedType: 'internal'
    publishVstsFeed: $(azure.artifact.feed.id)
    allowPackageConflicts: true
```
