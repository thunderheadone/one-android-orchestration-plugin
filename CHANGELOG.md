# [7.0.0](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/6.0.1...7.0.0) (2022-02-09)


### BREAKING CHANGES

    MOB-1925
* **aspects:** Aspects are upgraded

    MOB-1911
* **aspects:** Fixed a runtime error where static method `getLogger()` could not be found.



## [6.0.1](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/6.0.0...6.0.1) (2021-11-03)


### Bug Fixes

* **aspectj tools update:** updated the AspectJ toolkit to a final version and not a milestone ([597170a](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/597170a9056ec8196427b51d51b21c0ff0e40cd4))



# [6.0.0](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/5.0.1...6.0.0) (2021-10-21)


### Bug Fixes

* **aspectjtransformer, configuration:** fix enabled = false ClassNotFoundException ([d4211d1](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/d4211d13b4d020697ada246ac2314f1b2848a08a))
* **aspectjtransformerutils.kt:** prevent weaving of SDK code ([c6947b1](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/c6947b13745e9d638d6e6fa677064114a8a14947))
* **aspectjtransformerutils:** fixed a bug where an attempt to make an already existing file occurred ([7952655](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/79526550ea9f8be849daf2f69508b4383ab58d17))
* fixed an incorrect dependency configuration which used a test repository ([79b9e83](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/79b9e83680bd1a46cbaec6b92a267313768d1735))


### Features

* **android gradle plugin 4.2.0:** Upgraded to support Android Gradle Plugin 4.2.0 ([870c96d](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/870c96dd6c69dde77245ce2b3d5f128034691f67))


### BREAKING CHANGES

* **aspects:** Aspects are upgraded.

    MOB-1731
* **upgraded to kotlin 1.5.20:** Upgraded to Kotlin 1.5.20.

   MOB-1332
* **android gradle plugin 4.2.0:** Upgraded to Android Gradle Plugin 4.2.0

    MOB-1554
* **aspectjtransformer,androidtransformutils,tests:** New version of Gradle required which requires applications to upgrade.


## [5.0.1](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/5.0.0...5.0.1) (2021-07-19)


### Bug Fixes

* **aspectjtransfomerutils:** do not use colons in filename ([ee27da7](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/ee27da7ce55cf746b0df5a2674c8bbeb6cbf141f))



# [5.0.0](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/4.0.0...5.0.0) (2021-07-13)


### BREAKING CHANGES

* **aspects:** These new Aspects are required to use the Thunderhead SDK 10.0.0 release. Without
    these aspects identity transfer will not function.

    MOB-1238


# [4.0.0](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/compare/3.0.0...4.0.0) (2021-03-18)


### Bug Fixes

* **aspectjtransformer, configuration:** fix enabled = false ClassNotFoundException ([d4211d1](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/d4211d13b4d020697ada246ac2314f1b2848a08a))
* **aspectjtransformerutils:** fixed a bug where an attempt to make an already existing file occurred ([7952655](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/79526550ea9f8be849daf2f69508b4383ab58d17))


### improvement

* **generateconstantstask:** add support for `registerForActivityResult` ([b7bb2da](https://bitbucket.org/thunderhead-com/one-mobile-android-gradle-plugin/commits/b7bb2daa9ce4ae28b5a64edf60193c646ba3fe4f))


### BREAKING CHANGES

* **generateconstantstask:** New aspects are required for Identity Transfer in AndroidX Activities and
Fragments.


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
