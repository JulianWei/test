# ArrayOutOfRangeException <font color="#C8C8C8" size="3">CLASS</font>

Exception caused by attempting to use an index out of the allowed range. This can be created by the engine when it is trying to use an index on an array beyond its range. For example, a negative number, or a positive one larger than or equal to the length of the array, will cause this exception. A user may also create this exception pre-emptively as part of the argument check.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-ArrayOutOfRangeException-int-int"><b>ArrayOutOfRangeException</b></a>|`public ArrayOutOfRangeException(int, int)`

## Constructors
<a name="c-ArrayOutOfRangeException-int-int"></a>
### <code>public ArrayOutOfRangeException([int](../../Integer) *index*, [int](../../Integer) *max*)</code>
Create a standard ArrayOutOfRangeException instance. The message for this exception is fixed.
## Fields

## Methods
