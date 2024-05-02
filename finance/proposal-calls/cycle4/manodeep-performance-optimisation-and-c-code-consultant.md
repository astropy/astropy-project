### Title
Diagnose and improve performance for the Astropy package

### Project Team
Manodeep Sinha, ...

### Project Description

There are currently 63 open issues tagged with the [Performance label](https://github.com/astropy/astropy/issues?q=is%3Aissue+is%3Aopen+label%3APerformance), 
with the oldest issue nearly 8 years old - highlighting that dedicated effort might be necessary to reduce the 
number of open issues. Even within the [Astropy roadmap](https://github.com/astropy/astropy-project/blob/main/roadmap/roadmap.md), 
`Hardware and Performance` are tagged yellow and red, once again showing that dedicated effort is required to improve
how Astropy performs. This project aims to identify and mitigate high-impact performance issues within the Astropy codebase. 

### Project / Work

The proposed project will consist of these two aspects:

- Performance within python code:
There are odd things that can happen with performance. For example, during PyAstro 2018,
we found out that left-multiplying by units was significantly faster than (the usual convention)
right-multiply, i.e., `u.rad * x` was faster than `x * u.rad`. This would involve identifying
alternate python code that speed up existing python code while remaining 100% backwards compatible.
Micro-benchmarks would need to be added to the [benchmarking CI](https://github.com/astropy/astropy/pull/15779)
to catch regressions in the future. 

- C code review:
The astropy source repo has about 30% C code. A quick look shows that most of
the C code is written to be portable and not necessarily for performance. While this was a
good choice previously, the compilers and the supported OS's have improved sufficiently that
C code can now be written to be both *portable* and *performant*. For example, [this line](https://github.com/astropy/astropy/blob/47a8dac8f1dab6ce592be6048f70140adead4e1d/astropy/stats/src/compute_bounds.c#L23)
could easily be vectorised by adding a `#pragma omp simd reduction(+:mean)`, and 
assuming that the compiler is not auto-vectorising magically, that change might lead to 
a dramatic speed boost, certainly for large N. There might be easy performance gains like 
these throughout the C code base. In the ~5 mins that I spent looking at the C code, I have 
noticed another performance issue that I have reported as a new [issue](https://github.com/astropy/astropy/issues/16136. 

As an ancillary benefit, I am also happy to be tagged as a C code reviewer, particularly 
for code changes that (might) affect performance. I will note that such performance improvements 
works nicely with the [CI Benchmarks](https://github.com/astropy/astropy/pull/15779) PR 
from @MridulS and the performance improvements from @neutrinoceros. 

I am saying performance optimisation in the broad sense, and that includes reducing memory requirements, 
e.g., issues like [this reported memory exhaustion](https://github.com/astropy/astropy/issues/14002).

##### What I am unsure about
How to go about identifying which performance issues, when solved, will make the biggest impact 
for the Astropy end-users. For example, this could be identifying ones from the existing issues 
tagged with the performance label. Or are there potential issues that are as yet unknown (convolution, 
sky matching queries etc) that can have a major impact? 

In the second case, it may be that even creating micro-benchmarks for computationally expensive 
functions like convolution/match-coords are useful additions to the benchmark CI jobs. 

### Approximate Budget

I have guesstimated 24 hours as the time required to solve one 
performance issue, broken down as 16 hours (i.e., 2 work-days) for finding 
potential solutions, 6 hours for response to feedback + iterating + getting 
to optimal solution by consensus, and finally 2 hours to get PR approved and 
merged.

I have tentatively estimated 20 hrs/yr to review existing (15 hrs) and new (5 hrs) 
C code for performance issues.

Proposed budget for fixing two known and two unknown performance issues.

| Item                               | Breakdown                                        | Cost                |
|------------------------------------|--------------------------------------------------|----------------------
| Salary (python performance)        | 4 issues/yr * 24 hrs/issue * USD 150/hr          | USD 14.4k/yr        |
| Salary (C-code review)             |                  20 hrs/yr * USD 150/hr          | USD    3k/yr        |
| Travel to USA                      | Airfare (2k) + hotel (1.5k) + Incidentals (0.5k) | USD    4k/yr        |
| Partial salary (during travel)     |    1 week/yr * 20 hrs/week * USD 150/hr          | USD    3k/yr        |
| **Total**                          |                                                  | **USD 24.4k/yr**    |

Minimum feasible budget for fixing one known and one unknown performance issue.

| Item                               | Breakdown                                      | Cost                |
|------------------------------------|------------------------------------------------|----------------------
| Salary (python performance)        | 2 issues/yr * 24 hrs/issue * USD 150/hr        | USD   7.2k/yr       |
| Salary (C-code review)             |                  20 hrs/yr * USD 150/hr        | USD    3k/yr        |
| **Total**                          |                                                | **USD 10.2k/yr**    |


I am happy to work through and iterate on the budget as deemed necessary. 

### Period of Performance

This project is proposed for 3 years (subject to funding availability), starting late-Apr/early-May, 2024. 
