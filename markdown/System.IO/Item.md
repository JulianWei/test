# Item <font color="#C8C8C8" size="3">INTERFACE</font>

A file system item. Can be a file or directory.<br><br>When using this and other FS APIs, it's common to deal with paths. Unless noted, a path can be either absolute or relative (to working directory of the current process). A path comprises of one or more sections, and in case of relative path the path can be even empty. These section are separated by a path separator, which can differ based on the OS. However, Julian recognizes both '/' (POSIX) and '\' (Windows) as the equally legal path separator.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*|<a href="#m-getName-void"><b>getName</b></a>|`public String getName()`
|*method*|<a href="#m-create-void"><b>create</b></a>|`public Bool create()`
|*method*|<a href="#m-delete-void"><b>delete</b></a>|`public Bool delete()`
|*method*|<a href="#m-getPath-void"><b>getPath</b></a>|`public String getPath()`
|*method*|<a href="#m-exists-void"><b>exists</b></a>|`public Bool exists()`
|*method*|<a href="#m-isFile-void"><b>isFile</b></a>|`public Bool isFile()`

## Methods
<a name="m-getName-void"></a>
### <code>public String getName()</code>
Get the name of this item. This is only the simple name (with extension part) under the path.

**Returns**

<a name="m-getName-void-r"></a>

<a name="m-create-void"></a>
### <code>public Bool create()</code>
Create this item.

**Returns**

<a name="m-create-void-r"></a>True if the item was successfully created.

<a name="m-delete-void"></a>
### <code>public Bool delete()</code>
Delete this item.

**Returns**

<a name="m-delete-void-r"></a>True if the item was successfully deleted.

<a name="m-getPath-void"></a>
### <code>public String getPath()</code>
Get the absolute path of this item. This doesn't include the name.

**Returns**

<a name="m-getPath-void-r"></a>

<a name="m-exists-void"></a>
### <code>public Bool exists()</code>
Whether this item exist on file system.

**Returns**

<a name="m-exists-void-r"></a>True if the item exists.

<a name="m-isFile-void"></a>
### <code>public Bool isFile()</code>
Whether this item is a file

**Returns**

<a name="m-isFile-void-r"></a>True if the item is a file; false a directory.

