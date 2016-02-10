1)
```
{
    "program": {
        "declare": {
            "vars": "x y"
        },
        "while": {
            "minus": {
                "varref: {
                    "ref": "y"
                },
                "intlit": {
                    "value": "5"
                }
            },
            "declare": {
                "vars": "y"
            },
            "read": {
                "vars": "x y"
            },
            "assign": {
                "varref": "x",
                "times": {
                    "intlit": {
                        "value": "2"
                    },
                    "plus": {
                        "intlit": {
                            "value":"3"
                        },
                        "varref": {
                            "ref": "y"
                        }
                    }
                }
            }
        }
        "write": {
            "intlit": {
                "value": "5"
            }
        }
    }
}
```

2)

Abstract syntax tree
```
                    *
                  /   \
                 -     \
                /       \
               8         5
```


3)
```

```





