# FUNCTIONAL DEPENDENCY
A functional dependency is a relationship between two or more attributes (columns) in a table, where the value of one attribute uniquely determines the value of another attribute.

In other words, knowing the value of one attribute allows you to predict the value of another attribute with certainty.

## TYPES OF FUNCTIONAL DEPENDENCY

### FULL FUNCTIONAL DEPENDENCY
B is fully dependent on A if B depends on all the attributes in A, and removing any attribute from A would break the dependency.

### PARTIAL FUNCTIONAL DEPENDENCY
B is partially dependent on A if B depends on only a part of A, and removing certain attributes from A would not break the dependency.

### TRIVIAL FUNCTIONAL DEPENDENCY
A functional dependency A -> B is considered trivial if B is a subset of A.  <br>
Here B is dependent attribute and A is determinant attribute, providing no new information.

### NON-TRIVIAL FUNCTIONAL DEPENDENCY
A functional dependency A -> B is considered non-trivial if B is not a subset of A. <br>
Here B is dependent attribute and A is determinant attribute, providing new information.

## RULES OF 
