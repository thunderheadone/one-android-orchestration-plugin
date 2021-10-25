//[orchestration-plugin](../../../index.md)/[com.thunderhead.android.orchestration.api.resources](../index.md)/[ResourceModel](index.md)

# ResourceModel

[jvm]\
open class [ResourceModel](index.md)@Inject()constructor(**objectFactory**: ObjectFactory, **orchestrationDirectory**: DirectoryProperty)

DSL model to configure resource values.

The class is open as it is expected to be created by Gradle via org.gradle.api.plugins.ExtensionContainer.create and thus *should* be safe to cast as org.gradle.api.plugins.ExtensionAware.

thunderhead {\
  resources {\
    buildDirectory.set(File($buildDir, "customDir"))\
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
| [ResourceModel](-resource-model.md) | [jvm]<br>@Inject()<br>fun [ResourceModel](-resource-model.md)(objectFactory: ObjectFactory, orchestrationDirectory: DirectoryProperty)<br>ObjectFactory to construct lazy properties. |

## Properties

| Name | Summary |
|---|---|
| [buildDirectory](build-directory.md) | [jvm]<br>val [buildDirectory](build-directory.md): DirectoryProperty<br>Build Directory for Orchestration resources. |
