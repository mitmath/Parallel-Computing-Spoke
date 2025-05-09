# Interdisciplinary Numerical Methods: Parallelism in Julia "Spoke" 18.S192/16.S098

This course covers the the methods available to write high performance parallel codes in Julia, including threading, GPU acceleration, and distributed programming with MPI and Dagger.jl. 

By the end of the course students will be able to use Julia to write write portable and performant code that scales from their laptop CPUs to GPU-enabled supercomputer clusters like NERSC Perlmutter. These skills will be illustrated with a set of applications including scientific codes like Gray-Scott, and training large scale AI applications like LLMs.

## Logistics

**Lectures:** Mondays, Wednesdays, and Fridays 11 AM - 12 AM in room 36-144.

**Prerequisites:** 18.03, 18.06, or equivalents, and some programming experience. You should have taken the [first half-semester numerical "hub" 18.S190/16.S090](https://github.com/mitmath/numerical_hub). Familiarity with Julia is assumed.

**Instructors:** A. Edelman

**Teaching Assistants:** Raye Kimmerer (kimmerer@mit.edu), Eveylne Ringoot, Rabab Alomairy

**Office Hours:** 
- Raye on Tuesdays and Thursdays 12:45PM - 1:45PM on Zoom room `rayegun`.


**Lecture Recordings:** Unfortunately we are not teaching in a recorded classroom this semester.

**Links:** Worth bookmarking:

## Grading

- 6 Homeworks:  90%

- Class Participation: 10%

## Homeworks at a glance

| Homework                                                        | Assigned | Due    | Topic                                              | Notes | Solution                                                                             |
| --------------------------------------------------------------- | -------- | ------ | -------------------------------------------------- |------| ------------------------------------------------------------------------------------ | 
| [HW0](homework/HW0.pdf) | April 2 | April 7 @ 11:59PM | Logistics |
| [HW1](homework/HW1.pdf) | April 7 | April 14 @ 11:59PM | Threading | Updated 9/4|
| [HW2](homework/HW2.pdf) / [Perlmutter Instructions](homework/Perlmutter_Instructions.pdf) | April 20 | April 28 @ 11:59PM | Threading | |
| [HW3](homework/HW3.pdf) / [Pluto Notebook](notebooks/Seam_carving_helper.jl) | May 5 | May 10 @ 11:59PM | GPUs, seam carving | |

#### Lectures:


| #   | Day | Date  | Lecturer          | Topic                                                | Slides / Notes                                                                                                                                    | Notebooks                                                                                                                                                                                                                                                                                                                                                                |
| --- | --- | ----- | ----------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|    |       |          |                            |  **Week 1 - Overview of Parallel Computing**|
| 1  |   M  |  3/31     |      Edelman              |    Parallel Computing may not be what you think, [top500](https://top500.org/), matmul vs matadd | [Intro](https://docs.google.com/presentation/d/1jkJqieNuWh4_Yx6Ura3xiGUc0NmaDK6a6J_zQJfQoEU/edit?usp=sharing)|  [Language Horse Race](https://github.com/mitmath/JuliaComputation/blob/Fall24/notebooks/3_Julia%20is%20fast.ipynb)  |
| 2  |   W  |  4/2     |      Edelman              | If you live with one programming language, you dont know what you are missing   | [Slides](https://docs.google.com/presentation/d/16Zf_SnDNlUmcCdqoaDeyAQmmqpxC66k646DCm3BXt1o/edit?usp=sharing)||                                                             |   
| 3  |   F  |  4/4     |      Kimmerer              |  Allocations and other serial performance tips | | [PerformantSerial Julia Pluto Notebook](https://mitmath.github.io/Parallel-Computing-Spoke/notebooks/PerformantSerialJulia.html)    
|    |       |          |                            |  **Week 2 - Parallelism Concepts,Julia Performance, and Multithreading**| 
| 4 |   M  |  4/7    |      Edelman              |   If you see an algorithm that doesn't look like it should be parallel it's probably Parallel Prefix | [Slides](https://github.com/mitmath/18337/blob/master/lecture10/prefix.pptx)  | [reduce,prefix pluto](https://mitmath.github.io/18337/lecture9/reduce_prefix.html)|
| 5 |  W  |   4/9     |   Kimmerer, Ringoot       | Multithreading, hyperthreading, and pipelining   |   [Slides part 1](https://github.com/mitmath/Parallel-Computing-Spoke/blob/main/lectures/Lecture%2004_09_part1.pdf) [Slides part 2](lectures/04_09_2025%20-%20Threading.pdf)| [threading pluto notebook](https://mitmath.github.io/Parallel-Computing-Spoke/notebooks/ThreadingNotebook.html), [JuliaParallel Notebook](https://github.com/JuliaParallel/julia-hpc-tutorial-sc24/blob/main/parts/multithreading/multithreading.ipynb) |
| 6 |  F  |   4/11    |   Edelman       | Prefix Continued  |    |
|    |       |          |                            |  **Week 3 - Attaching to a  supercomputer, Multitasking & Intro GPU**|   
| 7 |  M |   4/14   | Kimmerer, Edelman      | Perlmutter, GPU pictures | [A100 Architecture White Paper](https://images.nvidia.com/aem-dam/en-zz/Solutions/data-center/nvidia-ampere-architecture-whitepaper.pdf)   |
| 8 | W | 4/16 | Alomairy | GPU background |[colab link](https://colab.research.google.com/drive/1d5DhDmU6-0YpmB6MNCoc_TlzTxwQs8Uw?usp=sharing) [gpu slides](https://docs.google.com/presentation/d/1GG7PMXWD4A5citjWOnRm881pS5NtCyRc/edit#slide=id.p1)
| 9 | F | 4/18 | Alomairy, Ringoot| GPU software | [Slides](https://docs.google.com/presentation/d/1GMYKndXzzzzYwu6LUqe0Ga6wPnd9R72w/edit#slide=id.p2) | |
|    |       |          |                            |  **Week 4 - GPU Computing**| 
| 10 | W | 4/23 | Alomairy | GPU Acceleration |  [Slides](https://docs.google.com/presentation/d/1GqkKC3f7f1dcg-X1wcxQd-KYEoQgD-lP/edit#slide=id.p1)| |
| 11 | F | 4/25 | Ringoot | GPU Acceleration |  [Slides](https://docs.google.com/presentation/d/1zqjzfpyOJOEiCR6sjz39_AlcaBZvccbV/edit?usp=sharing&ouid=111707541660722014594&rtpof=true&sd=true)| |
|    |       |          |                            |  **Week 5 - GPU Computing**|    
| 12 | M | 4/28 | Kimmerer / Edelman | The Julia Dream | [Notebook](notebooks/The%20Julia%20HPC%20dream.ipynb) |
| 13 | W | 4/30 | Edelman | Types in Julia | [Notebook](https://mit-c25-fall23.netlify.app/notebooks/7_ptypes.jl)  |
| 13 | W | 4/30 |  |  |   |
| 14 | F | 5/2 | Ringoot | GPU memory | [Slides](https://docs.google.com/presentation/d/1PYBEPSc7uB0zpojgmQhY5bZTHzCevZ3cVfs_DSwaEfk/edit?usp=sharing)  |
|    |       |          |                            |  **Week 6 - Distributed Computing (MPI + Dagger.jl)**|  
| 15 | M | 5/5 |  Samaroo | Dagger 1  | [Slides](https://docs.google.com/presentation/d/1E44THvMGDsZ2EtIApODy5Y7l3BBSD7XL0g1S-Rn8Xnk/edit?usp=sharing)  |
| 16 | W | 5/7 | Samaroo | Dagger 2 |   |
| 17 | F | 5/9|  Samaroo|  Dagger 3| [Slides](https://docs.google.com/presentation/d/1anH0R-7UnkgG9NkaA6E60g4212UrVzkXb7TBadlqevM/edit?usp=sharing)  |
|    |       |          |                            |  **Week 7 - Parallelism Concepts and Julia Performance**|    
 | 18 | M | 5/12 |  |  Class Party?  |   |   

