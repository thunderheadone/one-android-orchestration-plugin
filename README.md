# Thunderhead Orchestration Plugin

Thunderhead Gradle Plugin for augmenting an Android Application at build time.

Requires Gradle 5.6.4+

### Apply to project

- Using the `plugins` DSL
  - Kotlin Script (Application `build.gradle.kts` file)

    ```kotlin
      // build.gradle.kts
      plugins {
        id("com.thunderhead.android.orchestration-plugin") version "5.0.1"
      }
    ```

  - Groovy Script (Application `build.gradle` file)

    ```groovy
    // build.gradle
    plugins {
        id 'com.thunderhead.android.orchestration-plugin' version '5.0.1'
    }
    ```

  - Kotlin Script (Project `settings.gradle.kts' file)

    ```kotlin
      // settings.gradle.kts
      pluginManagement {
          repositories {
              google()
              jcenter()
              gradlePluginPortal()
              maven {
                  url = uri("https://repo.spring.io/milestone")
              }
          }
      }
    ```

  - Groovy (Project `settings.gradle' file)

    ```groovy
      // settings.gradle.kts
      pluginManagement {
          repositories {
              google()
              jcenter()
              gradlePluginPortal()
              maven {
                  url 'https://repo.spring.io/milestone'
              }
          }
      }
    ```
- Using the legacy `buildscript` DSL
  - Kotlin Script

    ```kotlin
    buildscript {
        repositories {
            google()
            jcenter()
            maven {
                name = "ThunderheadSpringMilestone"
                url = uri("https://repo.spring.io/milestone")
            }
            maven {
                name = "Thunderhead"
                url = uri("https://thunderhead.mycloudrepo.io/public/repositories/one-sdk-android")
            }
        }
        dependencies {
            classpath("com.thunderhead.android:orchestration-plugin:5.0.1")
        }
    }
    apply(plugin = "com.thunderhead.android:orchestration-plugin")
    ```

  - Groovy Script

    ```groovy
    buildscript {
        repositories {
            google()
            jcenter()
            maven {
                name 'ThunderheadSpringMilestone'
                url = 'https://repo.spring.io/milestone'
            }
            maven {
                name 'Thunderhead'
                url = 'https://thunderhead.mycloudrepo.io/public/repositories/one-sdk-android'
            }
        }
        dependencies {
            classpath 'com.thunderhead.android:orchestration-plugin:5.0.1'
        }
    }
    apply plugin: 'com.thunderhead.android.orchestration-plugin'
    ```

### DSL API Reference
  - Kotlin Script

```kotlin
// build.gradle.kts
thunderhead {
    enabled.set(true) // default true
    resources {
      buildDirectory.set(File("$buildDir/test")) // default buildDir/orchestration/resources
    }
    classProcessing {
      logfile.set(File("$buildDir/test/custom.log")) // defaults to buildDir/orchestration/classProccessorLog.log
      javaSourceTarget.set(JavaVersion.VERSION_1_8) // defaults to 1.7
      javaOutputTarget.set(JavaVersion.VERSION_1_8)  // defaults to 1.7
      processMainConfiguration.set(true) // default true
      processTestConfiguration.set(true) // default true
      // Compilers can forget to add correct bytecode metadata which is required for the orchestration plugin.
      // Ignoring the metadata will allow the plugin to complete successfully if there is a missing metadata issue.
      ignoreMissingMetadata() // default do not ignore.
    }
}
```

- Groovy Script
```groovy
// build.gradle
thunderhead {
    enabled = true // default true
    resources {
      buildDirectory = new File("$buildDir/test") // default buildDir/orchestration/resources
    }
    classProcessing {
      logfile = new File("$buildDir/test/custom.log") // defaults to buildDir/orchestration/classProcessorLog.log
      javaSourceTarget = JavaVersion.VERSION_1_8 // defaults to 1.7
      javaOutputTarget = JavaVersion.VERSION_1_8  // defaults to 1.7
      processMainConfiguration = true // default true
      processTestConfiguration = true // default true
      // Compilers can forget to add correct bytecode metadata which is required for the orchestration plugin.
      // Ignoring the metadata will allow the plugin to complete successfully if there is a missing metadata issue.
      ignoreMissingMetadata() // default do not ignore.
    }
}
```
