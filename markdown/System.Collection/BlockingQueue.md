# BlockingQueue <font color="#C8C8C8" size="3">CLASS</font>

A queue with extended capability of blocking on pulling operation until data is available.<br><br>With the <a href="../System.Collection/Queue">ordinary queue</a> the dequeue operation returns immediately with the element at the head, or null if the queue is empty. A blocking queue, however, supports dequeuing with extended waiting time, during which it will put the current thread into a waiting thread. When a new element is added, it will notify the waiting threads, so that the dequeue operation can proceed.  

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-BlockingQueue-void"><b>BlockingQueue</b></a>|`public BlockingQueue()`
|*method*|<a href="#m-pull-Integer-Bool"><b>pull</b></a>|`public (unknown) pull(Integer, Bool)`
|*method*|<a href="#m-enqueue-(unknown)"><b>enqueue</b></a>|`public Void enqueue((unknown))`
|*method*|<a href="#m-dequeue-void"><b>dequeue</b></a>|`public (unknown) dequeue()`

## Constructors
<a name="c-BlockingQueue-void"></a>
### <code>public BlockingQueue()</code>
Create a new blocking queue.
## Fields

## Methods
<a name="m-pull-Integer-Bool"></a>
### <code>public (unknown) pull([Integer](../../Integer) *timeoutInMillisec*, [Bool](../../Bool) *throwIfTimeout*)</code>
Remove an element from the head of queue. If the queue is empty, wait for <a href="m-pull-Integer-Bool-p-timeoutInMillisec">specified duration</a>. If new data becomes available within the duration this method will return successfully. Otherwise it either returns null, or throws, upon expiration.<br><br>This method will send the current thread into waiting state. Use caution to avoid deadlock.

**Parameters**

<a name="m-pull-Integer-Bool-p-timeoutInMillisec"></a>
- **timeoutInMillisec**
The time to wait, in milliseconds.
<a name="m-pull-Integer-Bool-p-throwIfTimeout"></a>
- **throwIfTimeout**
true if to throw out IllegalStateException upon waiting expiration.

**Returns**

<a name="m-pull-Integer-Bool-r"></a>The element to remove; null if the queue is empty. It cannot differentiate between empty queue and null element.

**Throws**

- [IllegalStateException](../../IllegalStateException)
Only if (throwIfTimeout)<a href="m-pull-Integer-Bool-p-throwIfTimeout">throwIfTimeout</a> is true.

<a name="m-enqueue-(unknown)"></a>
### <code>public Void enqueue([(unknown)](../../(unknown)) *ele*)</code>
Add a new element to the tail of queue. This will notify all the threads waiting at the call to <a href="../System.Collection/BlockingQueue">pull</a>.

**Parameters**

<a name="m-enqueue-(unknown)-p-ele"></a>
- **ele**
The new eleemnt to add. Can be null.

**Returns**

<a name="m-enqueue-(unknown)-r"></a>

<a name="m-dequeue-void"></a>
### <code>public (unknown) dequeue()</code>
Remove an element from the head of queue.<br><br>This method preserves the behavior of the <a href="../System.Collection/Queue">parent class</a>. It won't wait on an empty queue, and it will return null if the queue is empty.

**Returns**

<a name="m-dequeue-void-r"></a>The element to remove; null of the queue is empty. It cannot differentiate between empty queue and null element.

