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

Here is the description of the benchmarks for ASCON. 

**Goal:** find the number of active Sboxes for ... 

For the fixed model, we prepared [model1](/models/MD/test) 

For bounds against differential cryptanalysis,it has been proven that there exist at least 15 active S-boxes for 3 rounds while it's 13 for bounds against linear cryptanalysis.We provide some fixed models of searching for the minimum number of active S-boxes for 3 rounds.We list them here:

| Target | Model    | Solver  | Time (s)   | Optimization methods |
| --------| -------- | ------- |------- | ------- |
| ASCON   | [Diff_R3_A14_Seq](/models/ASCON/Diff_R3_A14_Seq.cnf)  | kissat  | 2449  |   | 
| ASCON   | [Diff_R3_A14_kmTotal](/models/ASCON/Diff_R3_A14_kmTotal.cnf)  | kissat  | 2618  |    | 
| ASCON   | [Diff_R3_A14_Sort](/models/ASCON/Diff_R3_A14_Sort.cnf)  | kissat  | 3529  |    | 
| ASCON   | [Diff_R3_A14_mTotal](/models/ASCON/Diff_R3_A14_mTotal.cnf)  | kissat  | 3531  |    | 
| ASCON   | [Diff_R3_A14_Total](/models/ASCON/Diff_R3_A14_Total.cnf)  | kissat  | 3999  |    | 
| ASCON   | [Diff_R3_A14_Cardnet](/models/ASCON/Diff_R3_A14_Cardnet.cnf)  | kissat  | 6659  |    |

| Target | Model    | Solver  | Time (s)   | Optimization methods |
| --------| -------- | ------- |------- | ------- |
| ASCON   | [Linear_R3_A12_Seq](/models/ASCON/Linear_R3_A12_Seq.cnf)  | kissat  | 516  |   | 
| ASCON   | [Linear_R3_A12_kmTotal](/models/ASCON/Linear_R3_A14_kmTotal.cnf)  | kissat  | 551  |    | 
| ASCON   | [Linear_R3_A12_Total](/models/ASCON/Linear_R3_A14_Total.cnf)  | kissat  | 677  |    | 
| ASCON   | [Linear_R3_A12_mTotal](/models/ASCON/Linear_R3_A14_mTotal.cnf)  | kissat  | 690  |    | 
| ASCON   | [Linear_R3_A12_Cardnet](/models/ASCON/Linear_R3_A14_Cardnet.cnf)  | kissat  |  728 |    | 
| ASCON   | [Linear_R3_A12_Sort](/models/ASCON/Linear_R3_A14_Sort.cnf)  | kissat  | 746  |    | 
