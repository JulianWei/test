# String <font color="#C8C8C8" size="3">CLASS</font>

String represents a fixed array of characters.<br><br>String is a very special class type in Julian. Its assignment behavior is copy-by-value, instead of copy-by-references. This means assigning a string SA to string SB would first create a bit-level copy of the value that SA points to, then let the copy be pointed by SB, discarding whatever SB was previously referring.<br><br>String is immutable. The methods exposed by this class are for reading its contents in various ways, and if any manipulating is implied (such as <a href="../String">replace</a>), it always mean to create a new string as the result of manipulation. The original string instance always remain unchanged.<br><br>String supports concatenaton operation by '+', which can also be used along with values of other types, as long as at least one operand is string.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*field*<font color="#FF9900"><sup>C</sup></font>|<a href="#f-length"><b>length</b></a>|`public const int length`
|*method*|<a href="#m-contains-var"><b>contains</b></a>|`public bool contains(var)`
|*method*|<a href="#m-endsWith-var"><b>endsWith</b></a>|`public bool endsWith(var)`
|*method*|<a href="#m-startsWith-var"><b>startsWith</b></a>|`public bool startsWith(var)`
|*method*|<a href="#m-indexOf-var-int"><b>indexOf</b></a>|`public int indexOf(var, int)`
|*method*|<a href="#m-firstOf-var"><b>firstOf</b></a>|`public int firstOf(var)`
|*method*|<a href="#m-substring-int-int"><b>substring</b></a>|`public String substring(int, int)`
|*method*|<a href="#m-trim-void"><b>trim</b></a>|`public String trim()`
|*method*|<a href="#m-toLower-void"><b>toLower</b></a>|`public String toLower()`
|*method*|<a href="#m-toUpper-void"><b>toUpper</b></a>|`public String toUpper()`
|*method*|<a href="#m-split-var"><b>split</b></a>|`public String split(var)`

## Constructors

## Fields
<a name="f-length"></a>
### <code>public const int length</code>
The length of this string.
## Methods
<a name="m-contains-var"></a>
### <code>public bool contains([var](../Any) *search*)</code>
Check if the string contains the given string or character.

**Parameters**

<a name="m-contains-var-p-search"></a>
- **search**
The sub-string, or a single chracater, to search within this string. Note this method is special in that it can take two different types.

**Returns**

<a name="m-contains-var-r"></a>true if the searched string/character is found.

**Throws**

- [System.TypeIncompatibleException](System/TypeIncompatibleException)
if the parameter has a type which is neither string nor char.

<a name="m-endsWith-var"></a>
### <code>public bool endsWith([var](../Any) *suffix*)</code>
Check if the string is ended with the given string or character.

**Parameters**

<a name="m-endsWith-var-p-suffix"></a>
- **suffix**
The sub-string, or a single chracater, to match to the end of this string. Note this method is special in that it can take two different types.

**Returns**

<a name="m-endsWith-var-r"></a>true if the given string/character is matched to the ending sequence of this string.

**Throws**

- [System.TypeIncompatibleException](System/TypeIncompatibleException)
if the parameter has a type which is neither string nor char.

<a name="m-startsWith-var"></a>
### <code>public bool startsWith([var](../Any) *prefix*)</code>
Check if the string is started with the given string or character.

**Parameters**

<a name="m-startsWith-var-p-prefix"></a>
- **prefix**
The sub-string, or a single chracater, to match to the start of this string. Note this method is special in that it can take two different types.

**Returns**

<a name="m-startsWith-var-r"></a>true if the given string/character is matched to the starting sequence of this string.

**Throws**

- [System.TypeIncompatibleException](System/TypeIncompatibleException)
if the parameter has a type which is neither string nor char.

<a name="m-indexOf-var-int"></a>
### <code>public int indexOf([var](../Any) *search*, [int](../Integer) *offset*)</code>
Get the starting index (0-based) of the given string or character within this string.<br><br>If only checking for the existence within the entire string, consider using <a href="../String#m-contains-var">contains()</a> instead.

**Parameters**

<a name="m-indexOf-var-int-p-search"></a>
- **search**
The sub-string, or a single chracater, to search with this string. Note this method is special in that it can take two different types.
<a name="m-indexOf-var-int-p-offset"></a>
- **offset**
The index on the this string from which the search will be performed.

**Returns**

<a name="m-indexOf-var-int-r"></a>If a non-negative value, it's the index marking the start of the first occurence of the given string/character; if negative, the given stirng/chracter doesn't exist.

**Throws**

- [System.TypeIncompatibleException](System/TypeIncompatibleException)
if the parameter has a type which is neither string nor char.

<a name="m-firstOf-var"></a>
### <code>public int firstOf([var](../Any) *search*)</code>
Get the starting index (0-based) of the first occurence of the given string or character within this string.<br><br>To search only within a certain scope of this string, call <a href="../String#m-indexOf-var-int">indexOf()</a> instead.

**Parameters**

<a name="m-firstOf-var-p-search"></a>
- **search**
The sub-string, or a single chracater, to search with this string. Note this method is special in that it can take two different types.

**Returns**

<a name="m-firstOf-var-r"></a>If a non-negative value, it's the index marking the start of the first occurence of the given string/character; if negative, the given stirng/chracter doesn't exist.

**Throws**

- [System.TypeIncompatibleException](System/TypeIncompatibleException)
if the parameter has a type which is neither string nor char.

<a name="m-substring-int-int"></a>
### <code>public String substring([int](../Integer) *start*, [int](../Integer) *end*)</code>
Get a substring out of this string.

**Parameters**

<a name="m-substring-int-int-p-start"></a>
- **start**
The starting index (inclusive).
<a name="m-substring-int-int-p-end"></a>
- **end**
The ending index (exclusive).

**Returns**

<a name="m-substring-int-int-r"></a>A substring out of this string.

**Throws**

- [System.ArgumentException](System/ArgumentException)
if the arguments contain negative value, or violates the order.

<a name="m-trim-void"></a>
### <code>public String trim()</code>
Trim the start and end of this tring, removing all the leading and trailing blank chracacters.<br><br>Blank characters are line feed (\r), carriage return (\n), horizontal tabulation (\t) and space ( ).

**Returns**

<a name="m-trim-void-r"></a>A trimmed string.

<a name="m-toLower-void"></a>
### <code>public String toLower()</code>
Convert the string to lower case.

**Returns**

<a name="m-toLower-void-r"></a>A string with same characters, except in lower case.

<a name="m-toUpper-void"></a>
### <code>public String toUpper()</code>
Convert the string to upper case.

**Returns**

<a name="m-toUpper-void-r"></a>A string with same characters, except in upper case.

<a name="m-split-var"></a>
### <code>public String split([var](../Any) *splitter*)</code>
Split the string into multiple substrings at the specified boundary.

**Parameters**

<a name="m-split-var-p-splitter"></a>
- **splitter**
The boundary to split at, which is not included into the resultant substrings.

**Returns**

<a name="m-split-var-r"></a>An array of strings split out of this string.

