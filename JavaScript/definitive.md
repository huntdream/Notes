JavaScript identifier must begin with 
```
a letter, an undersocre(_), or a dollar($)
```

reserved words
```
break	delete	function	return	typeof
case	do		if			switch	var
catch	else	in			this	void
continue	flase	instanceof	throw	while
debugger	finally	new		true	with
default		for		null	try
```

Primitive data types
```
Number Boolean	String	Null Undifined	Symbol
```
Any JavaScript value that not belong to them, is an
Object
```
An object is a collection of properties where each property has a name and a value.
```

Any JavaScript value can be converted to a boolean value,
the following values convert to `false`
```
undefined
null
0
-0
NaN
""	// the empty string
```
All the other values convert to `true`

Functions that have no return value return `undefined`

When JavaScript interpreter starts(or when a web browser loads a new page),it creates a new global object and gives it an initial set of properties that define:
- global properties like undefined, Infinity, NaN
- global functions like isNaN(), parseInt(), and eval()
- constructor functions like Date(), RegExp(), String(), Object(), Array()
- global object like Math, JSON

Whenever you try to refer to a property of a String, JavaScript converts the String value to an object as if by calling `new String()`