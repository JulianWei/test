# Attribute <font color="#C8C8C8" size="3">CLASS</font>

Attribute is a special class type which provides the ability to define meta-data for other ordinary types. Attribute inherits <a href="../Object">Object</a>, but cannot be instantiated directly by 'new' operator. Its use is strictly limited at certain prescribed sites at class and member definition.<br><br>An attribute can contain zero or more fields:<br><br><code><font color="#993366">**attribute**</font> Copyright {<br>&nbsp;&nbsp;<font color="#993366">**string**</font> name;<br>&nbsp;&nbsp;<font color="#993366">**int**</font> year;<br>}</code> And it's used with annotation syntax when defining other types:<br><br><code>[Copyright(name = <font color="#3300FF">"James Kucan"</font>, year=2010)]<br><font color="#993366">**class**</font> ServiceModel {<br>&nbsp;&nbsp;[Copyright(name = <font color="#3300FF">"Larson J. Fisher"</font>, year=2011)]<br>&nbsp;&nbsp;<font color="#993366">**void**</font> report(){<br><br>&nbsp;&nbsp;}<br>}</code> The usage of attributes, such as use-site and repeatability, can be controlled by <a href="System/AttributeType">meta-attribute</a>.<br><br>Julian doesn't enforce the types for fields of attribute, nor what an initializer may contain. When loading a type, all the dependent Attribute types will be loaded ahead of non-Attribute types in a resolved order based their mutual dependencies. This, however, is a best-effort by the engine, which doesn't guarantee the success with regards to that loading order. In fact, due to the nature of attributes, it's possible to cause loading failure because of cross-dependency among attributes and other types. The avoid such failures, it's recommended that only primitive types and system types be used for both the field type and throughout the initializer.<br><br>For more detailed description on Attribute, see broken-link.

## All Members
|**Type**|**Name**|**Signature**
|:-------|:-------|:------------

## Constructors

## Fields

## Methods
