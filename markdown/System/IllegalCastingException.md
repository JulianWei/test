# IllegalCastingException <font color="#C8C8C8" size="3">CLASS</font>

The casting is illegal. This can happen when the target type is not on the hierarchy of current type's inheritance.<br><br>In Julian, object casting is always safe when a type is cast to an super type or the same type. It's not possible to cast to a child type, if the runtime type of variable is indeed that type, or a subtype thereof. If not, or if casting to a side type (the type with which the current type only shares the common ancestor, which in the most common case is <a href="../../Object">Object</a>), will throw this exception.<br><br>Casting the primitive type may also cause this exception if the types are not castable (such as from int to bool), or if the target is an Object.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-IllegalCastingException-string"><b>IllegalCastingException</b></a>|`public IllegalCastingException(string)`

## Constructors
<a name="c-IllegalCastingException-string"></a>
### <code>public IllegalCastingException([string](../../String) *msg*)</code>
Create an instance of IllegalCastingException with specified message. Mainly reserved for system use.
## Fields

## Methods
