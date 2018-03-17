# Map <font color="#C8C8C8" size="3">CLASS</font>

A hash map to store data based on the calculated hash value, allowing fast element-targeting operation at O(1) cost.<br><br>An object stored in map will provide its hash through <a href="broken-link">Object.hashCode()</a> method. A primitive value will convert is numeric value into an integer to be used as hash. For example, byte value simply promotes the value to integer, and a float value get floored to an integer.<br><br>The hashcode is only a means to locate the slot in the map, but doesn't have to be unique. The uniqueness is determined by <a href="broken-link">Object.equals()</a> method. When putting a value into a map, if the slot suggested by the hashcode is already occupied, Object.equalsTo() is called between the new object and existing one. If the method returns true, the new object is not added; otherwise, the object will be added anyway. If there is more than one object using that slot, each of them will be compared against before the new object can be cleared of its uniqueness and added. The multiple objects stored on the same map slot are internally organized by a linked list. In best practice, try to make the hashcode as unique as possible to improve the performance, and always pay attention to equals() to ensure its proper functioning in determining the logical equality between two objects.<br><br>Julian supports map operation at language level. Use indexer syntax (`[`]) to achieve easy access:<br><br><code>&nbsp;&nbsp;&nbsp;map[key] = value1;<br>&nbsp;&nbsp;&nbsp;<font color="#993366">**var**</font> value2 = map[key];</code><br><br>Map is iterable. Each value returned during iteration is an <a href="../System.Collection/Entry">Entry</a>. Example:<br><br><code>&nbsp;&nbsp;&nbsp;<font color="#993366">**for**</font> (<font color="#993366">**var**</font> entry : map) {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Console.println(entry.key + <font color="#3300FF">"="</font> + entry.value);<br>&nbsp;&nbsp;&nbsp;}</code><br><br>The methods of this class are NOT thread safe.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Map-void"><b>Map</b></a>|`public Map()`
|*method*|<a href="#m-put-Object-Object"><b>put</b></a>|`public Void put(Object, Object)`
|*method*|<a href="#m-hasKey-Object"><b>hasKey</b></a>|`public Bool hasKey(Object)`
|*method*|<a href="#m-remove-Object"><b>remove</b></a>|`public Object remove(Object)`
|*method*|<a href="#m-get-Object"><b>get</b></a>|`public Object get(Object)`
|*method*|<a href="#m-size-void"><b>size</b></a>|`public Integer size()`

## Constructors
<a name="c-Map-void"></a>
### <code>public Map()</code>
Create a new map instance.
## Fields

## Methods
<a name="m-put-Object-Object"></a>
### <code>public Void put([Object](../../Object) *key*, [Object](../../Object) *value*)</code>
Put a key/value pair into the map. The key's hashCode() is to calculate the storage location, and its equals() method is used to determine the uniqueness.

**Parameters**

<a name="m-put-Object-Object-p-key"></a>
- **key**
The key to the map.
<a name="m-put-Object-Object-p-value"></a>
- **value**
The value to store under this key. Can be null.

**Returns**

<a name="m-put-Object-Object-r"></a>

<a name="m-hasKey-Object"></a>
### <code>public Bool hasKey([Object](../../Object) *key*)</code>
Check if the specified key exists in the map, without getting the value associated with it.

**Parameters**

<a name="m-hasKey-Object-p-key"></a>
- **key**
The key to the map.

**Returns**

<a name="m-hasKey-Object-r"></a>true if the key exists; false otherwise.

<a name="m-remove-Object"></a>
### <code>public Object remove([Object](../../Object) *key*)</code>
Remove the specified key from the the map.<br><br>

**Parameters**

<a name="m-remove-Object-p-key"></a>
- **key**
The key to the map.

**Returns**

<a name="m-remove-Object-r"></a>If the key existed, the value associated with this key; otherwise, null. Note if the valueis null this method cannot tell if a value of null has been removed or the key didn't exist. If such information is required, call <a href="broken-link">#hasKey</a> beforehand.

<a name="m-get-Object"></a>
### <code>public Object get([Object](../../Object) *key*)</code>
Get the value from the the map by the specified key.<br><br>

**Parameters**

<a name="m-get-Object-p-key"></a>
- **key**
The key to the map.

**Returns**

<a name="m-get-Object-r"></a>If the key existed, the value associated with this key; otherwise, null. Note if the valueis null this method cannot tell if a value of null has been retrieved or the key didn't exist. If such information is required, call <a href="broken-link">#hasKey</a> beforehand.

<a name="m-size-void"></a>
### <code>public Integer size()</code>
The size of map.

**Returns**

<a name="m-size-void-r"></a>

