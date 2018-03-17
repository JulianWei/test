# ConcurrentModificationException <font color="#C8C8C8" size="3">CLASS</font>

An exception to throw when attempt to modify a container occurs when such omdification is not allowed.<br><br>In Julian, a container can be iterated with language level support:<br><br><code>&nbsp;&nbsp;&nbsp;<font color="#993366">**for**</font> (<font color="#993366">**var**</font> a : list) {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... ... <font color="#669966">// Within this block the list is locked.</font><br>&nbsp;&nbsp;&nbsp;}</code><br><br>However, during the iteration the list will be locked down by the current thread. If another thread attempts to modify the container, such as by adding or removing data, this exception will be raised. Modifying from the current thread, however, will not cause this error, but can lead to undefined iteration results.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-ConcurrentModificationException-string"><b>ConcurrentModificationException</b></a>|`public ConcurrentModificationException(string)`

## Constructors
<a name="c-ConcurrentModificationException-string"></a>
### <code>public ConcurrentModificationException([string](../../String) *message*)</code>
Create a standard ConcurrentModificationException instance. While entirely legal, it's not recommended for a user to create such instances.
## Fields

## Methods
