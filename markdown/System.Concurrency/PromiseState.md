# PromiseState <font color="#C8C8C8" size="3">ENUM</font>

The state of a promise.<br><br>A promise goes through a very simple life cycle. It starts with <a href="../System.Concurrency/PromiseState#e-PENDING">PENDING</a>, during which it either runs a business function, or waits to be settled by a handle. The promise eventually gets settled in either of two possible states. If the function runs to end successfully, or the handle calls <a href="../System.Concurrency/PromiseHandle#m-resolve-void">resolve</a>, the promise is <a href="../System.Concurrency/PromiseState#e-RESOLVED">resolved</a>; if the function throws an exception, or the handle calls <a href="../System.Concurrency/PromiseHandle#m-reject-void">reject</a>, the promise ends up <a href="../System.Concurrency/PromiseState#e-REJECTED">rejected</a>.

## All Members
|**Type**|**Name**|**Value**
|:-------|:-------|:--------
|*constant*|<a href="#e-PENDING"><b>PENDING</b></a>|`0`
|*constant*|<a href="#e-RESOLVED"><b>RESOLVED</b></a>|`1`
|*constant*|<a href="#e-REJECTED"><b>REJECTED</b></a>|`2`

## Constants
<a name="e-PENDING"></a>
### <code>public const PromiseState PENDING = 0</code>
The promise is pending to settle.
<a name="e-RESOLVED"></a>
### <code>public const PromiseState RESOLVED = 1</code>
The promise is resolved. A result can be returned now immediately.
<a name="e-REJECTED"></a>
### <code>public const PromiseState REJECTED = 2</code>
The promise is rejected. An exception can be returned now immediately.

