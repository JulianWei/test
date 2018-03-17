# StackOverflowException <font color="#C8C8C8" size="3">CLASS</font>

The thread stack hits the limit and thus new frame cannot be allocated.<br><br>This is a fundamental system error and can be thrown anytime during the runtime, not necessarily where a function is called. At the point of this failure there is no guarantee that the engine can continue to function normally so there is no point of capturing it. In fact this exception won't be caught by catch block.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-StackOverflowException-void"><b>StackOverflowException</b></a>|`public StackOverflowException()`

## Constructors
<a name="c-StackOverflowException-void"></a>
### <code>public StackOverflowException()</code>
Create a platform class running exception with fixed message. While entirely legal, it's not recommended for a user to create such instances.
## Fields

## Methods
