# Stream <font color="#C8C8C8" size="3">INTERFACE</font>

An abstraction of data origin/sink. A stream can support up to three types of operations: reading, writing and repositioning. The user may query these capabilities before using a stream, but can also opt to proceed without pre-checking if willing to handle the error.<br><br>An internal pointer is pointing to the position within the stream where the next operation will start from. If the stream doesn't support repositioning, this pointer will only move forward.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*|<a href="#m-read-void"><b>read</b></a>|`public Byte read()`
|*method*|<a href="#m-read-Byte-Integer-Integer"><b>read</b></a>|`public Integer read(Byte[], Integer, Integer)`
|*method*|<a href="#m-write-Byte"><b>write</b></a>|`public Void write(Byte)`
|*method*|<a href="#m-write-Byte-Integer-Integer"><b>write</b></a>|`public Void write(Byte[], Integer, Integer)`
|*method*|<a href="#m-close-void"><b>close</b></a>|`public Void close()`
|*method*|<a href="#m-flush-void"><b>flush</b></a>|`public Void flush()`
|*method*|<a href="#m-mark-void"><b>mark</b></a>|`public Void mark()`
|*method*|<a href="#m-reset-void"><b>reset</b></a>|`public Void reset()`
|*method*|<a href="#m-skip-Integer"><b>skip</b></a>|`public Integer skip(Integer)`
|*method*|<a href="#m-canRead-void"><b>canRead</b></a>|`public Bool canRead()`
|*method*|<a href="#m-canWrite-void"><b>canWrite</b></a>|`public Bool canWrite()`
|*method*|<a href="#m-canMark-void"><b>canMark</b></a>|`public Bool canMark()`

## Methods
<a name="m-read-void"></a>
### <code>public Byte read()</code>
Read one byte from the stream.<br><br>This will move forward the stream pointer by one. If <a href="../System.IO/Stream#m-canRead-void">canRead()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Returns**

<a name="m-read-void-r"></a>The byte read from the stream. -1 if reaching the end.

<a name="m-read-Byte-Integer-Integer"></a>
### <code>public Integer read([Byte](../../Byte) *buffer*, [Integer](../../Integer) *offset*, [Integer](../../Integer) *count*)</code>
Try to read <a href="m-read-Byte-Integer-Integer-p-count">desired number</a> of bytes from the stream into the given buffer, starting from the <a href="m-read-Byte-Integer-Integer-p-offset">offset</a> and not exceeding the buffer's capacity. This will move forward the stream pointer by the number of bytes actually read. If the stream hits the end, or the buffer runs short of room, before reading the specified count, only those bytes will be read, making the returned value less than the count argument.<br><br>This method moves forward the stream pointer by the count equal to returned value. If <a href="../System.IO/Stream#m-canRead-void">canRead()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Parameters**

<a name="m-read-Byte-Integer-Integer-p-buffer"></a>
- **buffer**
The byte buffer to hold the data to be read from the stream.
<a name="m-read-Byte-Integer-Integer-p-offset"></a>
- **offset**
The offset on buffer to start filling the data in.
<a name="m-read-Byte-Integer-Integer-p-count"></a>
- **count**
The desired number of bytes to read.

**Returns**

<a name="m-read-Byte-Integer-Integer-r"></a>The count of bytes read from the stream. -1 if reaching the end without any bytes read.

<a name="m-write-Byte"></a>
### <code>public Void write([Byte](../../Byte) *data*)</code>
Write one byte to the stream.<br><br>This will move forward the stream pointer by one. If <a href="../System.IO/Stream#m-canWrite-void">canWrite()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Parameters**

<a name="m-write-Byte-p-data"></a>
- **data**
The single byte to write to this stream.

**Returns**

<a name="m-write-Byte-r"></a>

<a name="m-write-Byte-Integer-Integer"></a>
### <code>public Void write([Byte](../../Byte) *buffer*, [Integer](../../Integer) *offset*, [Integer](../../Integer) *count*)</code>
Try to write <a href="m-write-Byte-Integer-Integer-p-count">desired number</a> of bytes into the stream from the given buffer, starting from the <a href="m-write-Byte-Integer-Integer-p-offset">offset</a> and not exceeding the buffer's capacity. This will move forward the stream pointer by the number of bytes actually read. If the buffer hits the end before reading the specified count, only those bytes will be written, making the returned value less than the count argument.<br><br>This method moves forward the stream pointer by the count equal to returned value. If <a href="../System.IO/Stream#m-canWrite-void">canWrite()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Parameters**

<a name="m-write-Byte-Integer-Integer-p-buffer"></a>
- **buffer**
The byte buffer which holds the data to write into the stream.
<a name="m-write-Byte-Integer-Integer-p-offset"></a>
- **offset**
The offset on the buffer from which the data will be pulled.
<a name="m-write-Byte-Integer-Integer-p-count"></a>
- **count**
The desired number of bytes to write.

**Returns**

<a name="m-write-Byte-Integer-Integer-r"></a>The count of bytes written to the stream. 0 if no bytes have been written.

<a name="m-close-void"></a>
### <code>public Void close()</code>
Close the stream. Once the stream is closed it cannot be re-opened.

**Returns**

<a name="m-close-void-r"></a>

<a name="m-flush-void"></a>
### <code>public Void flush()</code>
Flush the stream. This will materialize all the data copy which may so far have only occurred inside in-memory data buffer, which is usually an implementation detail of the stream. It's best practice for the user to call this method between writing calls, as well as at the conclusion of data copy logic, to ensure all the data have effectively flown into the sink.

**Returns**

<a name="m-flush-void-r"></a>

<a name="m-mark-void"></a>
### <code>public Void mark()</code>
Mark the current position of stream. Calling <a href="../System.IO/Stream#m-reset-void">reset()</a> will move the stream pointer to the marked position.<br><br>If <a href="../System.IO/Stream#m-canMark-void">canMark()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Returns**

<a name="m-mark-void-r"></a>

<a name="m-reset-void"></a>
### <code>public Void reset()</code>
Move the stream pointer to the position marked by <a href="../System.IO/Stream#m-mark-void">mark()</a>.<br><br>If <a href="../System.IO/Stream#m-canMark-void">canMark()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Returns**

<a name="m-reset-void-r"></a>

<a name="m-skip-Integer"></a>
### <code>public Integer skip([Integer](../../Integer) *count*)</code>
Instead of reading, try to skip <a href="m-skip-Integer-p-count">desired number</a> of bytes from the stream. This will move forward the stream pointer by the number of bytes actually read. If the stream hits the end before reading the specified count, only those bytes will be skipped, making the returned value less than the count argument.<br><br>This method moves forward the stream pointer by the count equal to returned value. If <a href="../System.IO/Stream#m-canRead-void">canRead()</a> return false, this method will throw <a href="../System.IO/IOException">IOException</a>.

**Parameters**

<a name="m-skip-Integer-p-count"></a>
- **count**
The desired number of bytes to skip.

**Returns**

<a name="m-skip-Integer-r"></a>The count of bytes skipped.  -1 if reaching the end without any bytes skipped.

<a name="m-canRead-void"></a>
### <code>public Bool canRead()</code>
Whether this stream supports reading. This method governs <a href="../System.IO/Stream#m-read-void">read</a>, <a href="../System.IO/Stream">skip</a>.

**Returns**

<a name="m-canRead-void-r"></a>

<a name="m-canWrite-void"></a>
### <code>public Bool canWrite()</code>
Whether this stream supports writing. This method governs <a href="../System.IO/Stream">write</a>.

**Returns**

<a name="m-canWrite-void-r"></a>

<a name="m-canMark-void"></a>
### <code>public Bool canMark()</code>
Whether this stream supports writing. This method governs <a href="../System.IO/Stream#m-mark-void">mark</a>, <a href="../System.IO/Stream#m-reset-void">reset</a>.

**Returns**

<a name="m-canMark-void-r"></a>

