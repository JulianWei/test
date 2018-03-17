# Console <font color="#C8C8C8" size="3">CLASS</font>

Console provide means to input from and output to character-oriented terminal of the operating system.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-print-Object"><b>print</b></a>|`public static void print(Object)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-println-Object"><b>println</b></a>|`public static void println(Object)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-readln-void"><b>readln</b></a>|`public static String readln()`

## Constructors

## Fields

## Methods
<a name="m-print-Object"></a>
### <code>public static void print([Object](../../Object) *obj*)</code>
Print the given value to the console. If the value is an <a href="../../Object">Object</a>, calls <a href="../../Object#m-toString-void">Object.toString()</a> to get the string to output. If the value is of primitive type, prints its literal representation. If the value is null, prints "(null)".

**Parameters**

<a name="m-print-Object-p-obj"></a>
- **obj**


**Returns**

<a name="m-print-Object-r"></a>

<a name="m-println-Object"></a>
### <code>public static void println([Object](../../Object) *obj*)</code>
Print the given value to the console, then a line break sequences as defined by the underlying operating system. See <a href="../../Object#m-toString-void">toString()</a> for more details.

**Parameters**

<a name="m-println-Object-p-obj"></a>
- **obj**


**Returns**

<a name="m-println-Object-r"></a>

<a name="m-readln-void"></a>
### <code>public static String readln()</code>
Read the characters from standard input, until a line break sequences as defined by the underlying operating system is met. This method will be blocking the thread until the line break is accepted.

**Returns**

<a name="m-readln-void-r"></a>the string comprised of the input characters, excluding the line break at the end.

