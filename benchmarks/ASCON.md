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

For the fixed model, we prepared [model1](\models\ASCON\test) 

For bounds against differential cryptanalysis,it has been proven that there exist at least 15 active S-boxes for 3 rounds.We provide some fixed models of searching for the minimum number of active S-boxes for 3 rounds.We list them here:

| Target | Model    | Solver  | Time (s)   | Optimization methods |
| --------| -------- | ------- |------- | ------- |
| ASCON   | [R3_A14_Seq](/models/ASCON/R3_A14_Seq.cnf)  | kissat  | 2449  |   | 
| ASCON   | [R3_A14_Total](/models/ASCON/R3_A14_Total.cnf)  | kissat  | 3999  |    | 
