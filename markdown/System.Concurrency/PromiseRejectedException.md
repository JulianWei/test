# PromiseRejectedException <font color="#C8C8C8" size="3">CLASS</font>

The default exception to return or throw upon demand of a rejected promised. This class is mostly used by the system to facilitate faulting process, but a user's promise callback usually throws more specific exceptions.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-PromiseRejectedException-string"><b>PromiseRejectedException</b></a>|`public PromiseRejectedException(string)`

## Constructors
<a name="c-PromiseRejectedException-string"></a>
### <code>public PromiseRejectedException([string](../../String) *msg*)</code>
Create a standard PromiseRejectedException instance. The users, however, usually just fault the promise by throwing a more specific exception.
## Fields

## Methods
