![image](https://github.com/user-attachments/assets/57457cd1-bc08-4361-9b56-70cd0fd8d72f)![image](https://github.com/user-attachments/assets/defeff0d-7db2-4a04-9428-1766d49c2f4d)![image](https://github.com/user-attachments/assets/6900211d-286f-4f63-9992-5d6f34919879)![image](https://github.com/user-attachments/assets/5715fe76-f5ed-499e-a496-f13d7a30fc0d)![image](https://github.com/user-attachments/assets/e3933fa0-8b0a-4f41-93fe-f2924c896389)---
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

For the fixed model and free solver, we prepared the [test.smt](../models/MD/42step_right.smt2) for SMT solvers and [test.cnf](../models/MD/42step_right.cnf) for SAT solvers.

For RIPEMD-160 hash function, the most commonly used method for searching differential characteristics is segmented search and concatenation, which often leads to suboptimal characteristics. Therefore, we would like to know if different solvers can be used to accelerate the fixed model and optimize the existing analysis results.

Server Configuration: Ubuntu AMD EPYC 7302 16-Core Processor.

| Target | Model    | SMT Solver  | Command | Time (s)  | Optimization methods |
| --------| -------- | ------- |------- | ------- | ------- |
| RIPEMD-160 | [test.smt](../models/MD/42step_right.smt2)  | stp  | time stp -p test.smt2 > test.txt & | killed  |   |
| RIPEMD-160 | [test.smt](../models/MD/42step_right.smt2)  | boolector | time boolector –m test.smt2 > test.txt & |  > 259200  |    |
| RIPEMD-160 | [test.smt](../models/MD/42step_right.smt2)  | bitwuzla | time bitwuzla --print-model test.smt2  > test.txt & | 108598  |    | 


| Target | Model    | SAT Solver  | Command | Time (s)  | Optimization methods |
| --------| -------- | ------- |------- | ------- | ------- |
| RIPEMD-160 | [test.cnf](../models/MD/42step_right.cnf)  | cryptominisat5 | cryptominisat5 test.cnf > test.txt | 30883  |   |
| RIPEMD-160 | [test.cnf](../models/MD/42step_right.cnf)  | cadical | cadical test.cnf > test.txt |  > 604800 |    |
| RIPEMD-160 | [test.cnf](../models/MD/42step_right.cnf)  | kissat | kissat test.cnf > test.txt | 32764  |    | 

