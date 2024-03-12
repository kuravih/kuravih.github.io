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

<svg xmlns="http://www.w3.org/2000/svg" class="center clipart" width="640px" height="736px" viewBox="0 0 640 736" fill="none" stroke="black" stroke-width="2px" stroke-linecap="round" stroke-linejoin="round">
    <defs>
        <marker class="marker" id="ellipsisStartMarker" markerWidth="2px" markerHeight="6px" refX="1px" refY="7px" orient="0deg" stroke-width="0px" stroke-linecap="round" stroke-linejoin="round">
            <circle cy="3px" cx="1px" r="0.5px"/>
            <circle cy="5px" cx="1px" r="0.5px"/>
        </marker>
        <marker class="marker" id="ellipsisEndMarker" markerWidth="2px" markerHeight="6px" refX="1px" refY="-1px" orient="0deg" stroke-width="0px" stroke-linecap="round" stroke-linejoin="round">
            <circle cy="1px" cx="1px" r="0.5px"/>
            <circle cy="3px" cx="1px" r="0.5px"/>
        </marker>
    </defs>
    <path d="m 64 64 
             v 512" marker-start="url(#ellipsisStartMarker)" marker-end="url(#ellipsisEndMarker)" />
    <path d="m 128 64 
             v 512" marker-start="url(#ellipsisStartMarker)" marker-end="url(#ellipsisEndMarker)" />
    <path d="m 128 256
             h 48
             a 16 16 90 0 1 16 16
             v 160
             a 16 16 90 0 1 -16 16
             h -112" />
    <path d="m 64 320 
             h 112
             a 16 16 90 0 1 16 16
             v 96
             a 16 16 90 0 1 -16 16
             h -112" />
    <circle cy="128px" cx="64px" r="16px" fill="lightskyblue"></circle>
    <text class="text" x="256px" y="128px" stroke-width="0px" >Development commit ...</text>

    <circle cy="192px" cx="64px" r="16px" fill="lightskyblue"></circle>
    <text class="text" x="256px" y="192px" stroke-width="0px" >Increment development version</text>

    <circle cy="256px" cx="128px" r="8px" fill="lightgreen"></circle>
    <text class="text" x="256px" y="256px" stroke-width="0px" >Merge branch 'release/0.1.0'</text>

    <circle cy="320px" cx="64px" r="8px" fill="lightskyblue"></circle>
    <text class="text" x="256px" y="320px" stroke-width="0px" >Merge branch 'release/0.1.0' into develop</text>

    <circle cy="384px" cx="192px" r="16px" fill="plum"></circle>
    <text class="text" x="256px" y="384px" stroke-width="0px" >Version bump</text>

    <circle cy="448px" cx="64px" r="16px" fill="lightskyblue"></circle>
    <text class="text" x="256px" y="448px" stroke-width="0px" >Development commit ...</text>

    <circle cy="512px" cx="64px" r="16px" fill="lightskyblue"></circle>
    <text class="text" x="256px" y="512px" stroke-width="0px" >Development commit ...</text>

    <g>
        <rect x="48px" y="608px" width="32px" height="80px" rx="8px" stroke="#5D5D67" fill="lightskyblue"/>
        <text x="-648px" y="68px" stroke-width="0px" transform="rotate(-90)" text-anchor="middle" fill="#5D5D67" >Develop</text>
    </g>
    <g>
        <rect x="112px" y="608px" width="32px" height="80px" rx="8px" stroke="#5D5D67" fill="lightgreen"/>
        <text x="-648px" y="132px" stroke-width="0px" transform="rotate(-90)" text-anchor="middle" fill="#5D5D67" >Main</text>
    </g>
    <g>
        <rect x="176px" y="608px" width="32px" height="80px" rx="8px" stroke="#5D5D67" fill="plum"/>
        <text x="-648px" y="196px" stroke-width="0px" transform="rotate(-90)" text-anchor="middle" fill="#5D5D67" >Release</text>
    </g>
</svg>



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
