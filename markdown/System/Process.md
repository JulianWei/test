# Process <font color="#C8C8C8" size="3">CLASS</font>

The class to represent an OS process.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Process-string-string-ProcessConfig"><b>Process</b></a>|`public Process(string, string[], System.ProcessConfig)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-create-String-String"><b>create</b></a>|`public static Process create(String, String[])`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-getCurrent-void"><b>getCurrent</b></a>|`public static Process getCurrent()`
|*method*|<a href="#m-getName-void"><b>getName</b></a>|`public String getName()`
|*method*|<a href="#m-getArgs-void"><b>getArgs</b></a>|`public String getArgs()`
|*method*|<a href="#m-getEnvArg-String"><b>getEnvArg</b></a>|`public String getEnvArg(String)`
|*method*|<a href="#m-getWriteStream-void"><b>getWriteStream</b></a>|`public Stream getWriteStream()`
|*method*|<a href="#m-getReadStream-void"><b>getReadStream</b></a>|`public Stream getReadStream()`
|*method*|<a href="#m-getErrorStream-void"><b>getErrorStream</b></a>|`public Stream getErrorStream()`
|*method*|<a href="#m-start-void"><b>start</b></a>|`public void start()`
|*method*|<a href="#m-wait-void"><b>wait</b></a>|`public int wait()`
|*method*|<a href="#m-wait-int"><b>wait</b></a>|`public bool wait(int)`
|*method*|<a href="#m-isAlive-void"><b>isAlive</b></a>|`public bool isAlive()`
|*method*|<a href="#m-kill-void"><b>kill</b></a>|`public int kill()`
|*method*|<a href="#m-getExitCode-void"><b>getExitCode</b></a>|`public int getExitCode()`

## Constructors
<a name="c-Process-string-string-ProcessConfig"></a>
### <code>public Process([string](../../String) *name*, [string](../../string) *args*, [ProcessConfig](../System/ProcessConfig) *config*)</code>
Create a process with specific settings.<br><br>
## Fields

## Methods
<a name="m-create-String-String"></a>
### <code>public static Process create([String](../../String) *name*, [String](../../String) *args*)</code>
A facade to create a process with default settings.<br><br>

**Parameters**

<a name="m-create-String-String-p-name"></a>
- **name**
The (path and) name of executable. A simple name will be resolved to anexecutable against the executable paths of OS (for example, the PATH environment variable on Windows and Linux). A path-like name will be resolved against the file system.
<a name="m-create-String-String-p-args"></a>
- **args**
The argument array to pass along to the process. Each element will be treated as a single argument, even if it contains space characters.

**Returns**

<a name="m-create-String-String-r"></a>

<a name="m-getCurrent-void"></a>
### <code>public static Process getCurrent()</code>
Get the Process object for the currently running process.<br><br>Since the returned object represents the current process (a JVM instance on which Julian engine is running), most methods that have modifying behavior are not allowed to call.

**Returns**

<a name="m-getCurrent-void-r"></a>

<a name="m-getName-void"></a>
### <code>public String getName()</code>
Get the name of this process.

**Returns**

<a name="m-getName-void-r"></a>The exactly same name set by the constructor.

<a name="m-getArgs-void"></a>
### <code>public String getArgs()</code>
Get the arguments of this process.

**Returns**

<a name="m-getArgs-void-r"></a>The exactly same argumenst set by the constructor.

<a name="m-getEnvArg-String"></a>
### <code>public String getEnvArg([String](../../String) *name*)</code>
Get the environment variable. This method will only work against the current process object, otherwise it throws.

**Parameters**

<a name="m-getEnvArg-String-p-name"></a>
- **name**
The environment variable's name

**Returns**

<a name="m-getEnvArg-String-r"></a>The environment variable with the specified name. Null if not existing.

<a name="m-getWriteStream-void"></a>
### <code>public Stream getWriteStream()</code>
Get a stream to write to this process. This stream is backed by an OS pipeline. Note, however, if the process was started with inherited IO, or an explicitly set InputStream, then one cannot write to it programmatically and thus this method returns null.<br><br>

**Returns**

<a name="m-getWriteStream-void-r"></a>A stream to write to this process. Null if <a href="../System/ProcessConfig">getInheritedIO</a>is true or <a href="../System/ProcessConfig#m-getInputStream-void">getInputStream</a> is not null.

<a name="m-getReadStream-void"></a>
### <code>public Stream getReadStream()</code>
Get a stream to read from this process. This stream is backed by an OS pipeline. Note, however, if the process was started with inherited IO, or an explicitly set OutputStream, then one cannot read from it programmatically and thus this method returns null.<br><br>

**Returns**

<a name="m-getReadStream-void-r"></a>A stream to read from this process. Null if <a href="../System/ProcessConfig">getInheritedIO</a>is true or <a href="../System/ProcessConfig#m-getOutputStream-void">getOutputStream</a> is not null.

<a name="m-getErrorStream-void"></a>
### <code>public Stream getErrorStream()</code>
Get a stream to read from this process's standard error. This stream is backed by an OS pipeline. Note, however, if the process was started with inherited IO, or an explicitly set ErrorStream, then one cannot read from it programmatically and thus this method returns null.<br><br>

**Returns**

<a name="m-getErrorStream-void-r"></a>A stream to read from this process's standard error. Null if <a href="../System/ProcessConfig">getInheritedIO</a>is true or <a href="../System/ProcessConfig#m-getErrorStream-void">getErrorStream</a> is not null.

<a name="m-start-void"></a>
### <code>public void start()</code>
Start the process. A process can only be started once.

**Returns**

<a name="m-start-void-r"></a>

**Throws**

- [IllegalStateException](../../IllegalStateException)
if the process is not in <a href="../System/ProcessState#e-NOT_STARTED">a state to start</a>.

<a name="m-wait-void"></a>
### <code>public int wait()</code>
Wait for the process to finish.

**Returns**

<a name="m-wait-void-r"></a>The exit code of the process upon its completion.

<a name="m-wait-int"></a>
### <code>public bool wait([int](../../Integer) *millisec*)</code>
Wait, for only specified milliseconds, for the process to finish.

**Parameters**

<a name="m-wait-int-p-millisec"></a>
- **millisec**
The duration, in millisec, to wait for the process to finish.

**Returns**

<a name="m-wait-int-r"></a>True if the process ran to the end within the specified waiting duration.

<a name="m-isAlive-void"></a>
### <code>public bool isAlive()</code>
Check if the process is alive. This method will return true only before <a href="../System/Process#m-start-void">start()</a>, or after either <a href="../System/Process#m-wait-void">wait()</a> or <a href="../System/Process#m-kill-void">kill()</a> is called.

**Returns**

<a name="m-isAlive-void-r"></a>True if the process is still running.

<a name="m-kill-void"></a>
### <code>public int kill()</code>
Kill the process.

**Returns**

<a name="m-kill-void-r"></a>The exit code of the process upon its completion.

**Throws**

- [IllegalStateException](../../IllegalStateException)
if the process <a href="../System/ProcessState#e-NOT_STARTED">has not started yet</a>.

<a name="m-getExitCode-void"></a>
### <code>public int getExitCode()</code>


**Returns**

<a name="m-getExitCode-void-r"></a>

