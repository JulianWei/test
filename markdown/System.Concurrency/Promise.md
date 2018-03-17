# Promise <font color="#C8C8C8" size="3">CLASS</font>

This class represents a promise that a certain operation will eventually arrive at a conclusion, upon which a result or exception can be demanded.<br><br>The promise is the primary means in Julian to perform asynchronous programming. Its API is heavily inspired by JavaScript. In general, a user creates a Promise with a <a href="../../Function">Function</a>, and continues it with following operations that can be triggered either on successful completion or abortion. The continuation itself is a new promise, thus enabling the creation of the promise chain, which would run on its own thread, without blocking the thread from which the chain is created and invoked.<br><br>Many I/O APIs provides asynchronous methods which return Promises. These API serve as the starting point for most users in their asynchronous programming. However, the programmers may also create their own Promises and even control their completion through a handle. See <a href="../System.Concurrency/DeferredPromise">DeferredPromise</a> for more details.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Promise-Function"><b>Promise</b></a>|`public Promise(Function)`
|*constructor*|<a href="#c-Promise-void"><b>Promise</b></a>|`protected Promise()`
|*field*|<a href="#f-null"><b>null</b></a>|`protected PromiseQueue null`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-start-Function"><b>start</b></a>|`public static Promise start(Function)`
|*method*<font color="#800080"><sup>S</sup></font>|<a href="#m-defer-void"><b>defer</b></a>|`public static DeferredPromise defer()`
|*method*|<a href="#m-then-Function-Function"><b>then</b></a>|`public Promise then(Function, Function)`
|*method*|<a href="#m-then-Function"><b>then</b></a>|`public Promise then(Function)`
|*method*|<a href="#m-error-Function"><b>error</b></a>|`public Promise error(Function)`
|*method*|<a href="#m-fin-Function"><b>fin</b></a>|`public Promise fin(Function)`
|*method*|<a href="#m-getResult-Bool"><b>getResult</b></a>|`public (unknown) getResult(Bool)`
|*method*|<a href="#m-toString-void"><b>toString</b></a>|`public String toString()`

## Constructors
<a name="c-Promise-Function"></a>
### <code>public Promise([Function](../../Function) *s*)</code>
Create a promise and start immediately.<a name="c-Promise-void"></a>
### <code>protected Promise()</code>
Create a promise and but assign no operation to it. Therefore the promise will linger on <a href="../System.Concurrency/PromiseState#e-PENDING">PENDING</a> state.<br><br>This constructor is reserved only for subclasses and is subject to removal in the future.
## Fields
<a name="f-null"></a>
### <code>protected PromiseQueue null</code>

## Methods
<a name="m-start-Function"></a>
### <code>public static Promise start([Function](../../Function) *f*)</code>
A factory method to start a promise with a specified function.

**Parameters**

<a name="m-start-Function-p-f"></a>
- **f**


**Returns**

<a name="m-start-Function-r"></a>A promise that has been kicked off with the given function.

<a name="m-defer-void"></a>
### <code>public static DeferredPromise defer()</code>
A factory method to create a <a href="../System.Concurrency/DeferredPromise">deferred promise</a>, which is now staying on <a href="../System.Concurrency/PromiseState#e-PENDING">PENDING</a> state.

**Returns**

<a name="m-defer-void-r"></a>A promise that is pending.

<a name="m-then-Function-Function"></a>
### <code>public Promise then([Function](../../Function) *s*, [Function](../../Function) *e*)</code>
Continue this promise with one of two function, one for resolution, the other rejection.<br><br>The function to continue with can take up to two arguments: the first one an untyped value which is either the result produced by the previous promise, or exception that faulted the previous promise. The second value is a <a href="../System.Concurrency/PromiseHandle">PromiseHandle</a> referring to the current promise. Since this function is to be invoked dynamically, it's legal to pass any number of arguments, although only the first two will be heeded.

**Parameters**

<a name="m-then-Function-Function-p-s"></a>
- **s**
The function to continue upon resolution.
<a name="m-then-Function-Function-p-e"></a>
- **e**
The function to continue upon rejection.

**Returns**

<a name="m-then-Function-Function-r"></a>A new promise within which one of the two given functions is invoked.

<a name="m-then-Function"></a>
### <code>public Promise then([Function](../../Function) *s*)</code>
Continue this promise with a function on resolution. If this promise eventually rejects, the given function won't run, and the exception will be propagated to the new promise.<br><br>

**Parameters**

<a name="m-then-Function-p-s"></a>
- **s**
The function to continue upon success.

**Returns**

<a name="m-then-Function-r"></a>A new promise within which the given function is invoked, if the current one resolves. If the current one rejects,the exception is propagated to the new promise, which would not run the given function.

<a name="m-error-Function"></a>
### <code>public Promise error([Function](../../Function) *e*)</code>
Continue this promise with a function on rejection. If this promise eventually resolves, the given function won't run, and the result will be propagated to the new promise.<br><br>

**Parameters**

<a name="m-error-Function-p-e"></a>
- **e**


**Returns**

<a name="m-error-Function-r"></a>A new promise within which the given function is invoked, if the current one rejects. If the current one resolves,the result is propagated to the new promise, which would not run the given function.

<a name="m-fin-Function"></a>
### <code>public Promise fin([Function](../../Function) *f*)</code>
Always continue this promise with a function on completion of this promise.

**Parameters**

<a name="m-fin-Function-p-f"></a>
- **f**
The function to continue upon completion

**Returns**

<a name="m-fin-Function-r"></a>A new promise within which the given function is invoked.

<a name="m-getResult-Bool"></a>
### <code>public (unknown) getResult([Bool](../../Bool) *throwOnError*)</code>
Get the result or faulting exception of this promise.<br><br>This method will block if the promise has not completed yet.

**Parameters**

<a name="m-getResult-Bool-p-throwOnError"></a>
- **throwOnError**
true to re-throw the faulting exception if the promise rejected.

**Returns**

<a name="m-getResult-Bool-r"></a>the result, or exception in case of rejection.

<a name="m-toString-void"></a>
### <code>public String toString()</code>


**Returns**

<a name="m-toString-void-r"></a>

