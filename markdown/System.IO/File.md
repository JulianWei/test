# File <font color="#C8C8C8" size="3">CLASS</font>

A file, as defined by the underlying file system.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-File-string"><b>File</b></a>|`public File(string)`
|*method*|<a href="#m-isFile-void"><b>isFile</b></a>|`public bool isFile()`
|*method*|<a href="#m-getName-void"><b>getName</b></a>|`public String getName()`
|*method*|<a href="#m-getPath-void"><b>getPath</b></a>|`public String getPath()`
|*method*|<a href="#m-readAllText-void"><b>readAllText</b></a>|`public String readAllText()`
|*method*|<a href="#m-exists-void"><b>exists</b></a>|`public bool exists()`
|*method*|<a href="#m-create-void"><b>create</b></a>|`public bool create()`
|*method*|<a href="#m-delete-void"><b>delete</b></a>|`public bool delete()`
|*method*|<a href="#m-getReadStream-void"><b>getReadStream</b></a>|`public Stream getReadStream()`
|*method*|<a href="#m-getWriteStream-bool"><b>getWriteStream</b></a>|`public Stream getWriteStream(bool)`

## Constructors
<a name="c-File-string"></a>
### <code>public File([string](../../String) *path*)</code>
Create a new file with the specified path.
## Fields

## Methods
<a name="m-isFile-void"></a>
### <code>public bool isFile()</code>
Return true.

**Returns**

<a name="m-isFile-void-r"></a>

<a name="m-getName-void"></a>
### <code>public String getName()</code>
Get the name of this file. This is only the simple name (with extension part) under the path.

**Returns**

<a name="m-getName-void-r"></a>

<a name="m-getPath-void"></a>
### <code>public String getPath()</code>
Get the absolute path of this file. This doesn't include the name.

**Returns**

<a name="m-getPath-void-r"></a>

<a name="m-readAllText-void"></a>
### <code>public String readAllText()</code>
Read all contents from this file as text. This is rather convenient method for quick scripting, but won't scale well if the file is too large and the operation is too frequent. When dealing with reading large files at high frequency, always consider using an <a href="../System.IO/File#m-getReadStream-void">asynchronous stream</a> first.

**Returns**

<a name="m-readAllText-void-r"></a>The contains from this file, in the format of plain ASCII text.

<a name="m-exists-void"></a>
### <code>public bool exists()</code>
Whether this file exist on file system.

**Returns**

<a name="m-exists-void-r"></a>True if the file exists.

<a name="m-create-void"></a>
### <code>public bool create()</code>
Create a file represented by this object.

**Returns**

<a name="m-create-void-r"></a>True if the file was created; false if the file already exists.

**Throws**

- [System.IO.IOException](../System.IO/IOException)
An error occurred during file creation.

<a name="m-delete-void"></a>
### <code>public bool delete()</code>
Delete this file.

**Returns**

<a name="m-delete-void-r"></a>True if the file was successfully deleted; false if the file didn't exist.

**Throws**

- [System.IO.IOException](../System.IO/IOException)
An error occurred during file deletion.

<a name="m-getReadStream-void"></a>
### <code>public Stream getReadStream()</code>
Get a stream to read from this file.

**Returns**

<a name="m-getReadStream-void-r"></a>A stream that supports reading (both synchronously and asynchronously) but not writing or marking.

<a name="m-getWriteStream-bool"></a>
### <code>public Stream getWriteStream([bool](../../Bool) *append*)</code>
Get a stream to write into this file.

**Parameters**

<a name="m-getWriteStream-bool-p-append"></a>
- **append**


**Returns**

<a name="m-getWriteStream-bool-r"></a>A stream that supports writing but not reading or marking.

