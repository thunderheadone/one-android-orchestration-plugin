[orchestration-plugin](../../index.md) / [com.thunderhead.android.orchestration.api.resources](../index.md) / [ResourceModel](./index.md)

# ResourceModel

`open class ResourceModel`

DSL model to configure resource values.

The class is `open` as it is expected to be created by Gradle
via [org.gradle.api.plugins.ExtensionContainer.create](#)
and thus *should* be safe to cast as [org.gradle.api.plugins.ExtensionAware](#).

```
thunderhead {
  resources {
    buildDirectory.set(File($buildDir, "customDir"))
  }
}
```

### Parameters

`objectFactory` - [ObjectFactory](#) to construct lazy properties.

`orchestrationDirectory` - [DirectoryProperty](#) to use as a base output location.

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | `ResourceModel(objectFactory: ObjectFactory, orchestrationDirectory: DirectoryProperty)`<br>DSL model to configure resource values. |

### Properties

| Name | Summary |
|---|---|
| [buildDirectory](build-directory.md) | `val buildDirectory: DirectoryProperty`<br>Build Directory for Orchestration resources. |
