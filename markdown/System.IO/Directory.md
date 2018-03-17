# Directory <font color="#C8C8C8" size="3">CLASS</font>

A directory (a.k.a. folder), as defined by the underlying file system.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Directory-string"><b>Directory</b></a>|`public Directory(string)`
|*method*|<a href="#m-isFile-void"><b>isFile</b></a>|`public bool isFile()`
|*method*|<a href="#m-getName-void"><b>getName</b></a>|`public String getName()`
|*method*|<a href="#m-getPath-void"><b>getPath</b></a>|`public String getPath()`
|*method*|<a href="#m-exists-void"><b>exists</b></a>|`public bool exists()`
|*method*|<a href="#m-create-void"><b>create</b></a>|`public bool create()`
|*method*|<a href="#m-delete-void"><b>delete</b></a>|`public bool delete()`
|*method*|<a href="#m-listAll-void"><b>listAll</b></a>|`public Item listAll()`

## Constructors
<a name="c-Directory-string"></a>
### <code>public Directory([string](../../String) *path*)</code>
Create a new directory with the specified path.
## Fields

## Methods
<a name="m-isFile-void"></a>
### <code>public bool isFile()</code>
Return false.

**Returns**

<a name="m-isFile-void-r"></a>

<a name="m-getName-void"></a>
### <code>public String getName()</code>
Get the name of this directory. This is only the simple name (with extension part) under the path.

**Returns**

<a name="m-getName-void-r"></a>

<a name="m-getPath-void"></a>
### <code>public String getPath()</code>
Get the absolute path of this directory. This doesn't include the name.

**Returns**

<a name="m-getPath-void-r"></a>

<a name="m-exists-void"></a>
### <code>public bool exists()</code>
Whether this directory exist on file system.

**Returns**

<a name="m-exists-void-r"></a>True if the directory exists.

<a name="m-create-void"></a>
### <code>public bool create()</code>
Create a directory represented by this object.

**Returns**

<a name="m-create-void-r"></a>True if the directory was created; false if the directory already exists.

**Throws**

- [System.IO.IOException](../System.IO/IOException)
An error occurred during directory creation.

<a name="m-delete-void"></a>
### <code>public bool delete()</code>
Delete this directory recursively.<br><br>This operation is not transactional. If an exception is thrown during the call some items may have been deleted.<br><br>

**Returns**

<a name="m-delete-void-r"></a>True if the directory, along with all of its sub-directories and files contained with,were successfully deleted; false if the directory didn't exist.

**Throws**

- [System.IO.IOException](../System.IO/IOException)
An error occurred during directory deletion.

<a name="m-listAll-void"></a>
### <code>public Item listAll()</code>
List all items directly under this directory.<br><br>

**Returns**

<a name="m-listAll-void-r"></a>An array of items directly under this directory, including files and sub-directories. With this method,a recursion-based approach is usually applicable to processing all the items under a given directory.

