---
marp: true
theme: default
---

# Bioinformatics session

3rd Annual workshop on bioinformatics and variant interpretation in InPreD

<https://inpred.github.io/25-06_bioinfo_ws/bioinfo_ws>

![bg right](../img/tromso01.png)

---

## 1. Unit testing

---

### What is unit testing?

- test smallest piece of code that can be logically isolated in software application (function, subroutine, method)
- the smaller the better - more granular view of what is going on; also faster
- should not cross systems (database, filesystem, network) -> integration and functional tests

---

### Example

```python
# calculator.py
def add(x, y):
    """add numbers"""
    return x + y
```

```python
# test_calculator.py
import calculator

def test_add():
    assert calculator.add(1, 2) == 3
```

---

### Why do we need unit testing?

- early defect detection
- code quality improvement
- facilitates refactoring
- faster development cycles
- better documentation
- enables more frequent releases

---

### How to design a unit test?

- identify the unit (function, method)
- what is its functionality?
- what is the input (correct and incorrect)?
- how to handle incorrect input? (edge cases, invalid data)
- what does it return?
- positive and negative results should be tested

---

### Example

```python
# calculator.py
def add(x, y):
    """add numbers"""
    return x + y
```

```python
# test_calculator.py
import calculator

def test_add():
    assert calculator.add(1, 2) == 3
```

---

## 2. Nextflow
