---
layout: template
title: Propositional Logic
data: 2022-02-15
author: Omprakash
category: subject

sidebar:
  - name: Proposition
    key: what-is-a-proposition
  - name: Satisfiability
    key: satisfiability
  - name: Argument
    key: what-is-argument
  - name: Connectors
    key: connectors--operators
  - name: Precedence
    key: precedence-of-operators
  - name: Quantifiers
    key: quantifiers
---

# What is a Proposition?

Any statement that is either true or false, is termed as proposition.

There are two laws regarding proposition as follows:

- #### Law of excluded middle

  This law states that a proposition is required to be either true or false but not both.

- #### Law of contradiction

  ```
  True = not False
  False = not True
  ```

- ### Types of proposition:

  - **Atomic Proposition** : Any proposition which cannot be further divded is termed as atomic proposition.

  - **Compound Proposition** : One or more atomic proposition combined to form a compound proposition using _connectors/operators_ (i.e ~, ^, v, ->, <->).

  - `Note:- Both atomic and compound Proposition's are generally termed as Premises`.

  - **Tautology**: A propositional function which is true in every possible case. A tautology is also termed as Valid statement.

  - **Contradiction** : A propositional function which is false in every possible case.

  - **Contingency** : A propositional function which is some time true and sometime false.

### Satisfiability

A statement or a propsoition is said to be satisfiable if its truth table has **atleast one true value**, otherwise statement is unsatisfiable.

`Clearly, Tautology and Contingency are satisfiable whereas Contradiction is unsatisfiable.`

### What is Argument?

Collection of Premises on the basis of which we derive a conclusion is termed as Argument.

<img src="{{ site.baseurl }}/images/propositional_logic/argurement_discrete.png" class="img-fluid mx-auto d-block" alt="" width="400"/>

### Connectors / Operators

- **Negation (~)** : It is a NOT of digital electronics.

<table class = "table table-dark table-sm table-bordered align-middle">
    <thead>
        <tr> 
            <th scope="col">P</th>
            <th scope="col">~P</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>True</td>
            <td>False</td>
        </tr>
        <tr>
            <td>False</td>
            <td>True</td>
        </tr>
    </tbody>
</table>

- **Disjunction (v)** : It is a OR of digital electronics.

<table class = "table table-dark table-sm table-bordered align-middle">
    <thead>
        <tr> 
            <th scope="col">P</th>
            <th scope="col">Q</th>
            <th scope="col">P v Q</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>True</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>True</td>
            <td>False</td>
            <td>True</td>
        </tr>
        <tr>
            <td>False</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>False</td>
            <td>False</td>
            <td>False</td>
        </tr>
    </tbody>
</table>

- **Conjunction (^)** : It is AND of Digital Electronics

<table class = "table table-dark table-sm table-bordered align-middle">
    <thead>
        <tr> 
            <th scope="col">P</th>
            <th scope="col">Q</th>
            <th scope="col">P ^ Q</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>True</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>True</td>
            <td>False</td>
            <td>False</td>
        </tr>
        <tr>
            <td>False</td>
            <td>True</td>
            <td>False</td>
        </tr>
        <tr>
            <td>False</td>
            <td>False</td>
            <td>False</td>
        </tr>
    </tbody>
</table>

- **Implication (->)** : It is also an binary operator. P -> Q, is read as **If P then Q**.

  - With truth table as follows:

<table class = "table table-dark table-sm table-bordered align-middle">
    <thead>
        <tr> 
            <th scope="col">P</th>
            <th scope="col">Q</th>
            <th scope="col">P -> Q</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>True</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>True</td>
            <td>False</td>
            <td>False</td>
        </tr>
        <tr>
            <td>False</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>False</td>
            <td>False</td>
            <td>True</td>
        </tr>
    </tbody>
</table>

- `P -> Q = ~p v Q | If P then Q is equal to Not P OR Q`

- **Bidirectional operator (<->)** :
  - If sigifies if and only if (i.e iff)
  - Work as Ex-NOR of digital electronics
  <table class = "table table-dark table-sm table-bordered align-middle">
      <thead>
          <tr> 
              <th scope="col">P</th>
              <th scope="col">Q</th>
              <th scope="col">P <-> Q</th>
          </tr>
      </thead>
      <tbody>
          <tr>
              <td>True</td>
              <td>True</td>
              <td>True</td>
          </tr>
          <tr>
              <td>True</td>
              <td>False</td>
              <td>Flase</td>
          </tr>
          <tr>
              <td>False</td>
              <td>True</td>
              <td>False</td>
          </tr>
          <tr>
              <td>False</td>
              <td>False</td>
              <td>True</td>
          </tr>
      </tbody>
  </table>

### Precedence of Operators

<table class = "table table-info table-sm table-bordered align-middle">
    <thead>
        <tr> 
            <th scope="col">Operators</th>
            <th scope="col">Name</th>
            <th scope="col">Precedence</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>~</td>
            <td>Negation</td>
            <td>1</td>
        </tr>
        <tr>
            <td>^</td>
            <td>Conjunction</td>
            <td>2</td>
        </tr>
        <tr>
            <td>v</td>
            <td>Disjunctin</td>
            <td>3</td>
        </tr>
        <tr>
            <td>-></td>
            <td>Implication</td>
            <td>4</td>
        </tr>
        <tr>
            <td><-></td>
            <td>Biconditional</td>
            <td>5</td>
        </tr>
    </tbody>
</table>

### Converse, Inverse & Contrapositive

<table class = "table table-info table-sm table-bordered align-middle">
    <tbody>
        <tr>
            <td>Statement</td>
            <td>If p, then q.</td>
            <td> If two angles are Congurent, then they have same measure.</td>
        </tr>
        <tr>
            <td>Converse</td>
            <td>If q, then P.</td>
            <td> If two angles have same measure, then they are congurent.</td>
        </tr>
        <tr>
            <td>Inverse</td>
            <td>If not p, then not q.</td>
            <td> If two angles are not Congurent, then they don't have same measure.</td>
        </tr>
        <tr>
            <td>Contrapositive</td>
            <td>If not q, then not p</td>
            <td> If two angles don't have same measure, then they are not congurent.</td>
        </tr>
    </tbody>
</table>

### Quantifiers

First we have to understand the concept of **Predicates**. One of the downside of propositonal-logic is that we cannot restrict the domain of the subject, predicate's help us to do so.

**Predicate are wriitten as P(x)**, where P is the logic and x is the subject.

Predicates are used alongside quantifiers to express the extent to which a predicate is true over a range(domain) of elements.

There are two types of quantifiers:

1. Universal Quantifier
2. Existential Quantifier

### Some Properties of Quantifiers

<img src="{{ site.baseurl }}/images/propositional_logic/quantifiers_equivalence.jpg" class="img-fluid mx-auto d-block" alt="" width="400"/>

<img src="{{ site.baseurl }}/images/propositional_logic/qunatifiers_equivalence2.jpg" class="img-fluid mx-auto d-block" alt="" width="400"/>

<img src="{{ site.baseurl }}/images/propositional_logic/quantifiers_negation.jpg" class="img-fluid mx-auto d-block" alt="" width="400"/>
