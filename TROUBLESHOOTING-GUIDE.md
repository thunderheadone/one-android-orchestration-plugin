![Thunderhead Orchestration](https://i.imgur.com/gfizURy.png "Thunderhead")

The Thunderhead Orchestration Gradle Plugin for Android Troubleshooting Guide for common implementation issues.

## Table of Contents

- [Integration issues](#integration-issues)
  * [How to resolve cannot cast the outer type to a reference type.](#cannot-cast-the-outer-type-to-a-reference-type)

## Integration issues
### Cannot cast the outer type to a reference type.
The Orchestration plugin relies on correct bytecode metadata. Compilers can have bugs that do not
provide all the necessary metadata required. Missing metadata will result in the Android Application Bytecode
being incomplete.

If an Android Application which has the Orchestration plugin applied builds successfully but produces
a runtime `ClassNotFoundException`, or another related error, check the `classFileProcessorLog.log` found
in the build directory (defaults to `build/orchestration/classFileProcessorLog.log`). If an error
containing `Whilst processing type 'Lcom/example/type;' - cannot cast the outer type to a reference type.` is
found please try ignoring the missing metadata as follows:

1. Open the App level build.gradle where the Orchestration plugin has been applied.
2. If not already present, add the `thunderhead` configuration closure.
3. If not already present, add the `classProcessing` configuration closure to the `thunderhead` closure.
4. Configure `classProcessing` to ignore missing metadata by invoking the `ignoreMissingMetadata` method.
5. Test if the error has been resolved.

Example build.gradle:

Kotlin Script:
```kotlin
plugins {
    id("com.android.application") version "x.y.z"
    id("com.thunderhead.android.orchestration-plugin")
}

android {
// configuration...
}

// ADD THIS:
thunderhead {
    classProcessing {
        ignoreMissingMetadata()
    }
}
```

Groovy:
```groovy
plugins {
    id 'com.android.application' version 'x.y.z'
    id 'com.thunderhead.android.orchestration-plugin'
}

android {
// configuration...
}

// ADD THIS:
thunderhead {
    classProcessing {
        ignoreMissingMetadata()
    }
}
```
