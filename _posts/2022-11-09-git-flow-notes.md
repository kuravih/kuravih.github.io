---
title:  "Gitflow notes"
date:  2023-08-28 12:00:00 -0400
tags:  [git]
comments_id: 3
---

Guidelines for setting up and managing a repository with [Gitflow][gitflow_link]:

### Initialization

Initialize repository with `$ git flow init`.

Keep default branch names. `master` for production releases, `develop` for development, `feature/` for feature branches, `bugfix/` for bugfix branches, `release/` for release branches, `hotfix/` for hotfix branches and `support/` for support branches.
Use `v` as the version tag prefix. 

For this jekyll blog use branch names `post/` for feature branches (to be used for posts) and `publish/` for release branches (to be used for publishing).
Do not include workspace settings files such as `code-workspace` in the repository but include sync scripts such as `push.sh` and `pull.sh`.

Keep a version string in a file thats included in the repository itself (usually in a header file).

### Development

Commit routine development commits to the develop branch.

### Feature

Start and finish feature branches using the gitflow feature in [gitkraken][gitkraken_link].

### Release

Start the release using the gitflow feature in [gitkraken][gitkraken_link].

when prompted type in release version `x.y.z` (do not use prefixes)
Use the version numbering scheme below.
Prepare the release by committing any release specific changes to the release branch.
The final commit in the release branch must be updating the version string to match the release version specified in the previous step.
Finish release. 

Fist commit in the development branch after a release should be incrementing the version string `x.y.z+1` and re-append the `-dev` tag.

A typical release transaction should look like this:

![SVG](/assets/img/gitflow_release.svg "Gitflow release transaction"){: .center width="500px" }

version numbering scheme:

    - develop - 0.0.1-dev
    - release - 0.1.0
    - develop - 0.1.1-dev
    - develop - 0.1.2-dev
    - develop - 0.1.3-dev
    - release - 0.2.0
    - develop - 0.2.1-dev
    - develop - 0.2.2-dev
    - develop - 0.2.3-dev


[gitflow_link]: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

[gitkraken_link]: https://www.gitkraken.com/

[semver_link]: https://semver.org/
