# ProcessState <font color="#C8C8C8" size="3">ENUM</font>

The state of a process.<br><br>A process can only go through these states in a single direction. Once a process is terminated it cannot be started again.

## All Members
|**Type**|**Name**|**Value**
|:-------|:-------|:--------
|*constant*|<a href="#e-NOT_STARTED"><b>NOT_STARTED</b></a>|`0`
|*constant*|<a href="#e-IN_PROGRESS"><b>IN_PROGRESS</b></a>|`1`
|*constant*|<a href="#e-TERMINATED"><b>TERMINATED</b></a>|`2`

## Constants
<a name="e-NOT_STARTED"></a>
### <code>public const ProcessState NOT_STARTED = 0</code>
The process is not started.
<a name="e-IN_PROGRESS"></a>
### <code>public const ProcessState IN_PROGRESS = 1</code>
The process is in progress.
<a name="e-TERMINATED"></a>
### <code>public const ProcessState TERMINATED = 2</code>
The process is terminated. It might have run to completion or aborted.

