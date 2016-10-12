## Codebase

This topic describes how we maintain our codebase.

Our standards were inspired by [https:\/\/12factor.net\/codebase](https://12factor.net/codebase)

### Source Code Management

We use [Git](https://git-scm.com/) to manage changes in our codebase.

### Branches

There are two main branches that we use. 

| **Branch** | **Purpose** |
| --- | --- |
| master | Merge point for stable builds from development. Version tags are also tagged here. Hotfixes may be merged here. |
| development | Bleeding edge codebase. Feature branches are merged here. |

### Versions

We use [Semantic Versioning](http://semver.org/) to set versions in our codebase.

Versions are implemented by tagging a certain changeset in branch **master**

