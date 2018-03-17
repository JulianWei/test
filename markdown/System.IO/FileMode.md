# FileMode <font color="#C8C8C8" size="3">ENUM</font>

The mode to open a stream from a file.

## All Members
|**Type**|**Name**|**Value**
|:-------|:-------|:--------
|*constant*|<a href="#e-APPEND"><b>APPEND</b></a>|`0`
|*constant*|<a href="#e-CREATE"><b>CREATE</b></a>|`1`
|*constant*|<a href="#e-OPEN"><b>OPEN</b></a>|`2`

## Constants
<a name="e-APPEND"></a>
### <code>public const FileMode APPEND = 0</code>
If file doesn't exist, create one; if it does, append new contents to the end. File is in WRITE mode.
<a name="e-CREATE"></a>
### <code>public const FileMode CREATE = 1</code>
If file doesn't exist, create one; if it does, truncate the contents. File is in WRITE mode.
<a name="e-OPEN"></a>
### <code>public const FileMode OPEN = 2</code>
Open an existing file. If it doesn't exist, throw IOException. File is in READ mode.

