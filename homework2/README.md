# Homework 2

### Problem 1

#### (a)
Regex: [A-Z][0-9][A-Z] [0-9][A-Z][0-9]
Function: 
var canada = function(string) {
    var re = /[A-Z][0-9][A-Z] [0-9][A-Z][0-9]/;
    return re.test(string);
}

#### (b)
Regex: (^\d+((\_\d)\d*)?#[\dA-F]+(\_[\dA-F]+)*((\.[\dA-F]+(\_[\dA-F]+)*)?#(E[-+]?\d+)?)?)$|(^(([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*))$)
Function: 
var ada = function(string) {
    var re = /(^\d+((\_\d)\d*)?#[\dA-F]+(\_[\dA-F]+)*((\.[\dA-F]+(\_[\dA-F]+)*)?#(E[-+]?\d+)?)?)$|(^(([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*))$)/;
    return re.test(string);
}

#### (e)
Regex: /((^(?![a-zA-z][Oo][Ss]$))([a-zA-Z])*$)/
Function:
var noThreeLettersEndingWithOS = function(string) {
    var re = /(^(?![a-zA-z][Oo][Ss]$))([a-zA-Z])*/;
    return re.test(string);
}

#### (f)
Regex: /([0-1]*0000$)/
Function:
var divisibleBySixteen = function(string) {
    var re = /([0-1]*0000$)/;
    return re.test(string);
}

#### (i)
Regex: 

#### (j)
Regex: /((^(?!file$|find$|for$))([a-zA-Z])*$)/
Function: 
var withLookAround = function(string) {
    var re = /((^(?!file$|find$|for$))([a-zA-Z])*$)/;
    return re.test(string);
}