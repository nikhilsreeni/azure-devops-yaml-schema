---
title: TwineAuthenticate@0 - Python twine upload authenticate v0 task
description: Authenticate for uploading Python distributions using twine. Add '-r FeedName/EndpointName --config-file $(PYPIRC_PATH)' to your twine upload command. For feeds present in this organization, use the feed name as the repository (-r). Otherwise, use the endpoint name defined in the service connection (task version 0).
ms.date: 08/10/2022
monikerRange: ">=azure-pipelines-2019"
---

# TwineAuthenticate@0 - Python twine upload authenticate v0 task

<!-- :::description::: -->
:::moniker range=">=azure-pipelines-2019.1"

<!-- :::editable-content name="description"::: -->
Authenticate for uploading Python distributions using twine. Add '-r FeedName/EndpointName --config-file $(PYPIRC_PATH)' to your twine upload command. For feeds present in this organization, use the feed name as the repository (-r). Otherwise, use the endpoint name defined in the service connection.
<!-- :::editable-content-end::: -->

:::moniker-end

:::moniker range="=azure-pipelines-2019"

<!-- :::editable-content name="description"::: -->
Authentication for uploading python distributions using twine. Please add "-r FeedName/EndpointName --config-file $(PYPIRC_PATH)" to your twine upload command. For feeds present in this organization use feed name as repository(-r) otherwise use the endpoint name defined in the service connection.
<!-- :::editable-content-end::: -->

:::moniker-end
<!-- :::description-end::: -->

<!-- :::syntax::: -->
## Syntax

:::moniker range=">=azure-pipelines-2019.1"

```yaml
# Python twine upload authenticate v0
# Authenticate for uploading Python distributions using twine. Add '-r FeedName/EndpointName --config-file $(PYPIRC_PATH)' to your twine upload command. For feeds present in this organization, use the feed name as the repository (-r). Otherwise, use the endpoint name defined in the service connection.
- task: TwineAuthenticate@0
  inputs:
  # Feeds and Authentication
    #artifactFeeds: # string. My feeds (select below). 
    #externalFeeds: # string. Feeds from external organizations. 
  # Advanced
    #publishPackageMetadata: true # boolean. Publish pipeline metadata. Default: true.
```

:::moniker-end

:::moniker range="=azure-pipelines-2019"

```yaml
# Python Twine Upload Authenticate v0
# Authentication for uploading python distributions using twine. Please add "-r FeedName/EndpointName --config-file $(PYPIRC_PATH)" to your twine upload command. For feeds present in this organization use feed name as repository(-r) otherwise use the endpoint name defined in the service connection.
- task: TwineAuthenticate@0
  inputs:
  # Feeds and Authentication
    #artifactFeeds: # string. My feeds (select below). 
    #externalFeeds: # string. Feeds from external organizations.
```

:::moniker-end
<!-- :::syntax-end::: -->

<!-- :::inputs::: -->
## Inputs

<!-- :::item name="artifactFeeds"::: -->
:::moniker range=">=azure-pipelines-2019"

**`artifactFeeds`** - **My feeds (select below)**<br>
Input alias: `feedList`. Type: string.<br>
<!-- :::editable-content name="helpMarkDown"::: -->
Select feeds to authenticate present in this organization.
<!-- :::editable-content-end::: -->

:::moniker-end
<!-- :::item-end::: -->
<!-- :::item name="externalFeeds"::: -->
:::moniker range=">=azure-pipelines-2019"

**`externalFeeds`** - **Feeds from external organizations**<br>
Input alias: `externalSources`. Type: string.<br>
<!-- :::editable-content name="helpMarkDown"::: -->
Select endpoints to authenticate outside this organization. Make sure the endpoints have package upload permissions.
<!-- :::editable-content-end::: -->

:::moniker-end
<!-- :::item-end::: -->
<!-- :::item name="publishPackageMetadata"::: -->
:::moniker range=">=azure-pipelines-2019.1"

**`publishPackageMetadata`** - **Publish pipeline metadata**<br>
Type: boolean. Default value: true.<br>
<!-- :::editable-content name="helpMarkDown"::: -->
Associate this build/release pipeline’s metadata (run #, source code information) with the package when uploading to my feeds.
<!-- :::editable-content-end::: -->

:::moniker-end
<!-- :::item-end::: -->
<!-- :::inputs-end::: -->

<!-- :::outputVariables::: -->
## Output variables

:::moniker range=">=azure-pipelines-2019"

None.

:::moniker-end
<!-- :::outputVariables-end::: -->

<!-- :::remarks::: -->
<!-- :::editable-content name="remarks"::: -->
<!-- :::editable-content-end::: -->
<!-- :::remarks-end::: -->

<!-- :::examples::: -->
<!-- :::editable-content name="examples"::: -->
<!-- :::editable-content-end::: -->
<!-- :::examples-end::: -->

<!-- :::properties::: -->
## Requirements

:::moniker range=">=azure-pipelines-2019"

| Requirement | Description |
|-------------|-------------|
| Pipeline types | YAML, Classic build, Classic release |
| Runs on | Agent, DeploymentGroup |
| [Demands](/azure/devops/pipelines/process/demands) | None |
| [Capabilities](/azure/devops/pipelines/agents/agents#capabilities) | This task does not satisfy any demands for subsequent tasks in the job. |
| [Command restrictions](/azure/devops/pipelines/security/templates#agent-logging-command-restrictions) | Any |
| [Settable variables](/azure/devops/pipelines/security/templates#agent-logging-command-restrictions) | Any |
| Agent version |  2.115.0 or greater |
| Task category | Package |

:::moniker-end
<!-- :::properties-end::: -->

<!-- :::see-also::: -->
<!-- :::editable-content name="seeAlso"::: -->
<!-- :::editable-content-end::: -->
<!-- :::see-also-end::: -->