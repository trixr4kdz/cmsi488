#### Problem 1
```
{
    "program": {
        "declare": {
            "vars": ["x", "y"]
        },
        "while": {
            "minus": {
                "varref": {
                    "ref": "y"
                },
                "intlit": {
                    "value": 5
                }
            },
            "declare": {
                "vars": "y"
            },
            "read": {
                "vars": ["x", "y"]
            },
            "assign": {
                "varref": "x",
                "times": {
                    "intlit": {
                        "value": 2
                    },
                    "plus": {
                        "intlit": {
                            "value": 3
                        },
                        "varref": {
                            "ref": "y"
                        }
                    }
                }
            }
        },
        "write": {
            "intlit": {
                "value": 5
            }
        }
    }
}
```

#### Problem 2


Abstract syntax tree
```
                    *
                  /   \
                 -     \
                /       \
               8         5
```
-8 * 5 is similar to the dropping the negation from Exp2 and adding - Exp5 to Exp4 since 
-8 * 5 is different because

#### Problem 3
```

```





