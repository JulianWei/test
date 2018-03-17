# DateTime <font color="#C8C8C8" size="3">CLASS</font>

Represent a data time in Gregorian calendar.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-DateTime-int-int-int-int-int-int-int"><b>DateTime</b></a>|`public DateTime(int, int, int, int, int, int, int)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-getNow-void"><b>getNow</b></a>|`public static DateTime getNow()`
|*method*|<a href="#m-toString-void"><b>toString</b></a>|`public String toString()`
|*method*|<a href="#m-diff-DateTime"><b>diff</b></a>|`public Integer diff(DateTime)`
|*method*|<a href="#m-getPart-DateTimePart"><b>getPart</b></a>|`public Integer getPart(DateTimePart)`
|*method*|<a href="#m-getYear-void"><b>getYear</b></a>|`public Integer getYear()`
|*method*|<a href="#m-getMonth-void"><b>getMonth</b></a>|`public Integer getMonth()`
|*method*|<a href="#m-getDay-void"><b>getDay</b></a>|`public Integer getDay()`
|*method*|<a href="#m-getHour-void"><b>getHour</b></a>|`public Integer getHour()`
|*method*|<a href="#m-getMinute-void"><b>getMinute</b></a>|`public Integer getMinute()`
|*method*|<a href="#m-getSecond-void"><b>getSecond</b></a>|`public Integer getSecond()`
|*method*|<a href="#m-getMilli-void"><b>getMilli</b></a>|`public Integer getMilli()`

## Constructors
<a name="c-DateTime-int-int-int-int-int-int-int"></a>
### <code>public DateTime([int](../../Integer) *year*, [int](../../Integer) *month*, [int](../../Integer) *day*, [int](../../Integer) *hour*, [int](../../Integer) *minute*, [int](../../Integer) *second*, [int](../../Integer) *milli*)</code>
Create a datatime from each specified part.
## Fields

## Methods
<a name="m-getNow-void"></a>
### <code>public static DateTime getNow()</code>
Get the current local time.

**Returns**

<a name="m-getNow-void-r"></a>

<a name="m-toString-void"></a>
### <code>public String toString()</code>
Convert the time to a default form (yyyy/MM/dd-hh:mm:ss.SSS).

**Returns**

<a name="m-toString-void-r"></a>

<a name="m-diff-DateTime"></a>
### <code>public Integer diff([DateTime](../../DateTime) *another*)</code>
Return the difference in milliseconds (this - another)

**Parameters**

<a name="m-diff-DateTime-p-another"></a>
- **another**
The other datetime to subtract from this one.

**Returns**

<a name="m-diff-DateTime-r"></a>< 0 if the other datetime is later than this one. = 0 if equal; > 0 if earlier.

<a name="m-getPart-DateTimePart"></a>
### <code>public Integer getPart([DateTimePart](../../DateTimePart) *part*)</code>
Get the value of a specified part from this datetime.

**Parameters**

<a name="m-getPart-DateTimePart-p-part"></a>
- **part**
The part of this datetime to return.

**Returns**

<a name="m-getPart-DateTimePart-r"></a>The value of the required part.

<a name="m-getYear-void"></a>
### <code>public Integer getYear()</code>
Get year.

**Returns**

<a name="m-getYear-void-r"></a>

<a name="m-getMonth-void"></a>
### <code>public Integer getMonth()</code>
Get month. Note this value is 1-based, within the range of `[1, 12`].

**Returns**

<a name="m-getMonth-void-r"></a>

<a name="m-getDay-void"></a>
### <code>public Integer getDay()</code>
Get day. Note this value is 1-based, within the range of `[1, 31`].

**Returns**

<a name="m-getDay-void-r"></a>

<a name="m-getHour-void"></a>
### <code>public Integer getHour()</code>
Get hour.

**Returns**

<a name="m-getHour-void-r"></a>

<a name="m-getMinute-void"></a>
### <code>public Integer getMinute()</code>
Get minute.

**Returns**

<a name="m-getMinute-void-r"></a>

<a name="m-getSecond-void"></a>
### <code>public Integer getSecond()</code>
Get second.

**Returns**

<a name="m-getSecond-void-r"></a>

<a name="m-getMilli-void"></a>
### <code>public Integer getMilli()</code>
Get millisecond.

**Returns**

<a name="m-getMilli-void-r"></a>

