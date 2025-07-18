---
layout: single
toc: false
classes: wide
sidebar:  
  - title: " "
    image: /assets/images/logo.png
    image_alt: "image"
    nav: "docs"
---

Here is the description of the benchmarks for SHA-256.

**Goal:** find the highest probability of the message expansion of 32-step SHA-256.

For the fixed model and free solver, we prepared the [test.smt2](../models/SHA/test.smt2) for SMT solvers and [test.cnf](../models/SHA/32step_right.cnf) for SAT solvers.

For the SHA-256 hash function, a crucial step in differential analysis is to first search for a relatively complex local collision in the message expansion, where non-zero message differences appear in the middle steps and are then canceled in as many consecutive steps as possible in both forward and backward directions. This often requires carefully crafted conditions with a minimal number of constraints. Therefore, we would like to investigate whether different solvers can be leveraged to accelerate the fixed model and further optimize existing results in the local collision search phase.

Server Configuration: Ubuntu AMD EPYC 7302 16-Core Processor.

### SMT Solver Results

| Target      | Model                                             | SMT Solver  |  threads                 |Command                                                              | Time (s)        | Optimization Methods  |
|:-----------:|:-------------------------------------------------:|:-----------:|:--------:|:----------------------------------------------------------------:|:--------:|:----------------------:|
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | stp         | 1                        |`time stp -p test.smt2 --cryptominisat > test.txt &`                 |          |                       |
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | stp         | 4                        |`time stp -p test.smt2 --cryptominisat > test.txt &`                 |           |                       |
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | stp         | 8                        |`time stp -p test.smt2 --cryptominisat > test.txt &`                 |           |                       |
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | boolector   | 1                        |`time boolector –m test.smt2 > test.txt &`                           |         |                       |
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | bitwuzla    | 1                        |`time bitwuzla --print-model test.smt2 > test.txt &`                 |           |                       |
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | bitwuzla    | 4                        |`time bitwuzla --print-model test.smt2 > test.txt &`                 |           |                       |
| SHA-256     | [test.smt2](../models/MD/test.smt2)               | bitwuzla    | 8                        |`time bitwuzla --print-model test.smt2 > test.txt &`                 |           |                       |

---

### SAT Solver Results

| Target      | Model                                             | SAT Solver       | threads                |Command                                        | Time (s)       | Optimization Methods |
|-------------|---------------------------------------------------|------------------|------------------------|-----------------------------------------------|----------------|-----------------------|
| SHA-256     | [test.cnf](../models/MD/42step_right.cnf)         | cryptominisat5   | 1                      | `cryptominisat5 test.cnf > test.txt`          |           |                       |
| SHA-256     | [test.cnf](../models/MD/42step_right.cnf)         | cryptominisat5   | 4                      | `cryptominisat5 -t 4 test.cnf > test.txt`     |           |                       |
| SHA-256     | [test.cnf](../models/MD/42step_right.cnf)         | cryptominisat5   | 8                      | `cryptominisat5 -t 8 test.cnf > test.txt`     |           |                       |
| SHA-256     | [test.cnf](../models/MD/42step_right.cnf)         | cadical          | 1                      | `cadical test.cnf > test.txt`                 |        |                       |
| SHA-256     | [test.cnf](../models/MD/42step_right.cnf)         | kissat           | 1                      | `kissat test.cnf > test.txt`                  |           |                       |


