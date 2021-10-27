//[orchestration-plugin](../../../index.md)/[com.thunderhead.android.orchestration.api.classprocessing](../index.md)/[ClassProcessingModel](index.md)

# ClassProcessingModel

[jvm]\
open class [ClassProcessingModel](index.md)@Inject()constructor(**objectFactory**: ObjectFactory, **orchestrationDirectory**: DirectoryProperty)

DSL model to configure class processing.

The class is open as it is expected to be created by Gradle via org.gradle.api.plugins.ExtensionContainer.create and thus *should* be safe to cast as org.gradle.api.plugins.ExtensionAware.

thunderhead {\
  classProcessing {\
    logfile.set(File($buildDir, "customfile.log"))\
    javaSourceTarget.set(JavaVersion.VERSION_1_8)\
    javaOutputTarget.set(JavaVersion.VERSION_1_8)\
    processMainConfiguration.set(true)\
    processTestConfiguration.set(true)\
  }\
}

## Parameters

jvm

| | |
|---|---|
| objectFactory | ObjectFactory to construct lazy properties. |
| orchestrationDirectory | DirectoryProperty to use as a base output location. |

## Constructors

| | |
|---|---|
| [ClassProcessingModel](-class-processing-model.md) | [jvm]<br>@Inject()<br>fun [ClassProcessingModel](-class-processing-model.md)(objectFactory: ObjectFactory, orchestrationDirectory: DirectoryProperty)<br>ObjectFactory to construct lazy properties. |

## Functions

| Name | Summary |
|---|---|
| [ignoreMissingMetadata](ignore-missing-metadata.md) | [jvm]<br>fun [ignoreMissingMetadata](ignore-missing-metadata.md)()<br>Sometimes compilers can forget to put proper JVM Bytecode metadata. |

## Properties

| Name | Summary |
|---|---|
| [javaOutputTarget](java-output-target.md) | [jvm]<br>val [javaOutputTarget](java-output-target.md): Property<JavaVersion><br>Target Output Java Language Level. |
| [javaSourceTarget](java-source-target.md) | [jvm]<br>val [javaSourceTarget](java-source-target.md): Property<JavaVersion><br>Source Target Java Language Level. |
| [logfile](logfile.md) | [jvm]<br>val [logfile](logfile.md): RegularFileProperty<br>Class File Processor log file. |
| [processMainConfiguration](process-main-configuration.md) | [jvm]<br>val [processMainConfiguration](process-main-configuration.md): Property<[Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)><br>Orchestrate production code. |
| [processTestConfiguration](process-test-configuration.md) | [jvm]<br>val [processTestConfiguration](process-test-configuration.md): Property<[Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)><br>Orchestrate test code. |
| [properties](properties.md) | [jvm]<br>val [properties](properties.md): MapProperty<[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)><br>Dynamic Properties to change class processing behavior. |
