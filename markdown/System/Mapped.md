# Mapped <font color="#C8C8C8" size="3">ATTRIBUTE</font>

A class or interface marked by this attribute is mapped directly to a platform class or interface.<br><br>A class maps to a platform class and an interface maps to a platform interface. Only public constructors and methods are mapped, plus any constant static fields (which are marked as 'final' in Java). The platform's typing hierarchy will also be mirrored. Throughout the runtime the instance of a mapped class is essentially a wrapper of the underlying instance.<br><br>This approach allows a convenient and easy-to-use platform inter-operation at the price of performance. As of current version, this is the only way for ordinary users to talk to JVM classes.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*field*|<a href="#f-null"><b>null</b></a>|`public String null`
|*field*|<a href="#f-null"><b>null</b></a>|`public String null`

## Fields
<a name="f-null"></a>
### <code>public String null</code>
The class/interface name to map to. This name must be a fully qualified name and the type is expected to be loaded into JVM on demand.<a name="f-null"></a>
### <code>public String null</code>
The method name to map to. This is currently not supported.
