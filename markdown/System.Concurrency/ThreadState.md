# ThreadState <font color="#C8C8C8" size="3">ENUM</font>

The state of thread.<br><br>A thread runs through several stage in its life cycle. There is only one lifetime for a thread, so it cannot be started twice, even if it's already <a href="../System.Concurrency/ThreadState#e-DONE">done</a>.

## All Members
|**Type**|**Name**|**Value**
|:-------|:-------|:--------
|*constant*|<a href="#e-READY"><b>READY</b></a>|`0`
|*constant*|<a href="#e-RUNNING"><b>RUNNING</b></a>|`1`
|*constant*|<a href="#e-PENDING"><b>PENDING</b></a>|`2`
|*constant*|<a href="#e-DONE"><b>DONE</b></a>|`3`

## Constants
<a name="e-READY"></a>
### <code>public const ThreadState READY = 0</code>
The thread is ready to run.
<a name="e-RUNNING"></a>
### <code>public const ThreadState RUNNING = 1</code>
The thread is running.
<a name="e-PENDING"></a>
### <code>public const ThreadState PENDING = 2</code>
The thread is pending.
<a name="e-DONE"></a>
### <code>public const ThreadState DONE = 3</code>
The thread has finished running, either by normal completion or abortion.

