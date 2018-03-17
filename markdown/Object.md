# Object <font color="#C8C8C8" size="3">CLASS</font>

Object is the root class in Julian's typing system. All classes are derived from Object.<br><br>The class-based typing system in Julian is foundamentally analogous to that of Java/C#. It only supports single-inheritance so that a class can only have one parent class. If no such parent is specified in the delcaration, Object is used by default. A class, however, can have unlimited number of interfaces. Similarly,  an interface can also extend zero or more interfaces.<br><br>The method calling supports dynamic dispatching. The exact method to be called is dependent on the current runtime type. This can be illustrated by a classical example. Say we have class C and P, where C extends P. Then in the following code snippet,<br><br><code>P p = <font color="#993366">**new**</font> C();<br>p.fun();</code> what is being really called is implementation of fun() in C, should C have really re-implemented that method.<br><br>The members of a class can be categorized to static and non-static, a.k.a. instance-based. Static members can and should be be called from the class itself, while an instance-based member can only be called against the instance. Within the instance method body, one can refer to members of this class by 'this', and those of parent classes by 'super'. Recall, again, that such references are dynamically dispatched, so it's impossible to specify the member provided by a certain ancestor along the inheritance chain.<br><br>New instances of an Object can be created by 'new' operator, which is followed by a constructor call. A constructor may also call other constructors, which can be referenced by either 'this' or 'super' keyword:<br><br><code><font color="#993366">**class**</font> C : P {<br>&nbsp;&nbsp;C() : <font color="#993366">**this**</font>(5){}<br>&nbsp;&nbsp;C(<font color="#993366">**int**</font> i) : <font color="#993366">**super**</font>(i){}<br>}</code> Object is allocated in the heap area and therefore is always passed through references on the call stack. Assiging an object to another merely passes along the reference. The one prominent exception to this is for <a href="../String">String</a>, which is copied by value.<br><br>Object provides a bunch of basic methods with default implementations based on the underlying platform. This means these methods do not have to be implemented by the extending classes, but in certain circumstances such implementation is highly recommeded. manipulation. The original string instance always remain unchanged.<br><br>While Object is the root of class hierarchy, it's not the root of all types. All primitive types and <a href="../Any">Any</a> are not classes. Assigning Object values to primitive typed variables would usually result in illegal assignement exception.<br><br>For more detailed description on Object and typing system in general, see broken-link.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*constructor*|<a href="#c-Object-void"><b>Object</b></a>|`public Object()`
|*method*|<a href="#m-toString-void"><b>toString</b></a>|`public String toString()`
|*method*|<a href="#m-equals-Object"><b>equals</b></a>|`public bool equals(Object)`
|*method*|<a href="#m-hashCode-void"><b>hashCode</b></a>|`public int hashCode()`

## Constructors
<a name="c-Object-void"></a>
### <code>public Object()</code>
Create a new Object instance.
## Fields

## Methods
<a name="m-toString-void"></a>
### <code>public String toString()</code>
Get the string-formed representation for this object.<br><br>It's recommended that a cutomized object have a deterministic string representation, with its purposes up to the implementors. The string may provide a visualized insight into the contents of the object to facilitate developing process, or be essentially the very semantic value that the object is intended to carry.<br><br>If the subclass doesn't override this method, the default implementation is up to the platform. If overriden, the implementation should be idempotent and deterministic.

**Returns**

<a name="m-toString-void-r"></a>A string that represents the runtime value of this object.

<a name="m-equals-Object"></a>
### <code>public bool equals([Object](../Object) *another*)</code>
Determine the logical equality between this object and anther.<br><br>In Julian, with the exception of <a href="../String">string</a>, objects are compared by reference when '=' operator is used. To check the semantic equality based on the internal value contained by the instance, this method should be implemented and called in place of the operator. It's recommended to override this method instead of coming up with a customized equality-check method because this method is also called by a bunch of System classes, such as <a href="System.Collection/Map">Map</a>.<br><br>If the subclass doesn't override this method, the default implementation is to perform equality check by reference. If overriden, the implementation should be idempotent and deterministic.

**Parameters**

<a name="m-equals-Object-p-another"></a>
- **another**
The other object against which the equality is checked.

**Returns**

<a name="m-equals-Object-r"></a>true if the two objects are considered equal, however equality means as far as the types of thetwo participating objects are concerned.

<a name="m-hashCode-void"></a>
### <code>public int hashCode()</code>
Compute a hash code from this object.<br><br>The hash code is used by certain system classes, most prominently <a href="System.Collection/Map">Map</a>, which needs to project an item at a slot in the map based on the hash value. Not meant for cryptographical purpose, the hash code is neither necessarily unique, nor one-directional. However, for the perfomance consideration, a high-quality implementation usually produces less collision than a poor one.<br><br>If the subclass doesn't override this method, the default implementation is up to the platform. If overriden, the implementation should be idempotent and deterministic.

**Returns**

<a name="m-hashCode-void-r"></a>An integer that represents the hash code of this object. Different instances might produce same hash code.

