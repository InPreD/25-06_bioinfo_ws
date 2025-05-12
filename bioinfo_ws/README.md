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

### Set up unit testing for your functions

- install pytest

  ```bash
  $ pip install pytest
  ```

- add your function to a module at `my_module/my_module.py`
- add your unit test at `my_module/tests/my_module_test.py`
- in the test file import your module `from my_module.my_module import my_function`

---

### First exercise

- go to https://github.com/InPreD/25-06_bioinfo_ws_unit_testing

![width:500px](../img/unit_testing_codespace01.png)

---

### First exercise

![](../img/unit_testing_codespace02.png)

---

### First exercise

- pytest was already installed in the codespace
- the suggested layout was already applied
- create a branch for your work:

  ```bash
  $ git checkout -b unit-tests-<your name>
  ```

- start with the first exercise in `first/tests/first_test.py`
- whenever you are done, commit your changes (use [commit message conventions](https://inpred.github.io/24-03_bioinfo_ws/#19)):

  ```bash
  $ git add first/tests/first_test.py
  $ git commit -m "test: <your commit message>"
  ```

- and we push them to GitHub:

```bash
$ git push --set-upstream origin unit-tests-<your name>
```

---

## 2. Nextflow
