# [3.0.0](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/2.0.0...3.0.0) (2021-01-28)


### Features

* **aspects:** use new Aspects with better logging ([2db4d53](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/2db4d531ebea6d6a58442b5480f26cd4c50d38ee))

### BREAKING CHANGES

* **aspects:** These new Aspects are required to use the Thunderhead SDK 9.0.0 release. Without
    these aspects identity transfer will not function.

    THX-53244



# [2.0.0](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/1.0.1...2.0.0) (2020-10-01)


### Bug Fixes

* fixed an incorrect dependency configuration which used a test repository ([79b9e83](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/79b9e83680bd1a46cbaec6b92a267313768d1735))


### Features

* **aspectj:** updated AspectJ to 1.9.7.M1 to be able to ignore missing metadata in bytecode. ([e6e2039](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/e6e20392af03dce261e975339b6f7faf2c97f653))
* **aspectjtransformer,androidtransformutils,tests:** android Gradle Plugin 3.6.4 and Gradle 5.6.4 ([5d77b45](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/5d77b45b053aecea407dee3b2392cd9bb0df22f9))
* **build:** automate the release process to Github ([9ce7d4e](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/9ce7d4e60c458e55f062d5217bf88062d419ebca))
* **class processing:** add support for properties during class processing ([b53dfee](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/b53dfee7d7607f5c2f5414fcf7552e6e49352288))


### Reverts

* Revert "[THX-49670]" ([5405906](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/5405906c6ac3c60736479521b5317d96291c72d5))
* Revert "* Updated semanticVersion to 2.0.0." ([31c0863](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/31c086318c4e65d4825e02b5539b565fb81eaadd))


### BREAKING CHANGES

* **aspectj:** The new version requires a gradle configuration change to successfully build an application.

    THX-50359
* Previous versions of the Orchestration Plugin have been removed and are no longer accessible.

THX-49202
* **aspectjtransformer,androidtransformutils,tests:** New version of Gradle required which requires applications to upgrade.

    THX-46312



## [1.0.1](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/1.0.0...1.0.1) (2020-03-25)


### Bug Fixes

* **aspectjtransformer.kt:** include library modules as source ([50986cd](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/50986cdb303d3144cc8def1de288985a591bdf68))



# 1.0.0 (2019-04-15)


### Bug Fixes

* **VersionUtil.kt buildSrc:** Fixed git branch name comparison to trim whitespace. ([cb00c21](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/cb00c21))


### Code Refactoring

* **Android Aspects Download:** Use Gradle Configurations instead of Direct Download for Aspects ([49de52e](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/49de52e))


### Features

* **Initial Plugin:** Orchestration Plugin created with small public API. ([0633fbc](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/0633fbc))


### BREAKING CHANGES

* **Android Aspects Download:** Orchestration Gradle DSL api resources-aspectsDownloadUrl has been removed.

    THX-37893

* **VersionUtil.kt buildSrc:** This changes the formula for determining the semantic version at configuration time.
* **Initial Plugin:** The original AspectJ Plugin will no longer work.

    THX-37241
