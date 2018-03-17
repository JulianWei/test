# Lock <font color="#C8C8C8" size="3">CLASS</font>

A process-wide lock that controls access to a certain region in code block.<br><br>Julian provides language-level support for using a lock:<br><br><code>&nbsp;&nbsp;&nbsp;<font color="#993366">**var**</font> mylck = <font color="#993366">**new**</font> Lock();<br>&nbsp;&nbsp;&nbsp;lock (mylck) {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... ... <font color="#669966">// critical region guarded by the lock.</font><br>&nbsp;&nbsp;&nbsp;}</code>

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Lock-void"><b>Lock</b></a>|`public Lock()`
|*method*|<a href="#m-lock-void"><b>lock</b></a>|`public void lock()`
|*method*|<a href="#m-unlock-void"><b>unlock</b></a>|`public void unlock()`
|*method*|<a href="#m-wait-void"><b>wait</b></a>|`public bool wait()`
|*method*|<a href="#m-wait-int"><b>wait</b></a>|`public int wait(int)`
|*method*|<a href="#m-notify-void"><b>notify</b></a>|`public void notify()`

## Constructors
<a name="c-Lock-void"></a>
### <code>public Lock()</code>
Create a new lock.
## Fields

## Methods
<a name="m-lock-void"></a>
### <code>public void lock()</code>
Apply the lock from the place where this is called.<br><br>If the lock is held by other threads, this method will block until the lock is secured.

**Returns**

<a name="m-lock-void-r"></a>

<a name="m-unlock-void"></a>
### <code>public void unlock()</code>
Release the lock. Throw <a href="../System/IllegalStateException">IllegalStateException</a> if the lock is not owned by the current thread.

**Returns**

<a name="m-unlock-void-r"></a>

<a name="m-wait-void"></a>
### <code>public bool wait()</code>
Wait until acquiring the lock or getting interrupted.<br><br>

**Returns**

<a name="m-wait-void-r"></a>true if the waiting was interrupted and this thread failed to obtain the lock;false if the lock was successfully acquired.

<a name="m-wait-int"></a>
### <code>public int wait([int](../../Integer) *milliSec*)</code>
Wait until acquiring the lock, timing out, or getting interrupted.<br><br>

**Parameters**

<a name="m-wait-int-p-milliSec"></a>
- **milliSec**
The time to wait on this lock, in milliseconds.

**Returns**

<a name="m-wait-int-r"></a>return time spent on waiting in millisec, which must be less than <a href="m-wait-int-p-milliSec">the argument</a>;or 0 if timed out, or -1 if getting interrupted.

<a name="m-notify-void"></a>
### <code>public void notify()</code>
Notify all the other threads waiting on the lock. The platform will make an arbitrary decision on who will be holding the lock next.<br><br>Throw <a href="../System/IllegalStateException">IllegalStateException</a> if the lock is not owned by the current thread.

**Returns**

<a name="m-notify-void-r"></a>

