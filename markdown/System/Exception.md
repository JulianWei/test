# Exception <font color="#C8C8C8" size="3">CLASS</font>

The exception class that can be thrown by scripts, or raised directly from the engine.<br><br>All Julian exceptions are derived from this class. An exception can be captured using the classic try-catch blocks, where exception are matched against each catch section in the script order.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Exception-void"><b>Exception</b></a>|`public Exception()`
|*constructor*|<a href="#c-Exception-string"><b>Exception</b></a>|`public Exception(string)`
|*constructor*|<a href="#c-Exception-string-Exception"><b>Exception</b></a>|`public Exception(string, System.Exception)`
|*method*|<a href="#m-getMessage-void"><b>getMessage</b></a>|`public String getMessage()`
|*method*|<a href="#m-getStackTrace-void"><b>getStackTrace</b></a>|`public String getStackTrace()`
|*method*|<a href="#m-getCause-void"><b>getCause</b></a>|`public Exception getCause()`

## Constructors
<a name="c-Exception-void"></a>
### <code>public Exception()</code>
Create an exception without any specific information.<a name="c-Exception-string"></a>
### <code>public Exception([string](../../String) *message*)</code>
Create an exception with message.<a name="c-Exception-string-Exception"></a>
### <code>public Exception([string](../../String) *message*, [Exception](../System/Exception) *cause*)</code>
Create an exception with message and cause.
## Fields

## Methods
<a name="m-getMessage-void"></a>
### <code>public String getMessage()</code>
Get the message.

**Returns**

<a name="m-getMessage-void-r"></a>Can be null if the message was not specified during construction.

<a name="m-getStackTrace-void"></a>
### <code>public String getStackTrace()</code>
Get the current stack trace, starting from the function where the exception was thrown (originating function) and ending with the current function.

**Returns**

<a name="m-getStackTrace-void-r"></a>Can be null if the message was not specified during construction.

<a name="m-getCause-void"></a>
### <code>public Exception getCause()</code>
Get the cause of this exception, if any.

**Returns**

<a name="m-getCause-void-r"></a>Can be null if the cause was not specified during construction.

