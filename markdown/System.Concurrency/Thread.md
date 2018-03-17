# Thread <font color="#C8C8C8" size="3">CLASS</font>

A program thread.<br><br>A thread is a light-weight execution unit within a process. A thread has its own stack and runs independently from other threads, only subject to thread scheduling controlled by the underlying managed platform or operating system.<br><br>Julian doesn't have a thread manager on its own. The threads are created and are scheduled by the platform (JVM) thread manager. However, except for the main thread, which is the default thread on which the script engine starts execution, all other threads are background threads and will terminate upon completion of the main thread.<br><br>Once started, threads cannot be stopped or suspended. However, they can be interrupted by calling <a href="../System.Concurrency/Thread#m-interrupt-void">interrupt()</a>, yet such events will go unnoticed if the thread's business logic doesn't actively check and react to it. The only real effect an interruption can cause is to force the thread to exit sleeping.<br><br>Threads can synchronized with each other through a particular class: <a href="../System.Concurrency/Lock">Lock</a>. If threads are competing on certain resources, use a lock to guard the critical region.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Thread-Function-string-ThreadPriority"><b>Thread</b></a>|`public Thread(Function, string, System.Concurrency.ThreadPriority)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-create-Function"><b>create</b></a>|`public static Thread create(Function)`
|*method*|<a href="#m-getName-void"><b>getName</b></a>|`public String getName()`
|*method*|<a href="#m-start-void"><b>start</b></a>|`public Void start()`
|*method*|<a href="#m-join-void"><b>join</b></a>|`public Void join()`
|*method*|<a href="#m-interrupt-void"><b>interrupt</b></a>|`public Void interrupt()`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-getCurrent-void"><b>getCurrent</b></a>|`public static Thread getCurrent()`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-sleep-Integer"><b>sleep</b></a>|`public static Bool sleep(Integer)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-checkInterruption-void"><b>checkInterruption</b></a>|`public static Bool checkInterruption()`
|*method*|<a href="#m-getState-void"><b>getState</b></a>|`public ThreadState getState()`

## Constructors
<a name="c-Thread-Function-string-ThreadPriority"></a>
### <code>public Thread([Function](../../Function) *fun*, [string](../../String) *name*, [ThreadPriority](../System.Concurrency/ThreadPriority) *pri*)</code>
Create a thread with specified function, name and priority.
## Fields

## Methods
<a name="m-create-Function"></a>
### <code>public static Thread create([Function](../../Function) *fun*)</code>
A factory method to create a thread with a function. The thread will have a default name and normal priority.

**Parameters**

<a name="m-create-Function-p-fun"></a>
- **fun**
The function to run on this thread.

**Returns**

<a name="m-create-Function-r"></a>A thread ready to start.

<a name="m-getName-void"></a>
### <code>public String getName()</code>
Get the name of this thread.

**Returns**

<a name="m-getName-void-r"></a>Thread's name.

<a name="m-start-void"></a>
### <code>public Void start()</code>
Start the thread.<br><br>Calling this on the current thread will throw <a href="../System/IllegalStateException">IllegalStateException</a>.

**Returns**

<a name="m-start-void-r"></a>

<a name="m-join-void"></a>
### <code>public Void join()</code>
Wait until the specified thread is finished.<br><br>This method will block until the thread finishes. Calling this on the current thread will throw <a href="../System/IllegalStateException">IllegalStateException</a>.

**Returns**

<a name="m-join-void-r"></a>

<a name="m-interrupt-void"></a>
### <code>public Void interrupt()</code>
Send interruption signal to this thread.<br><br>Note the receiving thread must have logic to check this and react accordingly. The sender must not assume such logic exists and therefore shall not solely rely on this to coordinate inter-thread works.

**Returns**

<a name="m-interrupt-void-r"></a>

<a name="m-getCurrent-void"></a>
### <code>public static Thread getCurrent()</code>
Get the Thread object for the currently running thread.

**Returns**

<a name="m-getCurrent-void-r"></a>The thread object representing the current thread (the one on which this method is called)

<a name="m-sleep-Integer"></a>
### <code>public static Bool sleep([Integer](../../Integer) *periodInMillisec*)</code>
Let the current thread sleep for specified duration.

**Parameters**

<a name="m-sleep-Integer-p-periodInMillisec"></a>
- **periodInMillisec**
sleep duration in milliseconds

**Returns**

<a name="m-sleep-Integer-r"></a>true if interrupted, with the interruption flag reset; false if time is up.

<a name="m-checkInterruption-void"></a>
### <code>public static Bool checkInterruption()</code>
Check if the thread has been interrupted. Also reset the interruption flag.

**Returns**

<a name="m-checkInterruption-void-r"></a>true if interrupted, with the interruption flag reset; false if not.

<a name="m-getState-void"></a>
### <code>public ThreadState getState()</code>
Get state of the thread.

**Returns**

<a name="m-getState-void-r"></a>

