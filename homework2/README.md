# Homework 2

### Problem 1

#### (a)
Regex: [A-Z][0-9][A-Z] [0-9][A-Z][0-9]
Function: 

#### (b)
^(([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*))$        This is for decimal literals

([\dA-F][\dA-F#]*)([.][\dA-F#]+)?((E[-+][\dA-F#]+)|(([_][\dA-F#]+)?)*)|^(([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*))$|^#$

(^[\dA-F]+#?[\dA-F]*#?)([.][\dA-F]+#?)?((([_][\dA-F]+#?)?)|(E[-+][\dA-F]+)*$)|^#$
|(^([\d]+)([.][\d]+)?((E[-+]?[\d]+)|(([_][\d]+)?)*)$)|^#$

(^[\dA-F]+#?[\dA-F]*#?)([.][\dA-F]+#?)?((([_][\dA-F]+#?)?)|(E[-+][\dA-F]+))*$|^#$           \\ THis is for the most part the based literals

(^([0-9]+(#[0-9].[0-9]+(_[0-9]*)*)*#[Ee][-+]?[0-9]+)$) The rest of the based literal

#### (e)
Regex: /((^(?![a-zA-z][Oo][Ss]$))([a-zA-Z])*$)/
Function:
var noThreeLettersEndingWithOS = function(string) {
    var re = /(^(?![a-zA-z][Oo][Ss]$))([a-zA-Z])*/g;
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