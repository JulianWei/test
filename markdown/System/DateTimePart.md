# DateTimePart <font color="#C8C8C8" size="3">ENUM</font>

The constituent parts of a data time object, in Gregorian calendar.<br><br>Pay particular attention to the index for each part. Both MONTH and DAY are 1-based; HOURS and below are 0-based.

## All Members
|**Type**|**Name**|**Value**
|:-------|:-------|:--------
|*constant*|<a href="#e-YEAR"><b>YEAR</b></a>|`0`
|*constant*|<a href="#e-MONTH"><b>MONTH</b></a>|`1`
|*constant*|<a href="#e-DAY"><b>DAY</b></a>|`2`
|*constant*|<a href="#e-HOUR"><b>HOUR</b></a>|`3`
|*constant*|<a href="#e-MINUTE"><b>MINUTE</b></a>|`4`
|*constant*|<a href="#e-SECOND"><b>SECOND</b></a>|`5`
|*constant*|<a href="#e-MILLISECOND"><b>MILLISECOND</b></a>|`6`

## Constants
<a name="e-YEAR"></a>
### <code>public const DateTimePart YEAR = 0</code>
Year
<a name="e-MONTH"></a>
### <code>public const DateTimePart MONTH = 1</code>
Month (1-12)
<a name="e-DAY"></a>
### <code>public const DateTimePart DAY = 2</code>
Day in a month (1-31)
<a name="e-HOUR"></a>
### <code>public const DateTimePart HOUR = 3</code>
Hour in a day (0-23)
<a name="e-MINUTE"></a>
### <code>public const DateTimePart MINUTE = 4</code>
Minute in an hour (0-59)
<a name="e-SECOND"></a>
### <code>public const DateTimePart SECOND = 5</code>
Second in a minute (0-59)
<a name="e-MILLISECOND"></a>
### <code>public const DateTimePart MILLISECOND = 6</code>
Millisecond in a second (0-999)

