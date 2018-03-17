# ClassLoadingException <font color="#C8C8C8" size="3">CLASS</font>

Exception thrown during loading a type. Despite the name, this can be thrown for loading any types, including class, interface, attribute and enum.<br><br>In Julian, a type is loaded when it's first used, so importing a module, and defining a type in the current script, doesn't trigger type loading. Only by referencing a type for the first time during runtime will that type, along with all the dependencies, get loaded. If any type couldn't be loaded in this process, the entire type set will not be loaded. In Julian this is referred to as "Loading Completeness Principle", or simple LCP.<br><br>A type may fail to load by various reasons. Most likely, since Julian is in interpreted language, the semantic check on the type will only happen by the time the loading is attempted. So failing to comply with the type definition semantics and restrictions can easily lead to such failure.<br><br>This exception is expected to be thrown by the engine, not user's script, although its constructors are public and free to call.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-ClassLoadingException-string"><b>ClassLoadingException</b></a>|`public ClassLoadingException(string)`
|*constructor*|<a href="#c-ClassLoadingException-string-Exception"><b>ClassLoadingException</b></a>|`public ClassLoadingException(string, System.Exception)`

## Constructors
<a name="c-ClassLoadingException-string"></a>
### <code>public ClassLoadingException([string](../../String) *msg*)</code>
Create a class loading exception with specific message. While entirely legal, it's not recommended for a user to create such instances.<a name="c-ClassLoadingException-string-Exception"></a>
### <code>public ClassLoadingException([string](../../String) *msg*, [Exception](../System/Exception) *cause*)</code>
Create a class loading exception with specific message and cause. While entirely legal, it's not recommended for a user to create such instances.
## Fields

## Methods
