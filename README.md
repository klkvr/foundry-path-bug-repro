## README
To test the bug, clone the repro and run `forge compile` in the root.
The ouput will look like this:
```
Compiler run failed:
Error (6480): Derived contract must override function "foo". Two or more base classes define function with same name and parameter types.
 --> src/D.sol:6:1:
  |
6 | contract D is B, C {}
  | ^^^^^^^^^^^^^^^^^^^^^
Note: Definition in "A": 
 --> src/A.sol:4:5:
  |
4 |     function foo() public {}
  |     ^^^^^^^^^^^^^^^^^^^^^^^^
Note: Definition in "A": 
 --> src/a.sol:4:5:
  |
4 |     function foo() public {}
```