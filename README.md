# Interdisciplinary Numerical Methods: Parallelism in Julia "Spoke" 18.S192/16.S098

This course covers the the methods available to write high performance parallel codes in Julia, including threading, GPU acceleration, and distributed programming with MPI and Dagger.jl. 

By the end of the course students will be able to use Julia to write write portable and performant code that scales from their laptop CPUs to GPU-enabled supercomputer clusters like NERSC Perlmutter. These skills will be illustrated with a set of applications including scientific codes like Gray-Scott, and training large scale AI applications like LLMs.

## Logistics

**Lectures:** Mondays, Wednesdays, and Fridays 11 AM - 12 AM in room 36-144.

**Prerequisites:** 18.03, 18.06, or equivalents, and some programming experience. You should have taken the [first half-semester numerical "hub" 18.S190/16.S090](https://github.com/mitmath/numerical_hub). Familiarity with Julia is assumed.

**Instructors:** A. Edelman

**Teaching Assistants:** Raye Kimmerer, Eveylne Ringoot, Rabab Alomairy

**Office Hours:** 
- Raye on Tuesdays and Thursdays 12:45PM - 1:45PM on Zoom room `rayegun`.


**Lecture Recordings:** Unfortunately we are not teaching in a recorded classroom this semester.

**Links:** Worth bookmarking:

## Grading

- 6 Homeworks:  90%

- Class Participation: 10%

## Homeworks at a glance

| Homework                                                        | Assigned | Due    | Topic                                              | Solution                                                                             |
| --------------------------------------------------------------- | -------- | ------ | -------------------------------------------------- | ------------------------------------------------------------------------------------ | 
| [HW0](homework/HW0.pdf) | April 2 | April 7 @ 11:59PM | Logistics |

## Lectures at a glance (Lectures being updated.)


#### Homework: [Homework 0 due April 7](homework/HW0.pdf)
#### Lectures:


| #   | Day | Date  | Lecturer          | Topic                                                | Slides / Notes                                                                                                                                    | Notebooks                                                                                                                                                                                                                                                                                                                                                                |
| --- | --- | ----- | ----------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|    |       |          |                            |  **Week 1 - Overview of Parallel Computing**|
| 1  |   M  |  3/31     |      Edelman              |    Parallel Computing may not be what you think, [top500](https://top500.org/), matmul vs matadd | [Intro](https://docs.google.com/presentation/d/1jkJqieNuWh4_Yx6Ura3xiGUc0NmaDK6a6J_zQJfQoEU/edit?usp=sharing)|  [Language Horse Race](https://github.com/mitmath/JuliaComputation/blob/Fall24/notebooks/3_Julia%20is%20fast.ipynb)  |
| 2  |   W  |  4/2     |      Edelman              | If you live with one programming language, you dont know what you are missing   | [Slides](https://docs.google.com/presentation/d/16Zf_SnDNlUmcCdqoaDeyAQmmqpxC66k646DCm3BXt1o/edit?usp=sharing)||                                                             |   
| 3  |   F  |  4/4     |      Kimmerer              |  Allocations and other serial performance tips | | [PerformantSerial Julia Pluto Notebook](https://mitmath.github.io/Parallel-Computing-Spoke/notebooks/PerformantSerialJulia.html)    
|    |       |          |                            |  **Week 2 - Parallelism Concepts and Julia Performance**| 
| 4 |   M  |  4/7    |      Edelman              |   If you see an algorithm that doesn't look like it should be parallel it's probably Parallel Prefix | 
|    |       |          |                            |  **Week 3 -  Multithreading and Multitasking**|    
|    |       |          |                            |  **Week 4 - GPU Computing**|    
|    |       |          |                            |  **Week 5 - GPU Computing**|    
|    |       |          |                            |  **Week 6 - Distributed Computing (MPI + Dagger.jl)**|    
|    |       |          |                            |  **Week 7 - Parallelism Concepts and Julia Performance**|    
    

