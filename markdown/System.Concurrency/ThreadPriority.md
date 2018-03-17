# ThreadPriority <font color="#C8C8C8" size="3">ENUM</font>

The priority of this thread. This setting is heavily dependent on the underlying implementation and thus is mostly used as a hint rather than directive.

## All Members
|**Type**|**Name**|**Value**
|:-------|:-------|:--------
|*constant*|<a href="#e-LOW"><b>LOW</b></a>|`0`
|*constant*|<a href="#e-NORMAL"><b>NORMAL</b></a>|`1`
|*constant*|<a href="#e-HIGH"><b>HIGH</b></a>|`2`

## Constants
<a name="e-LOW"></a>
### <code>public const ThreadPriority LOW = 0</code>
The thread has lower priority.
<a name="e-NORMAL"></a>
### <code>public const ThreadPriority NORMAL = 1</code>
The thread has normal priority. This is the default setting for a thread.
<a name="e-HIGH"></a>
### <code>public const ThreadPriority HIGH = 2</code>
The thread has high priority.

