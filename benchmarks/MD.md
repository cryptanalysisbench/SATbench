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

Here is the description of the benchmarks for RIPEMD-160.

**Goal:** find the highest probability of the right branch of 42-step RIPEMD-160.

For the fixed model and free solver, we prepared the [test.smt2](https://raw.githubusercontent.com/cryptanalysisbench/SATbench/main/models/MD/test.smt2) for SMT solvers and [test.cnf](../models/MD/42step_right.cnf) for SAT solvers.

For RIPEMD-160 hash function, the most commonly used method for searching differential characteristics is segmented search and concatenation, which often leads to suboptimal characteristics. Therefore, we would like to know if different solvers can be used to accelerate the fixed model and optimize the existing analysis results.

Server Configuration: Ubuntu AMD EPYC 7302 16-Core Processor.

### SMT Solver Results

| Target      | Model                                             | SMT Solver | Command                                                  | Time (s)    | Optimization Methods |
|-------------|---------------------------------------------------|-------------|-----------------------------------------------------------|-------------|-----------------------|
| RIPEMD-160  | [test.smt2](https://raw.githubusercontent.com/cryptanalysisbench/SATbench/main/models/MD/test.smt2)       | stp         | `time stp -p test.smt2 > test.txt &`                     | killed      |                       |
| RIPEMD-160  | [test.smt2](https://raw.githubusercontent.com/cryptanalysisbench/SATbench/main/models/MD/test.smt2)    | boolector   | `time boolector –m test.smt2 > test.txt &`               | > 259200    |                       |
| RIPEMD-160  | [test.smt2](https://raw.githubusercontent.com/cryptanalysisbench/SATbench/main/models/MD/test.smt2)     | bitwuzla    | `time bitwuzla --print-model test.smt2 > test.txt &`     | 108598      |                       |

---

### SAT Solver Results

| Target      | Model                                             | SAT Solver      | Command                                      | Time (s)    | Optimization Methods |
|-------------|---------------------------------------------------|------------------|-----------------------------------------------|-------------|-----------------------|
| RIPEMD-160  | [test.cnf](../models/MD/42step_right.cnf)         | cryptominisat5   | `cryptominisat5 test.cnf > test.txt`          | 30883       |                       |
| RIPEMD-160  | [test.cnf](../models/MD/42step_right.cnf)         | cadical          | `cadical test.cnf > test.txt`                 | > 604800    |                       |
| RIPEMD-160  | [test.cnf](../models/MD/42step_right.cnf)         | kissat           | `kissat test.cnf > test.txt`                  | 32764       |                       |


