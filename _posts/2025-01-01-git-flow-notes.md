---
title:  "Gitflow notes"
date:  2025-01-01 12:00:00 -0400
tags:  [git]
---

Guidelines for setting up and managing a repository with [Gitflow][gitflow_link]:

# Initialization

Initialize repository with:
```bash
git flow init
```
Use default settings:

- `[master]` for production releases
- `[develop]` for development
- `[feature/]` for feature branches
- `[bugfix/]` for bugfix branches
- `[release/]` for release branches
- `[hotfix/]` for hotfix branches
- `[support/]` for support branches.
- No version tag prefix. 
- Hooks and filters directory? `[.../.git/hooks]`

keep the version in a single location inside the project.
For meson projects version is kept in a `meson.build`.
For python projects `pyproject.toml` etc.
For unstructured projects `version.txt`

# Release

**1. Start the release branch**\\
From `develop` run:
```bash
git flow release start 1.0.0
```
This creates a `release/1.0.0` branch off `develop`.

**2. Bump your version number**\\
On the `release` branch, update the file(s) hold your version - e.g. `meson.build`, `pyproject.toml`, `version.txt`, etc. Commit that change:
```bash
git commit -m "chore: bump version to 1.0.0"
```
This is also the time for last-minute release prep: update a `CHANGELOG`, fix docs, etc. No new features.

**3. Finish the release**
```bash
git flow release finish 1.0.0 -m "Release version 1.0.0"
```
The tag message is required. If not provided you'll be prompted for a tag message.
This operation does three things automatically:
- Merges `release/1.0.0` → `master`
- Tags `master` with `v1.0.0`
- Merges `release/1.0.0` back → `develop`
- Deletes the `release` branch

**4. Push everything**
```bash
git push origin master
git push origin develop
git push origin --tags
```

**5. Continue working**\\
On the `develop` branch, update the file(s) hold your version - e.g. `meson.build`, `pyproject.toml`, `version.txt`, etc. Commit that change:
```bash
git commit -m "chore: bump version to 0.2.0-dev"
```

##### Commit messages

Use conventional commit message prefixes:

- `feat:` - new feature
- `fix:` - bug fix
- `chore:` - maintenance tasks (version bumps, dependency updates, tooling changes)
- `docs:` - documentation only
- `refactor:` - code restructuring

##### Versioning

Use [Semantic Versioning][semver_link]:

| Change type                              |(major.minor.patch)         |
|:-----------------------------------------|:---------------------------|
| Breaking changes                         |1.0.0 → 2.0.0               |
| New features (backwards-compatible)      |1.0.0 → 1.1.0               |
| Bug fixes                                |1.0.0 → 1.0.1               |


# Feature

From `develop`

```bash
git flow feature start my-feature
```

Work on your feature, making commits as normal. When done:
```bash
git flow feature finish my-feature
```

This merges the `feature` branch back into `develop` and deletes the `feature` branch. Then push:

```bash
git push origin develop
```
No tagging, no touching `master`. Features only ever interact with `develop`.

[gitflow_link]: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

[gitkraken_link]: https://www.gitkraken.com/

[semver_link]: https://semver.org/
