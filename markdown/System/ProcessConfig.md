# ProcessConfig <font color="#C8C8C8" size="3">CLASS</font>

The configuration set to use when spawning a process.<br><br>The configuration object must be fully set before it's used to start a process. Once the process is started any new changes to this object won't affect the behavior of the running process.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*|<a href="#m-setWorkingDir-String"><b>setWorkingDir</b></a>|`public void setWorkingDir(String)`
|*method*|<a href="#m-getWorkingDir-void"><b>getWorkingDir</b></a>|`public String getWorkingDir()`
|*method*|<a href="#m-setInheritedIO-bool"><b>setInheritedIO</b></a>|`public void setInheritedIO(bool)`
|*method*|<a href="#m-isInheritedIO-void"><b>isInheritedIO</b></a>|`public bool isInheritedIO()`
|*method*|<a href="#m-addEnvArg-String-String"><b>addEnvArg</b></a>|`public void addEnvArg(String, String)`
|*method*|<a href="#m-getEnvArgs-void"><b>getEnvArgs</b></a>|`public Map getEnvArgs()`
|*method*|<a href="#m-setInputStream-Stream"><b>setInputStream</b></a>|`public void setInputStream(Stream)`
|*method*|<a href="#m-setOutputStream-Stream"><b>setOutputStream</b></a>|`public void setOutputStream(Stream)`
|*method*|<a href="#m-setErrorStream-Stream"><b>setErrorStream</b></a>|`public void setErrorStream(Stream)`
|*method*|<a href="#m-getInputStream-void"><b>getInputStream</b></a>|`public Stream getInputStream()`
|*method*|<a href="#m-getOutputStream-void"><b>getOutputStream</b></a>|`public Stream getOutputStream()`
|*method*|<a href="#m-getErrorStream-void"><b>getErrorStream</b></a>|`public Stream getErrorStream()`

## Constructors

## Fields

## Methods
<a name="m-setWorkingDir-String"></a>
### <code>public void setWorkingDir([String](../../String) *dir*)</code>
Set working directory of the process.

**Parameters**

<a name="m-setWorkingDir-String-p-dir"></a>
- **dir**


**Returns**

<a name="m-setWorkingDir-String-r"></a>

<a name="m-getWorkingDir-void"></a>
### <code>public String getWorkingDir()</code>
Get working directory of the process.

**Returns**

<a name="m-getWorkingDir-void-r"></a>

<a name="m-setInheritedIO-bool"></a>
### <code>public void setInheritedIO([bool](../../Bool) *shouldInherit*)</code>
Set if the process will inherit the I/O channels from the parent process.<br><br>If inheriting, the process simply directs its standard I/O to the corresponding channels used by the parent process. However, this behavior can be overwritten by explicitly setting a stream to a particular channel, such as <a href="../System/ProcessConfig#m-setInputStream-Stream">setInputStream</a>.<br><br>If intending to redirect I/O from the current process, i.e. programmatically write to the process's input and read from the output, must not set this to true.

**Parameters**

<a name="m-setInheritedIO-bool-p-shouldInherit"></a>
- **shouldInherit**
if true, the subprocess will inherit the I/O channels from the parent process.

**Returns**

<a name="m-setInheritedIO-bool-r"></a>

<a name="m-isInheritedIO-void"></a>
### <code>public bool isInheritedIO()</code>
Get if the process is inheriting the I/O channels from the parent process.

**Returns**

<a name="m-isInheritedIO-void-r"></a>false if not inheriting.

<a name="m-addEnvArg-String-String"></a>
### <code>public void addEnvArg([String](../../String) *key*, [String](../../String) *value*)</code>
Add an environment variable to the process.

**Parameters**

<a name="m-addEnvArg-String-String-p-key"></a>
- **key**
The variable's name.
<a name="m-addEnvArg-String-String-p-value"></a>
- **value**
The variable's value.

**Returns**

<a name="m-addEnvArg-String-String-r"></a>

<a name="m-getEnvArgs-void"></a>
### <code>public Map getEnvArgs()</code>
Get a map whihc contains all environment variables, with their names as the key.

**Returns**

<a name="m-getEnvArgs-void-r"></a>

<a name="m-setInputStream-Stream"></a>
### <code>public void setInputStream([Stream](../../Stream) *stream*)</code>
Set an input stream to be used as the standard input from within the process.<br><br>Setting this value will overwrite the inherited standard input stream by setting <a href="../System/ProcessConfig#m-setInheritedIO-bool">inherited IO</a>.

**Parameters**

<a name="m-setInputStream-Stream-p-stream"></a>
- **stream**
A stream to send input to the process. The stream must be readable.

**Returns**

<a name="m-setInputStream-Stream-r"></a>

<a name="m-setOutputStream-Stream"></a>
### <code>public void setOutputStream([Stream](../../Stream) *stream*)</code>
Set an output stream to be used as the standard output from within the process.<br><br>Setting this value will overwrite the inherited standard output stream by setting <a href="../System/ProcessConfig#m-setInheritedIO-bool">inherited IO</a>.

**Parameters**

<a name="m-setOutputStream-Stream-p-stream"></a>
- **stream**
A stream to take output out of the process. The stream must be writable.

**Returns**

<a name="m-setOutputStream-Stream-r"></a>

<a name="m-setErrorStream-Stream"></a>
### <code>public void setErrorStream([Stream](../../Stream) *stream*)</code>
Set an output stream to be used as the standard error from within the process.<br><br>Setting this value will overwrite the inherited standard error stream by setting <a href="../System/ProcessConfig#m-setInheritedIO-bool">inherited IO</a>.

**Parameters**

<a name="m-setErrorStream-Stream-p-stream"></a>
- **stream**
A stream to take error output out of the process. The stream must be writable.

**Returns**

<a name="m-setErrorStream-Stream-r"></a>

<a name="m-getInputStream-void"></a>
### <code>public Stream getInputStream()</code>
Get the input stream which was set by <a href="../System/ProcessConfig#m-setInputStream-Stream">setInputStream()</a>.

**Returns**

<a name="m-getInputStream-void-r"></a>Null if not set.

<a name="m-getOutputStream-void"></a>
### <code>public Stream getOutputStream()</code>
Get the output stream which was set by <a href="../System/ProcessConfig#m-setOutputStream-Stream">setOutputStream()</a>.

**Returns**

<a name="m-getOutputStream-void-r"></a>Null if not set.

<a name="m-getErrorStream-void"></a>
### <code>public Stream getErrorStream()</code>
Get the output stream which was set by <a href="../System/ProcessConfig#m-setErrorStream-Stream">setErrorStream()</a>.

**Returns**

<a name="m-getErrorStream-void-r"></a>Null if not set.

