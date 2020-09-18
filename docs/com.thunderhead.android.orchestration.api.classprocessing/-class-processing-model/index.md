[orchestration-plugin](../../index.md) / [com.thunderhead.android.orchestration.api.classprocessing](../index.md) / [ClassProcessingModel](./index.md)

# ClassProcessingModel

`open class ClassProcessingModel`

DSL model to configure class processing.

The class is `open` as it is expected to be created by Gradle
via [org.gradle.api.plugins.ExtensionContainer.create](#)
and thus *should* be safe to cast as [org.gradle.api.plugins.ExtensionAware](#).

```
thunderhead {
  classProcessing {
    logfile.set(File($buildDir, "customfile.log"))
    javaSourceTarget.set(JavaVersion.VERSION_1_8)
    javaOutputTarget.set(JavaVersion.VERSION_1_8)
    processMainConfiguration.set(true)
    processTestConfiguration.set(true)
  }
}
```

### Parameters

`objectFactory` - [ObjectFactory](#) to construct lazy properties.

`orchestrationDirectory` - [DirectoryProperty](#) to use as a base output location.

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | `ClassProcessingModel(objectFactory: ObjectFactory, orchestrationDirectory: DirectoryProperty)`<br>DSL model to configure class processing. |

### Properties

| Name | Summary |
|---|---|
| [javaOutputTarget](java-output-target.md) | `val javaOutputTarget: Property<JavaVersion>`<br>Target Output Java Language Level. Sensible default of 1.7. |
| [javaSourceTarget](java-source-target.md) | `val javaSourceTarget: Property<JavaVersion>`<br>Source Target Java Language Level. Sensible default of 1.7. |
| [logfile](logfile.md) | `val logfile: RegularFileProperty`<br>Class File Processor log file. Sensible default of `buildDir/orchestration/classFileProcessorLog.log` |
| [processMainConfiguration](process-main-configuration.md) | `val processMainConfiguration: Property<`[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>`<br>Orchestrate production code. Sensible default of true. |
| [processTestConfiguration](process-test-configuration.md) | `val processTestConfiguration: Property<`[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`>`<br>Orchestrate test code. Sensible default of false. |
| [properties](properties.md) | `val properties: MapProperty<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>`<br>Dynamic Properties to change class processing behavior. The public members should be used instead of directly using this property. |

### Functions

| Name | Summary |
|---|---|
| [ignoreMissingMetadata](ignore-missing-metadata.md) | `fun ignoreMissingMetadata(): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Sometimes compilers can forget to put proper JVM Bytecode metadata. Invoke this function if you think a class processing error is caused by missing metadata. |
