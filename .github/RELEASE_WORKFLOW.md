# Release Workflow

This document describes the workflow to apply for releasing.

## Steps

1. Prepare

    * Code is ready, documented, tested for versioning.
    * Update `CHANGELOG.md` according to the release version, release date and change details, and the [[Changelog Template](#changelog-template)] below.
    * Commit `CHANGELOG.md`.

2. Tag & Release

    * ALTERNATIVE 1 - Tag locally then make the GitHub release

      * `git checkout master` **#** Be sure to be on master branch
      * `git tag -a v<X.Y.Z> -m "Release version <X.Y.Z>"` **#** Tag master HEAD
      * `git push origin master --tags` **#** Push master branch with tags to the remote origin
      * Create the release on GitHub according to the [[GitHub Release Template](#github-release-template)] below with the existing tag.

    * ALTERNATIVE 2 - Create tag at the GitHub release creation step

      * Create the release on GitHub according to the [[GitHub Release Template](#github-release-template)] below especially for TAG and TITLE.
      * `git pull origin` **#** To locally pull the tag

## Changelog Template

```text
# Changelog

## Version <X.Y.Z> (<YYYY-MM-DD>)

Breaking Changes:

* <TEXT>

New Features:

* <TEXT>

Improvement:

* <TEXT>

Bugfixes:

* <TEXT>
```

## GitHub Release Template

* TAG (_Existing or to create_):

  * v<X.Y.Z>

* TITLE (_The same as tag_):

  * v<X.Y.Z>

* BODY TEMPLATE:

```text
<TEXT/COMMENT>

Please get the Docker image on [[Docker Hub](https://hub.docker.com/r/swafproject/swaf)]: `docker pull swafproject/swaf`

<RELEASE_NOTE_BODY_COPIED_FROM_CHANGELOG>
```