# Enum <font color="#C8C8C8" size="3">CLASS</font>

Enum is a special class type which defines an ordered enumeration of names, each associated with an integer value. Enum inherits <a href="../Object">Object</a>, but cannot be instantiated. Its use is strictly limited to immutable access to its members in a static context.<br><br>To declare an enum,<br><br><code><font color="#993366">**enum**</font> Color {<br>&nbsp;&nbsp;RED = 0,<br>&nbsp;&nbsp;YELLOW = 1,<br>&nbsp;&nbsp;GREEN = 2<br>}</code> The integer value defined for each name is not required. If not provided, it's defaulted to the value of previous name plus 1. In the case of first name, it's defaulted to 0. Each value must be distinct within the enum, otherwise would cause definition exception when the type is loaded.<br><br>The name of an enum can be referred to by normal addressing syntax, such as<br><br><code>Color c = Color.YELLOW;</code> However, these names cannot be used as a left value.<br><br>An enum variable, when defined without an initializer, will be initialized to the first name of that enum type. The null value cannot be assigned to an enum variable.<br><br>An enum's member has two constant fields. <a href="broken-link">literal</a> exposes the name as a <a href="../String">string</a>, <a href="broken-link">ordinal</a> the associated integer value.<br><br>Julian provides syntax-level support for switch logic based on an enum variable:<br><br><code>Color c = ...;<br><font color="#993366">**switch**</font>(c){<br><font color="#993366">**case**</font> RED: ...<br><font color="#993366">**case**</font> YELLOW: ...<br><font color="#993366">**case**</font> GREEN: ...<br>}</code><br><br>For more detailed description on Enum, see broken-link.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*field*<font color="#FF9900"><sup>C</sup></font>|<a href="#f-ordinal"><b>ordinal</b></a>|`public const Integer ordinal`
|*field*<font color="#FF9900"><sup>C</sup></font>|<a href="#f-literal"><b>literal</b></a>|`public const String literal`

## Constructors

## Fields
<a name="f-ordinal"></a>
### <code>public const Integer ordinal</code>
The integer value associated with this member.<a name="f-literal"></a>
### <code>public const String literal</code>
The name of this member, exactly as is defined in the type's definition.
## Methods
