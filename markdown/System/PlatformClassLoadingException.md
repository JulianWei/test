# PlatformClassLoadingException <font color="#C8C8C8" size="3">CLASS</font>

Exception thrown when loading a platform type.<br><br>In Julian, a platform type is loaded when a script type mapping to it is first used, so importing a module, and defining a mapped type in the current script, doesn't trigger type loading. Only by referencing a type for the first time during runtime will that type, along with all the platform dependencies, get loaded. This process strictly adheres to "Loading Completeness Principle", so that if any type cannot be loaded, none in the dependency closure will be.<br><br>A platform type may fail to load by various reasons. The type may be not locatable within the platform runtime (on JVM, this means the class is not visible from the classpath). There are also some significant restrictions on the types being mapped, and failing any of them will cause the type to be un-mappable. For more details, see broken-link.<br><br>This exception is expected to be thrown by the engine, not user's script, although its constructor is public and free to call.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-PlatformClassLoadingException-string"><b>PlatformClassLoadingException</b></a>|`public PlatformClassLoadingException(string)`

## Constructors
<a name="c-PlatformClassLoadingException-string"></a>
### <code>public PlatformClassLoadingException([string](../../String) *className*)</code>
Create a platform class loading exception with specific message. While entirely legal, it's not recommended for a user to create such instances.
## Fields

## Methods
