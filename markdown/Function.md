# Function <font color="#C8C8C8" size="3">CLASS</font>

Function is the base class for all global functions, methods and lambdas defined in Julian.<br><br>Function has the first-class property in Julian. Like all other classes, it inherits <a href="../Object">Object</a>. What sets it apart from other classes is the ability to execute. To invoke a function, use "()" grammar with argument expressions listed between ( and ). For example,<br><br><code>fun(1, <font color="#3300FF">"a"</font>, someVal);</code> Since function is first-class instance, it can be assigned and passed around:<br><br><code><font color="#993366">**void**</font> fun(){};<br><font color="#993366">**var**</font> f = fun;<br>f();</code> The same can be done for methods (both instance and static) and lambdas.<br><br>In general, Function in Julian doesn't enforce a strong typing. When a Function type is declared somewhere, a function instance of any given signature can be passed in. By the time a function is invoked, the arguments will be checked strickly, and when the function returns, the return value's type will also be checked against the declared type. This behavior can be relaxed a little by <a href="../Function#m-invoke-var">dynamic invocation</a>.<br><br>This class is neither instantiate nor extensible. For more detailed description on Function, see broken-link.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------
|*method*|<a href="#m-invoke-var"><b>invoke</b></a>|`public var invoke(Any[])`

## Constructors

## Fields

## Methods
<a name="m-invoke-var"></a>
### <code>public var invoke([var](../Any) *args*)</code>
Invoke the function dynamically.<br><br>When calling a function using Julian's built-in grammar, namely in the form of "fun(a, b)", the arguments are checked for each parameter's type at corresponding position, and the count of arguments are also checked to be same as that of parameters.<br><br>When invoking the method dynamically, however, the count of arguments are not checked. If the arguments are less than required, the missing ones will be initialized with the default value of the declared parameeter type. In the contrast, if the arguments are more than required, the excessive one will be discarded. For the arguments that fall into the range of paramters, their types are still checked as in the normal calling procedure.<br><br>Another property of dynamic invocation is that if the function doesn't return a value (void), a null value will be returned instead.

**Parameters**

<a name="m-invoke-var-p-args"></a>
- **args**
The same arguments that would be passed to the function when calling it normally, except the countof arguments doesn't have to be the same as that of parameters.

**Returns**

<a name="m-invoke-var-r"></a>The same value the function would return when being called normally, except if the function returnsnothing (void), a null will be returned insttead.

