# PlatformOriginalException <font color="#C8C8C8" size="3">CLASS</font>

Exception thrown when the platform runtime encountered an error.<br><br>When a user mapped type encountered a runtime exception, it will pop up through the platform stack and emerged at the platform-engine boundary, at which an exception of this type will be created, wrapping the underlying error and preserving its stack. Thus this exception's stack trace will contain both the script trace and the platform trace.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-PlatformOriginalException-string-string"><b>PlatformOriginalException</b></a>|`public PlatformOriginalException(string, string)`

## Constructors
<a name="c-PlatformOriginalException-string-string"></a>
### <code>public PlatformOriginalException([string](../../String) *className*, [string](../../String) *msg*)</code>
Create a platform class running exception with the class name and specific message. While entirely legal, it's not recommended for a user to create such instances.
## Fields

## Methods
