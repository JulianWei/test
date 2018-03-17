# UnknownTypeException <font color="#C8C8C8" size="3">CLASS</font>

The type being referred to is not known to the script engine.<br><br>In Julian, when a type is first used it will be loaded. The type searching is performed against the current namespace pool, targeting the entire module path set, in addition to the system classes. The namespace pool consists of all the imported module's name, as well as System module. If the type is not located under any of these modules this exception will be thrown.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-UnknownTypeException-string"><b>UnknownTypeException</b></a>|`public UnknownTypeException(string)`

## Constructors
<a name="c-UnknownTypeException-string"></a>
### <code>public UnknownTypeException([string](../../String) *msg*)</code>
Create an instance of UnknownTypeException with specified message. Mainly reserved for system use.
## Fields

## Methods
