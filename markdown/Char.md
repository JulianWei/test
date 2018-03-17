# Char <font color="#C8C8C8" size="3">PRIMITIVE</font>

**Language-level Alias** - <font color="#993366" size="3"><code><b>char</b></code></font>

The char type in Julian language. A char value corresponds to the literal representation of the code point on ASCII table.<br><br>In Julian, the char value can be written in literal form quoted with single quote ('). Usually a single character is enclosed by ' and ', but it's also possible to use back-slash (\) to escape certain control chracaters, among them line feed (\r), carriage return (\n), horizontal tabulation (\t), nul (\0). One can also use octal representation for a character, which takes the form of '\NNN', where N is a digit tnat is between 0 and 7. Note the max value is '~' (or 126 if cast to a byte or an integer).<br><br>char type can be hard-cast to byte or integer value as the index of its code point on ASCII table. For example, 'a' has a numerical value of 97.<br><br>char type can be concatenated to other characters or string value with '+' operator in the literal form of this value.<br><br>char is a primitive type. Therefore it can only be assigned to a variable with same type or an <a href="../Any">untyped</a> variable.
