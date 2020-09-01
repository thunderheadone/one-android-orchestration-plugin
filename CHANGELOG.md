# 1.0.1 (2020-03-25)


### Bug Fixes

* **aspectjtransformer.kt:** include library modules as source



# 1.0.0 (2019-04-15)


### Bug Fixes

* **VersionUtil.kt buildSrc:** Fixed git branch name comparison to trim whitespace.


### Code Refactoring

* **Android Aspects Download:** Use Gradle Configurations instead of Direct Download for Aspects


### Features

* **Initial Plugin:** Orchestration Plugin created with small public API.


### BREAKING CHANGES

* **Android Aspects Download:** Orchestration Gradle DSL api resources-aspectsDownloadUrl has been removed.

    THX-37893

* **VersionUtil.kt buildSrc:** This changes the formula for determining the semantic version at configuration time.
* **Initial Plugin:** The original AspectJ Plugin will no longer work.

    THX-37241
