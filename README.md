# LLM-Assisted Assertion Generation for RTL Verification

## Overview

This project explores the use of Large Language Models (LLMs) to automatically generate SystemVerilog Assertions (SVA) for RTL designs and validate them using formal verification tools.

The workflow separates **assertion generation** from **formal validation**, allowing generated properties to be checked for correctness, usefulness, and redundancy rather than treating LLM outputs as trusted.

## Methodology

The project pipeline consists of:

1. Providing structured RTL specifications and signal information to an LLM
2. Generating candidate SVA assertions
3. Classifying assertions as safety, liveness, or invariants
4. Validating assertions using SymbiYosys
5. Using counterexamples to refine failing assertions
6. Analyzing correctness, redundancy, usefulness, and coverage

The evaluated RTL designs include modules such as **FIFO, Arbiter, FSM Controller, and simple datapaths**. 

## Tools

- Verilog / SystemVerilog
- SystemVerilog Assertions (SVA)
- SymbiYosys
- Python
- Claude / ChatGPT
- GTKWave

## Evaluation

Generated assertions are analyzed for:

- Correctness
- Consistency
- Completeness
- Trivial or redundant properties
- Bug and corner-case detection
- Improvement after counterexample-based refinement

Formal verification results include **PASS/FAIL outcomes and counterexamples for failing assertions**. 

## Project Goal

The goal is to study how effectively LLMs can assist hardware verification while ensuring that every generated assertion is independently validated using formal methods. 
