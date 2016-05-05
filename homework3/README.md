# Homework 3

### Problem 1

#### (a) The grammar produces a string w such that w is a member of (a, b)* where the number of a's in the string are always more than the number of b's.

#### (b) 
```
                S
              /   \
             /     \ 
            A       M
           / \      |
         'a' ''     S
                  /   \
                 /     \
                A       ''
              / |  \
             /  |   \    
            /   |    \     
          'b'   A     A
               / \    | \
              /   \   |  \
            'a'   '' 'a'  ''
```

#### (c) The grammar is not LL(1) 

#### (d) The grammar is ambiguous since, by definition, a string that can be produced using 2 or more different derivation trees is ambiguous. Consider the string 'aaabbaa'. We can produce 2 different derivation trees for the string 'aaabbaa':
```
                    S
                  /   \ 
                 /     \
                A       M
               / \       \
              /   \       \
             'a'   E       S
                         /   \
                        /     \
                       A       M
                      / \       \
                     /   \       \
                    'a'   E       S
                                /   \
                               /     \
                              A       M
                             / \       
                            /   \       
                           'a'   E
                                  \     
                                   \
                                    S
                                  /   \
                                 /     \
                                'b'     A
                                      / | \
                                     /  |  \
                                  'b'   A   A
                                      / |   | \
                                     /  |   |  \
                                    'a' E  'a'  E

```

### Problem 2