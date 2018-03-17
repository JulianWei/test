# Queue <font color="#C8C8C8" size="3">CLASS</font>

A queue to provide data access capability based on first-in-first-out (FIFO) order.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Queue-void"><b>Queue</b></a>|`public Queue()`
|*method*|<a href="#m-enqueue-(unknown)"><b>enqueue</b></a>|`public Void enqueue((unknown))`
|*method*|<a href="#m-dequeue-void"><b>dequeue</b></a>|`public (unknown) dequeue()`
|*method*|<a href="#m-size-void"><b>size</b></a>|`public Integer size()`

## Constructors
<a name="c-Queue-void"></a>
### <code>public Queue()</code>
Create a new queue.
## Fields

## Methods
<a name="m-enqueue-(unknown)"></a>
### <code>public Void enqueue([(unknown)](../../(unknown)) *ele*)</code>
Add a new element to the tail of queue.

**Parameters**

<a name="m-enqueue-(unknown)-p-ele"></a>
- **ele**
The new eleemnt to add. Can be null.

**Returns**

<a name="m-enqueue-(unknown)-r"></a>

<a name="m-dequeue-void"></a>
### <code>public (unknown) dequeue()</code>
Remove an element from the head of queue.

**Returns**

<a name="m-dequeue-void-r"></a>The element to remove; null if the queue is empty. It cannot differentiate between empty queue and null element.

<a name="m-size-void"></a>
### <code>public Integer size()</code>
Get the current size of the queue.

**Returns**

<a name="m-size-void-r"></a>The size of queue.

