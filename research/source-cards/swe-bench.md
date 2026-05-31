# SWE-bench repository and docs

## Title

SWE-bench repository and docs

## Organization or Author

SWE-bench project

## URL

https://github.com/SWE-bench/SWE-bench

## Date Published If Available

ICLR 2024 paper; repository live

## Date Accessed

2026-05-31

## Source Type

Research benchmark and open-source repository

## Reliability Rating

High

## Key Claims

- SWE-bench evaluates models on real-world GitHub software issues.
- The agent receives a codebase and issue and must generate a patch.
- The evaluation harness uses Docker for reproducibility.

## Caveats

- Benchmark scores are not a substitute for local project-specific evals.

## Workflow Implications

- Bug-fix workflow uses reproduce, patch, verify, and report.
- Local evals use golden tasks rather than broad model claims.
- Review evidence matters more than benchmark reputation.

## Where the Source Is Used in the Repo

- `evals/README.md`
- `workflows/bug-fix.md`
