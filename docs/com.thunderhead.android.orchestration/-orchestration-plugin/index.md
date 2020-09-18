[orchestration-plugin](../../index.md) / [com.thunderhead.android.orchestration](../index.md) / [OrchestrationPlugin](./index.md)

# OrchestrationPlugin

`class OrchestrationPlugin : Plugin<Project>`

Thunderhead Orchestration Plugin.

Requires an Android Gradle plugin to be applied to the Gradle Project prior
application. A [com.android.build.api.transform.Transform](#) is added to the
applied Android Gradle plugin. The transform is applied during configuration because the Android
plugin does not allow for lazy additions to the transformation list. Instead
the Android Plugins does eager configuration using the `afterEvaluate`
Gradle build hook meaning a transformer cannot be added during the
execution phase.

All Orchestration Tasks are configured to run before the [MAIN_PREBUILD](#)
task. This task was chosen because it is created by the Android Gradle
plugin at "apply" time and can therefore be accessed eagerly by other
build tools without impacting the configuration phase build times.
All other tasks are created lazily by the Android Gradle plugin. If
the Android Gradle plugin ever exposes the lazy task [org.gradle.api.tasks.TaskProvider](#)
then that should be used instead to configure the task dependency graph.
The latest Android Gradle plugin, 3.3.0 at the time of this note,
does not expose the task providers.

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | `OrchestrationPlugin()`<br>Thunderhead Orchestration Plugin. |

### Functions

| Name | Summary |
|---|---|
| [apply](apply.md) | `fun apply(target: Project): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
