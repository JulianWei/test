# FileStream <font color="#C8C8C8" size="3">CLASS</font>

A stream backed by a file as defined on the underlying file system.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-FileStream-string-FileMode"><b>FileStream</b></a>|`public FileStream(string, System.IO.FileMode)`
|*method*|<a href="#m-canRead-void"><b>canRead</b></a>|`public bool canRead()`
|*method*|<a href="#m-canWrite-void"><b>canWrite</b></a>|`public bool canWrite()`
|*method*|<a href="#m-readAsync-byte-int-Function"><b>readAsync</b></a>|`public Promise readAsync(Byte[], int, Function)`
|*method*|<a href="#m-readAllAsync-byte-Function"><b>readAllAsync</b></a>|`public Promise readAllAsync(Byte[], Function)`
|*method*|<a href="#m-canReadAsync-void"><b>canReadAsync</b></a>|`public bool canReadAsync()`

## Constructors
<a name="c-FileStream-string-FileMode"></a>
### <code>public FileStream([string](../../String) *path*, [FileMode](../System.IO/FileMode) *mode*)</code>
Create a file stream with specified path and <a href="../System.IO/FileMode">mode</a>.
## Fields

## Methods
<a name="m-canRead-void"></a>
### <code>public bool canRead()</code>


**Returns**

<a name="m-canRead-void-r"></a>True if the stream was open with <a href="../System.IO/FileMode#e-OPEN">OPEN</a>.

<a name="m-canWrite-void"></a>
### <code>public bool canWrite()</code>


**Returns**

<a name="m-canWrite-void-r"></a>True if the stream was open with <a href="../System.IO/FileMode#e-APPEND">APPEND</a> or <a href="../System.IO/FileMode#e-CREATE">CREATE</a>.

<a name="m-readAsync-byte-int-Function"></a>
### <code>public Promise readAsync([byte](../../Byte) *buffer*, [int](../../Integer) *offset*, [Function](../../Function) *callback*)</code>
(INHERITED DOC)<br><br>Read asynchronously from the stream to the buffer, and invokes callback upon completion.<br><br>This method tries to read as many bytes as possible from the stream into the given buffer, starting from the <a href="m-readAsync-byte-int-Function-p-offset">offset</a> and not exceeding the buffer's capacity. This will move forward the stream pointer by the number of bytes actually read. If the stream hits the end, or the buffer runs short of room before reading the specified count, only those bytes will be read, making the returned value less than the count argument.<br><br>Upon successful completion, the callback function will be invoked. The callback function has signature <code>[Function](../../Function)([int](../../Integer), [PromiseHandle](../System.Concurrency/PromiseHandle))</code>, with first parameter indicating the number of bytes successfully read. If the reading failed, this callback won't be called, and the users must process that with a continuation on the promise itself.<br><br>This method moves forward the stream pointer by the count equal to returned value. If <a href="../System.IO/FileStream#m-canReadAsync-void">canRead()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.<br><br>

**Parameters**

<a name="m-readAsync-byte-int-Function-p-buffer"></a>
- **buffer**
The byte buffer to hold the data which is read off of the stream.
<a name="m-readAsync-byte-int-Function-p-offset"></a>
- **offset**
The offset on buffer to start filling the data in.
<a name="m-readAsync-byte-int-Function-p-callback"></a>
- **callback**
The function to be called upon successful reading. The type of this functionis <code>[Function](../../Function)([int](../../Integer), [PromiseHandle](../System.Concurrency/PromiseHandle))</code>, first parameter indicating the number of bytes successfully read. -1 if reaching the end.

**Returns**

<a name="m-readAsync-byte-int-Function-r"></a>A promise that can be continued on. An on-success callback will take as argument the result returned from the <a href="m-readAsync-byte-int-Function-p-callback">callback</a>; an on-erro callback will take as argument the exception faulting the IO operation.

<a name="m-readAllAsync-byte-Function"></a>
### <code>public Promise readAllAsync([byte](../../Byte) *buffer*, [Function](../../Function) *callback*)</code>
(INHERITED DOC)<br><br>Read asynchronously from the stream to the buffer until the end of stream is hit, and invokes callback upon completion for evertime a chunk of data is read, which usually fills the buffer, except for the last time.<br><br>This method tries to read as many bytes as possible from the stream into the given buffer. Once it reads a chunk of data, it will invoke the callback function, which has signature <code>[Function](../../Function)([int](../../Integer), [PromiseHandle](../System.Concurrency/PromiseHandle))</code>, with first parameter indicating the number of bytes successfully read. If the reading failed, this callback won't be called, and the users must process that with a continuation on the promise itself.<br><br>This method moves forward the stream pointer to the end of stream. If <a href="../System.IO/FileStream#m-canReadAsync-void">canRead()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.<br><br>

**Parameters**

<a name="m-readAllAsync-byte-Function-p-buffer"></a>
- **buffer**
The byte buffer to hold the data which is read off of the stream.
<a name="m-readAllAsync-byte-Function-p-callback"></a>
- **callback**
The function to be called upon successful reading. The type of this functionis <code>[Function](../../Function)([int](../../Integer), [PromiseHandle](../System.Concurrency/PromiseHandle))</code>, first parameter indicating the number of bytes successfully read. -1 if reaching the end. Throughout the promise's life cycle this callback will be invoked multiple times.

**Returns**

<a name="m-readAllAsync-byte-Function-r"></a>A promise that can be continued on. An on-success callback will take as argument the result returned from the <a href="m-readAllAsync-byte-Function-p-callback">callback</a>; an on-erro callback will take as argument the exception faulting the IO operation.

<a name="m-canReadAsync-void"></a>
### <code>public bool canReadAsync()</code>
(INHERITED DOC)<br><br>Whether this stream supports reading. This method governs <a href="../System.IO/FileStream#m-readAsync-byte-int-Function">readAsync</a>, <a href="../System.IO/FileStream#m-readAllAsync-byte-Function">readAllAsync</a>.

**Returns**

<a name="m-canReadAsync-void-r"></a>True if the stream was open with <a href="../System.IO/FileMode#e-OPEN">OPEN</a>.

