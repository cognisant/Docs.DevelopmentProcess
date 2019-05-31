# Source Control and Delivery

All development projects will be stored in a Git repository hosted on Github.com.

## Master

All repositories will contain a branch named `master`. This contains code which has been delivered to customers, every commit on master should be tagged as a release.

## Feature Branches

All development of new features should be performed on a feature branch, the branch name should be a concise description of the change, e.g `prevent-product-free-text-entry`.

When a feature branch is created a Github pull request should be started. This can be used for discussion and code review while work is still in progress.

Once development of a feature is complete:

- The branch will be built and deployed to our development environment.
- The feature will be tested, and can be demonstrated to users for feedback.
- Code should be reviewed by somebody other than the person who wrote it. This will be enforced by Github branch protection settings.
- Once testing and code review present no further issues the pull request can be merged to `master`.
- The merge commit on `master` should be tagged as a release with a semantic version number.
- The customer will perform their own testing, and either reject the release requesting further changes, or deploy the feature.

## Support Branches

Occasionally it may be necessary to release an emergency bugfix to something other than the current release on master. This will normally be due to a customer not yet having validated and deployed the most current release.

If this occurs, a support branch named `support/X.X` will be created by branching from the appropriate master version.
Hot-fixes or features can then be branched from this support branch, every commit on the support branch will be considered a release, similar to the commits on master. These releases will receive a version number between that of the base version and the subsequent version on master.

### Example

Imagine `master` contains the following releases:

- v1.1.0
- v1.1.1
- v1.2.0

And it becomes necessary to release a fix for a bug in 1.1.1.

A support branch named `support/1.1.X` should be created based on the v1.1.1 commit.
A feature or hotfix branch should be created, tested, and merged into `support/1.1.X` using the process described above for feature branches.
Commits on this branch will be released, starting at version 1.1.2.

If this fix also needs to be applied to 1.2.0, the relevant commits should be cherry picked onto a feature branch created from master.

## Continuous Integration

Commits to this repository will be automatically detected by Teamcity, which will build, test and (if successful) produce a deployable set of artifacts.

## Versioning

As part of the teamcity build process, GitVersion will be run to tag the build with an appropriate version number based on the source control branching scheme described above.

## Best Pratices

- **Avoid merge commits:** When two or more team members are working on a single branch simultaneously, they should avoid merge commits by doing one of the following:
    - Pulling before committing
   	- Using `git pull --rebase` after committing without pulling
