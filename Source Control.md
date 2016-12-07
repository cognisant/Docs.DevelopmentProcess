# Source Control and Delivery

All development projects will be stored in a Git repository hosted on Github.com. 

## Master

All repositories will contain a branch named `master`. This contains code which has been delivered to customers, every commit on master should be tagged as a release.

## Feature Branches

All development of new features should be performed on a feature branch, named `feature/<description>`.

When a feature branch is created a Github pull request should be started. This can be used for discussion and code review while work is still in progress.

Once development of a feature is complete:

- The branch will be built and deployed to our development environment
- The feature will be tested, and can be demonstrated to users for feedback
- Code should be reviewed by somebody other than the person who wrote it. This will be enforced by Github branch protection settings
- Once testing and code review present no further issues the pull request can be merged to `master`
- The merge commit on `master` should be tagged as a release with a semantic version number
- This release will then be delivered to customers (hopefully automatically, but process TBC). 
- The customer will perform their own testing, and either reject the release requesting further changes, or deploy the feature.

## Release Branches

In normal circumstances we should try to release features independently as soon as development is complete.
In the event that multiple features are to be bundled together into a single release, a release branch named `release/<description>` should be created and have all features merged into it
The contents of the release branch should then be tested and released in the manner described above for feature branches.

## Support Branches

Occasionally it may be necessary to release an emergency bugfix to something other than the current release on master. This will normally be due to a customer not yet having validated and deployed the most current release.
If this occurs, a support branch named `support/X.X` will be created by branching from the appropriate master version.
Hotfixes or features can then be branched from this support branch, every commit on the support branch will be considered a release, similar to the commits on master. These releases will receive a version number between that of the base version and the subsequent version on master.

###Example

Imagine `master` contains the following releases:

- v1.1.0
- v1.1.1
- v1.2.0

And it becomes necessary to release a fix for a bug in 1.1.1.

A support branch named `support/1.1.X` should be created based on the v1.1.1 commit.
A feature or hotfix branch should be created, tested, and merged using the process described above for feature branches.
Commits on this branch will be released, starting at version 1.1.2.

## Continuous Integration

Commits to this repository will be automatically detected by Teamcity, which will build, test and (if successful) produce a deployable set of artifacts.

## Versioning

As part of the teamcity build process, GitVersion will be run to tag the build with an appropriate version number based on the source control branching scheme described below.



