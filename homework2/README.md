# Homework 2

### Problem 1

#### (a)
```
Regex: ^[A-Z][0-9][A-Z] [0-9][A-Z][0-9]$
Function: 
var canada = function(string) {
    var re = /^[A-Z][0-9][A-Z] [0-9][A-Z][0-9]$/;
    return re.test(string);
}
```
####(b)
```
Regex:[4]\d{3}([- ]?\d{4}){3}
Function:
var legalVisa = function(string) {
    var re = /[4]\d{3}([- ]?\d{4}){3}/;
    return re.test(string);
}
```

####(c)
```
Regex: [5][1-5]\d{2}([- ]?\d{4}){3}
Function:
var legalMaster = function(string) {
    var re = /[5][1-5]\d{2}([- ]?\d{4}){3}/;
    return re.test(string);
}
```

#### (d)
```
Regex: (^\d+((\_\d)\d*)?#[\dA-F]+(\_[\dA-F]+)*((\.[\dA-F]+(\_[\dA-F]+)*)?#(E[-+]?\d+)?)?)$|(^(([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*))$)
Function: 
var ada = function(string) {
    var re = /(^\d+((\_\d)\d*)?#[\dA-F]+(\_[\dA-F]+)*((\.[\dA-F]+(\_[\dA-F]+)*)?#(E[-+]?\d+)?)?)$|(^(([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*))$)/;
    return re.test(string);
}
```

#### (e)
```
Regex: /((^(?![a-zA-z][Oo][Ss]$))([a-zA-Z])*$)/
Function:
var noThreeLettersEndingWithOS = function(string) {
    var re = /(^(?![a-zA-z][Oo][Ss]$))([a-zA-Z])*/;
    return re.test(string);
}
```

#### (f)
```
Regex: /([0-1]*0000$)/
Function:
var divisibleBySixteen = function(string) {
    var re = /([0-1]*0000$)/;
    return re.test(string);
}
```
#### (g)
```
Regex: /[2-9]|[12]\d|3[0-6]/
Function:
var twothroughthritysix = function(string) {
    var re = /[2-9]|[12]\d|3[0-6]/
    return re.test(string);
}
```

#### (h)
```
Regex: \(\*(.)*\*\)\
Function:
var mlcomment = fucntion (string) {
    var re = \(\*(.)*\*\)
    return re.test(string);
}
```

#### (i)
```
Regex: ^([a-eg-zA-Z][a-zA-Z]*)|(f([a-hj-np-z][a-zA-Z]*)?)|(fi([a-kmo-zA-Z][a-zA-Z]*)?)|(fil([a-df-zA-Z][a-zA-Z]*)?)|file([a-zA-Z]+)|(fo([a-qs-zA-Z][a-zA-Z]*)?)|for([a-zA-Z]+)|(fin([a-ce-zA-Z][a-zA-Z]*)?)|find([a-zA-Z]+)
Function:
var withoutLookAround = function(string) {
    var re = \^([a-eg-zA-Z][a-zA-Z]*)|(f([a-hj-np-z][a-zA-Z]*)?)|(fi([a-kmo-zA-Z][a-zA-Z]*)?)|(fil([a-df-zA-Z][a-zA-Z]*)?)|file([a-zA-Z]+)|(fo([a-qs-zA-Z][a-zA-Z]*)?)|for([a-zA-Z]+)|(fin([a-ce-zA-Z][a-zA-Z]*)?)|find([a-zA-Z]+)\
    return re.test(string);
}
```

#### (j)
```
Regex: /((^(?!file$|find$|for$))([a-zA-Z])*$)/
Function: 
var withLookAround = function(string) {
    var re = /((^(?!file$|find$|for$))([a-zA-Z])*$)/;
    return re.test(string);
}
```
