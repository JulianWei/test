# Array <font color="#C8C8C8" size="3">CLASS</font>

Array is an indexiable vector structure with direct language support. It inherits from <a href="../Object">Object</a>, and is instantiated using new expression with a special grammar.<br><br>To declare an array of one or two dimentions,<br><br><code><font color="#993366">**int**</font>[] ia;<br><font color="#993366">**string**</font>[][] saa;</code> The [] grammar can be expanded to any degree.<br><br>To intialize an array, there are two ways. First an all-empty array can be initialized by specifying lengths at each dimension in a new expression,<br><br><code><font color="#993366">**int**</font>[] ia = <font color="#993366">**new**</font> <font color="#993366">**int**</font>[3];<br><font color="#993366">**string**</font>[][] saa = <font color="#993366">**new**</font> <font color="#993366">**string**</font>[2][10];</code> Alternatively an array initializer can be used to specify values at each index.<br><br><code><font color="#993366">**int**</font>[] ia = <font color="#993366">**new**</font> <font color="#993366">**int**</font>[]{10, 20};</code> It should be noted that these two syntaxes cannot be mixed in any fashion.<br><br>To access an element on an array, use '[]' syntax, a.k.a. indexer:<br><br><code><font color="#993366">**int**</font> i = ia[2];<br>ia[f()+3] = g();</code><br><br>Array is interatible. This mean one can use foreach grammar on an array:<br><br><code><font color="#993366">**for**</font>(<font color="#993366">**int**</font> i : ia) {<br>&nbsp;&nbsp;...<br>}</code><br><br>Array's length is immutable and fixed during initialization. To use a scalable structure consider <a href="System.Collection/List">List</a>.<br><br>For more detailed description on Array, see broken-link.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*field*<font color="#FF9900"><sup>C</sup></font>|<a href="#f-length"><b>length</b></a>|`public const Integer length`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-copy-Array-Integer-Array-Integer-Integer"><b>copy</b></a>|`public static Integer copy(Array, Integer, Array, Integer, Integer)`

## Constructors

## Fields
<a name="f-length"></a>
### <code>public const Integer length</code>
The length of this array. Note for multi-dimensional array this refers to the length of the first dimension.
## Methods
<a name="m-copy-Array-Integer-Array-Integer-Integer"></a>
### <code>public static Integer copy([Array](../Array) *src*, [Integer](../Integer) *srcOffset*, [Array](../Array) *dst*, [Integer](../Integer) *dstOffset*, [Integer](../Integer) *count*)</code>
Copy certain section of one array to that of another.

**Parameters**

<a name="m-copy-Array-Integer-Array-Integer-Integer-p-src"></a>
- **src**
The source array.
<a name="m-copy-Array-Integer-Array-Integer-Integer-p-srcOffset"></a>
- **srcOffset**
The offset at source array to start copy from. 0-based.
<a name="m-copy-Array-Integer-Array-Integer-Integer-p-dst"></a>
- **dst**
The target array.
<a name="m-copy-Array-Integer-Array-Integer-Integer-p-dstOffset"></a>
- **dstOffset**
The offset at target array to start copy to. 0-based.
<a name="m-copy-Array-Integer-Array-Integer-Integer-p-count"></a>
- **count**
The total length to copy over

**Returns**

<a name="m-copy-Array-Integer-Array-Integer-Integer-r"></a>The number of elements copied. This number is less than or equal to <a href="m-copy-Array-Integer-Array-Integer-Integer-p-count">the specified count</a>.

**Throws**

- [System.Lang.RuntimeCheckException](System.Lang/RuntimeCheckException)
if the parameters are not meeting the requirements, such astype being incompatible, values overlapping, illegal values or illegal combination thereof, of parametrers, etc.

