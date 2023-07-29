# FUNCTIONAL DEPENDENCY
A functional dependency is a relationship between two or more attributes (columns) in a table, where the value of one attribute uniquely determines the value of another attribute.

In other words, knowing the value of one attribute allows you to predict the value of another attribute with certainty.

## TYPES OF FUNCTIONAL DEPENDENCY

**FULL FUNCTIONAL DEPENDENCY**

B is fully dependent on A if **B depends on all the attributes in A**, and **removing any attribute** from A **would break the dependency**.

**PARTIAL FUNCTIONAL DEPENDENCY**

B is partially dependent on A if **B depends on only a part of A**, and removing certain attributes from A **would not break the dependency**.

**TRIVIAL FUNCTIONAL DEPENDENCY**

A functional dependency A -> B is considered trivial if **B is a subset of A**.  <br>
Here B is dependent attribute and A is determinant attribute, **providing no new information**.

**NON-TRIVIAL FUNCTIONAL DEPENDENCY**

A functional dependency A -> B is considered non-trivial if **B is not a subset of A**. <br>
Here B is dependent attribute and A is determinant attribute, **providing new information**.

## RULES OF FUNCTIONAL DEPENDENCY - ARMSTRONG'S AXIOMS
Armstrong's axioms are a set of rules that form the foundation for reasoning about functional dependencies (FDs) in a relational database. These axioms help to derive new FDs from given FDs

**Reflexivity (Augmentation Rule)**

If Y is functionally dependent on X, then adding any attributes Z to X does not change the functional dependency. <br>
In other words, if X -> Y holds, then XZ -> Y also holds.

**Augmentation (Additive Rule)**

If X -> Y holds, then adding the same attribute Z to both sides of the functional dependency preserves its validity. <br>
In other words, if X -> Y holds, then X -> YZ also holds.

**Transitivity (Transitive Rule)**

If X -> Y and Y -> Z both hold, then we can infer the transitive dependency X -> Z. <br>
In other words, if X -> Y and Y -> Z hold, then X -> Z also holds.
