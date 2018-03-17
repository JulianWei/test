# Function <font color="#C8C8C8" size="3">CLASS</font>

Function is the base class for all global functions, methods and lambdas defined in Julian.<br><br>Function has the first-class property in Julian. Like all other classes, it inherits <a href="../Object">Object</a>. What sets it apart from other classes is the ability to execute. To invoke a function, use "()" grammar with argument expressions listed between ( and ). For example,<br><br><code>fun(1, <font color="#3300FF">"a"</font>, someVal);</code> Since function is first-class instance, it can be assigned and passed around:<br><br><code><font color="#993366">**void**</font> fun(){};<br><font color="#993366">**var**</font> f = fun;<br>f();</code> The same can be done for methods (both instance and static) and lambdas.<br><br>In general, Function in Julian doesn't enforce a strong typing. When a Function type is declared somewhere, a function instance of any given signature can be passed in. By the time a function is invoked, the arguments will be checked strickly, and when the function returns, the return value's type will also be checked against the declared type. This behavior can be relaxed a little by <a href="../Function">dynamic invocation</a>.<br><br>This class is neither instantiate nor extensible. For more detailed description on Function, see broken-link.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------

## Constructors

## Fields

## Methods
