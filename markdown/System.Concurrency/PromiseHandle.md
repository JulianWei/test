# PromiseHandle <font color="#C8C8C8" size="3">CLASS</font>

A handle exposed to the callback to manipulate promise result explicitly.<br><br>The promise normally sets its state by convention. If the function running in the promise completes successfully it will set the promise to <a href="../System.Concurrency/PromiseState#e-RESOLVED">RESOLVED</a>. If the function throws an exception which went unhandled the promise will turn to <a href="../System.Concurrency/PromiseState#e-REJECTED">REJECTED</a>. By the time a follow-up promise runs the state is reset to PENDING, but depending on what continuation function gets invoked the state may get carried over from the previous promise.<br><br>Without explicit interference through the handle, the RESOLVED state will continue to be propagated down the chain, unless the continuation function on success throws; the REJECTED state will do the same, unless the continuation function on error completes successfully.<br><br>Through the handle, however, the continuation logic can explicitly set the state of the current promise. This is useful in many scenarios, such as forcing the abortion without exception-based logic control, or restoring the state in a promise handling a rejected antecedent. Moreover this can be used to control the state of a <a href="../System.Concurrency/DeferredPromise">synthesized promise</a>.<br><br>Once the promise is resolved this way, it cannot be explicitly set to REJECTED through the same handle. However, a following unhandled exception within the same callback may overwrite the state.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*|<a href="#m-resolve-void"><b>resolve</b></a>|`public void resolve()`
|*method*|<a href="#m-resolve-(unknown)"><b>resolve</b></a>|`public void resolve((unknown))`
|*method*|<a href="#m-reject-void"><b>reject</b></a>|`public void reject()`
|*method*|<a href="#m-reject-String"><b>reject</b></a>|`public void reject(String)`
|*method*|<a href="#m-reject-Exception"><b>reject</b></a>|`public void reject(Exception)`

## Constructors

## Fields

## Methods
<a name="m-resolve-void"></a>
### <code>public void resolve()</code>
Resolve the promise controlled by this handle, without setting any data. Calling <a href="../System.Concurrency/Promise#m-getResult-bool">Promise.getResult()</a> will return null.

**Returns**

<a name="m-resolve-void-r"></a>

<a name="m-resolve-(unknown)"></a>
### <code>public void resolve([(unknown)](../../(unknown)) *result*)</code>
Resolve the promise controlled by this handle with specific data.

**Parameters**

<a name="m-resolve-(unknown)-p-result"></a>
- **result**


**Returns**

<a name="m-resolve-(unknown)-r"></a>The end result to settle this promise. Calling <a href="../System.Concurrency/Promise#m-getResult-bool">Promise.getResult()</a> will return it.

<a name="m-reject-void"></a>
### <code>public void reject()</code>
Reject the promise controlled by this handle, with a default cause. Calling <a href="../System.Concurrency/Promise#m-getResult-bool">Promise.getResult()</a> will return or throw a <a href="../System.Concurrency/PromiseRejectedException">PromiseRejectedException</a>.

**Returns**

<a name="m-reject-void-r"></a>

<a name="m-reject-String"></a>
### <code>public void reject([String](../../String) *msg*)</code>
Reject the promise controlled by this handle, with a specified message. Calling <a href="../System.Concurrency/Promise#m-getResult-bool">Promise.getResult()</a> will return or throw a <a href="../System.Concurrency/PromiseRejectedException">PromiseRejectedException</a> that contains this message.

**Parameters**

<a name="m-reject-String-p-msg"></a>
- **msg**
A message to initialize <a href="../System.Concurrency/PromiseRejectedException">PromiseRejectedException</a>.

**Returns**

<a name="m-reject-String-r"></a>

<a name="m-reject-Exception"></a>
### <code>public void reject([Exception](../../Exception) *ex*)</code>
Reject the promise controlled by this handle, with a specified exception. Calling <a href="../System.Concurrency/Promise#m-getResult-bool">Promise.getResult()</a> will return or throw this exception.

**Parameters**

<a name="m-reject-Exception-p-ex"></a>
- **ex**
An exception to set as the cause of rejection.

**Returns**

<a name="m-reject-Exception-r"></a>

