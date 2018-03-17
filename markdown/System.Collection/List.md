# List <font color="#C8C8C8" size="3">CLASS</font>

A list is a serial, self-scalable data structure that can grow its capacity on demand. This class is backed by a dynamically re-allocated platform array, which is not exposed through the API. The underlying implementation implies that the position-based operation can be costly, especially when the size grows significantly.<br><br>The list is iterable with the following syntax:<br><br><code>&nbsp;&nbsp;&nbsp;<font color="#993366">**for**</font> (<font color="#993366">**var**</font> a : list) {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... ... <font color="#669966">// can access element (a), but not update list</font><br>&nbsp;&nbsp;&nbsp;}</code><br><br>The methods of this class are thread safe.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-List-void"><b>List</b></a>|`public List()`
|*method*|<a href="#m-add-Object"><b>add</b></a>|`public void add(Object)`
|*method*|<a href="#m-get-int"><b>get</b></a>|`public Object get(int)`
|*method*|<a href="#m-put-int-Object"><b>put</b></a>|`public void put(int, Object)`
|*method*|<a href="#m-remove-int"><b>remove</b></a>|`public Object remove(int)`
|*method*|<a href="#m-size-void"><b>size</b></a>|`public int size()`
|*method*|<a href="#m-map-Function"><b>map</b></a>|`public List map(Function)`
|*method*|<a href="#m-reduce-Function-(unknown)"><b>reduce</b></a>|`public (unknown) reduce(Function, (unknown))`

## Constructors
<a name="c-List-void"></a>
### <code>public List()</code>
Create a new and empty List object, with default capacity.
## Fields

## Methods
<a name="m-add-Object"></a>
### <code>public void add([Object](../../Object) *element*)</code>
Add an item at the end of the list. This operation increase the size by 1.

**Parameters**

<a name="m-add-Object-p-element"></a>
- **element**
The element to add. This element can be null and of any type.

**Returns**

<a name="m-add-Object-r"></a>

<a name="m-get-int"></a>
### <code>public Object get([int](../../Integer) *index*)</code>
Get the item at the specified index.

**Parameters**

<a name="m-get-int-p-index"></a>
- **index**
The index at which the item will be returned.

**Returns**

<a name="m-get-int-r"></a>

**Throws**

- [System.ArrayOutOfRangeException](../System/ArrayOutOfRangeException)
When the index is out of range.

<a name="m-put-int-Object"></a>
### <code>public void put([int](../../Integer) *index*, [Object](../../Object) *value*)</code>
Set the item at the specified index. The index must be within the range of current size.

**Parameters**

<a name="m-put-int-Object-p-index"></a>
- **index**
The index at which the item will be returned.
<a name="m-put-int-Object-p-value"></a>
- **value**


**Returns**

<a name="m-put-int-Object-r"></a>

**Throws**

- [System.ArrayOutOfRangeException](../System/ArrayOutOfRangeException)
When the index is out of range.

<a name="m-remove-int"></a>
### <code>public Object remove([int](../../Integer) *index*)</code>
Remove the item at the specified index. The index must be within the range of current size.

**Parameters**

<a name="m-remove-int-p-index"></a>
- **index**
The index at which the item will be removed.

**Returns**

<a name="m-remove-int-r"></a>The removed item.

**Throws**

- [System.ArrayOutOfRangeException](../System/ArrayOutOfRangeException)
When the index is out of range.

<a name="m-size-void"></a>
### <code>public int size()</code>


**Returns**

<a name="m-size-void-r"></a>The size of list.

<a name="m-map-Function"></a>
### <code>public List map([Function](../../Function) *f*)</code>
Experimental - to remove.

**Parameters**

<a name="m-map-Function-p-f"></a>
- **f**


**Returns**

<a name="m-map-Function-r"></a>

<a name="m-reduce-Function-(unknown)"></a>
### <code>public (unknown) reduce([Function](../../Function) *f*, [(unknown)](../../(unknown)) *initial*)</code>
Experimental - to remove.

**Parameters**

<a name="m-reduce-Function-(unknown)-p-f"></a>
- **f**

<a name="m-reduce-Function-(unknown)-p-initial"></a>
- **initial**


**Returns**

<a name="m-reduce-Function-(unknown)-r"></a>

