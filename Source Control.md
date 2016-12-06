# Source Control

All development projects will be stored in a Git repository hosted on Github.com. 

# Branching Model

## Master

All repositories will contain a branch named `master`. This contains code which has been delivered to customers, every commit on master should be tagged as a release.

## Feature Branches

All development of new features should be performed on a feature branch, named `feature/<description>`. For large peices of work where multiple developers are collaborating, it may be necessary to create additional sub-branches during the development of a feature.

# Continuous Integration

Commits to this repository will be automatically detected by Teamcity, which will build, test and (if successful) produce a deployable set of artifacts.

## Versioning

As part of the teamcity build process, GitVersion will be run to tag the build with an appropriate version number based on the source control branching scheme described below.



