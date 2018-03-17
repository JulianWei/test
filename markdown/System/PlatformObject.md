# PlatformObject <font color="#C8C8C8" size="3">INTERFACE</font>

An interface used to mark a <a href="../System/Mapped">mapped</a> platform type so that certain platform members can be implemented here. Useful when explicitly defining <a href="../../Object">Object</a> methods, such as toString(), which may have the same name as a member on platform Object. The explicitly defined methods can then call these methods.<br><br>These methods must not be implemented explicitly. The engine will automatically implement them when loading a type marked by this interface.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*|<a href="#m-pfToString-void"><b>pfToString</b></a>|`public String pfToString()`
|*method*|<a href="#m-pfHashCode-void"><b>pfHashCode</b></a>|`public int pfHashCode()`
|*method*|<a href="#m-pfEquals-Object"><b>pfEquals</b></a>|`public bool pfEquals(Object)`

## Methods
<a name="m-pfToString-void"></a>
### <code>public String pfToString()</code>
The delegating method to call toString() defined on the platform class.

**Returns**

<a name="m-pfToString-void-r"></a>The string representation of the platform object.

<a name="m-pfHashCode-void"></a>
### <code>public int pfHashCode()</code>
The delegating method to call hashcode() defined on the platform class.

**Returns**

<a name="m-pfHashCode-void-r"></a>An integer calculated from the platform object.

<a name="m-pfEquals-Object"></a>
### <code>public bool pfEquals([Object](../../Object) *val*)</code>
The delegating method to call equals(Object) defined on the platform class.<br><br>

**Parameters**

<a name="m-pfEquals-Object-p-val"></a>
- **val**
The object to compare with. If the argument is not a mapped objectthis method will return false; otherwise it delegates that to the equals(Object) method defined on the platform class.

**Returns**

<a name="m-pfEquals-Object-r"></a>True if the argument is considered equal to this one.

