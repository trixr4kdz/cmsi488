# Homework 3

### Problem 1

##### (a) The grammar produces a string w such that w is a member of (a, b)* where the number of a's in the string w are always more than the number of b's.

##### (b) 
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

##### (c) The grammar is not LL(1) because when you are at A ::= 'a' E, the production rule E can then become either E ::= 'a' B or the empty string. 

##### (d) The grammar is ambiguous since, by definition, a string that can be produced using 2 or more different derivation trees is ambiguous. Consider the string 'aaabbaa'. We can produce 2 different derivation trees for the string 'aaabbaa':
```
          S                                                 S
        /   \                                             /   \   
       /     \                                           /     \ 
      A       M                                         A       M
     / \       \                                       / \       \   
    /   \       \                                     /   \       \  
   'a'   E       S                                   'a'   E       S   
         |     /   \                                       |     /   \ 
        ''    /     \                                     ''    /     \
             A       M                                         A       M
            / \       \                                       / \       \
           /   \       \                                     /   \       \
          'a'   E       S                                   'a'   E       S
                |     /   \                                      /|       | \ 
               ''    /     \                                    / |       |  \
                    A       M                                 'a' B       A    M
                   / \                                           /|      / \   |   
                  /   \                                         / |     /   \  ''       
                 'a'   E                                      'b' E   'a'   E
                        \                                        / \         |
                         \                                      /   \        ''
                          S                                   'b'    A
                        /   \                                       / \ 
                       /     \                                     /   \
                      'b'     A                                  'a'    E
                            / | \                                       |
                           /  |  \                                      ''
                        'b'   A   A
                            / |   | \
                           /  |   |  \
                          'a' E  'a'  E
                              |       |
                              ''      ''
```

### Problem 2

##### (a) The grammar is not LL(1) since if at an id, the production can be expanded to either just the id or to a declaration/assignment (or whatever the ':='' Exp does). In other words, the Exp can be Exp --> Term TermTail --> Factor '' --> id, or Exp --> id ':=' Exp.


##### (b) To make it LL(1), we can split Exp into 2 levels of expression such that we have: 
```
Exp  ::=  id ':=' Exp1
Exp1 ::=  Term Termtail
```

##### (c) There doesn't seem to be much difference between this grammar and a PEG (except for the notation) so the PEG equivalent of this grammar is:
```
Exp         <--  id ':=' Exp / Term TermTail
TermTail    <--  ('+' Term TermTail)?
Term        <--  Factor FactorTail
FactorTail  <--  ('*' Factor FactorTail)?
Factor      <--  '(' Exp ')' / id
```

### Problem 3
```
Exp        --> id ':=' Exp1 {Exp.value := id.val := Exp1.value}
Exp1       --> Term {TermTail_2.accumulate := TermTail.accumulate + Term.value} 
                  TermTail_2 {TermTail.value := TermTail_2.value}
TermTail   --> ('+' Term {TermTail_2.accumulate := TermTail.accumulate + Term.value} 
                  TermTail_2 {TermTail.value := TermTail_2.value})?
                  {TermTail.value := TermTail.accumulate}
Term       --> Factor {FactorTail.accumulate := Factor.value} FactorTail {Term.value = FactorTail.value}
FactorTail --> ('*' Factor {FactorTail_2.accumulate := FactorTail.accumulate * Factor.value} 
                  FactorTail_2 {FactorTail.value := FactorTail_2.value})?
Factor     --> '(' Exp ')' {Factor.value := Exp.value} | id {Factor.value := id.value}
```

### Problem 4
```

```