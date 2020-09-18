[orchestration-plugin](../../index.md) / [com.thunderhead.android.orchestration.api.classprocessing](../index.md) / [ClassProcessingModel](index.md) / [&lt;init&gt;](./-init-.md)

# &lt;init&gt;

`ClassProcessingModel(objectFactory: ObjectFactory, orchestrationDirectory: DirectoryProperty)`

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