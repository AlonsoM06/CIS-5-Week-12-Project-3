# Project 3 · Fifty students


## Demo video (required)

Paste a link to a short video of you running this assignment (tool + code + run).
Work without a working video link is incomplete.

**Your demo:** https://drive.google.com/file/d/1ciO7ubAfc3W5c0i-hUDBPzZX3n1MMNGs/view?usp=sharing

**Week 12 · Project 3**  
**Theme:** Project 2’s report, on fifty random scores  
**Type:** Cumulative mini project (replaces the lab and the homework this week)

## What to ship
One array of fifty scores. Each score is one student. The starter fills the array with `rand`, the same way Project 2 did. You count the letter grades, print who needs office hours, and report the average. Functions do that work. `main` fills the array, calls the functions, and prints the report.

The numbers change every time the program runs. Do not type scores or names into the file.

## The functions
Use these signatures. The parameter list is the lesson.

```cpp
void countGrades(const int scores[], int n,
                 int& a, int& b, int& c, int& d, int& failing);
double average(const int scores[], int n);
void officeHours(const int scores[], int n, int* failingCount);
```

`countGrades` walks with `for`. It writes the five counts through the references and does not print.

- A is 90 and up
- B is 80 to 89
- C is 70 to 79
- D is 60 to 69
- Failing is below 60

A score of 60 is a D. It does not get an office-hours line. The five counts add up to 50.

`average` returns the mean as a `double`: `sum * 1.0 / n`. It does not print. If `n` is 0, return 0.

`officeHours` walks with `while`. For each score under 60 it prints:

```text
Student at index i needs to come to office hours.
```

`failingCount` is a pointer. When it is not `nullptr`, write how many of those lines you printed through `*failingCount`. When it is `nullptr`, still print the lines, and do not write through the pointer.

`n` is an ordinary copy. Pass `n` with the array. Do not use `sizeof` to discover the length. Put `const` on the array, because these functions only read it.

## Requirements
1. Leave `srand` and the fill loop alone. Every score comes from `rand() % 100`, a value from 0 through 99. Do not type scores or names into the source.
2. Print each index and its score, in order, before the totals.
3. `countGrades` writes A, B, C, D, and failing through `int&`. The five numbers add up to 50. The function does not print.
4. `average` returns the mean and does not print. `main` prints that returned value.
5. `officeHours` prints one line per score under 60, and writes the line count through `int*` when the pointer is not `nullptr`.
6. `main` calls the three functions. The `Failing` count and `Office hours` are the same number.
7. In the README, write a short explanation in your own words. Name the three functions. Say what the references change in `main`, what the pointer writes, what a `nullptr` skips, and why `average` returns a `double`. Under that paragraph, paste the run you actually got.


    // The reference in our code helps change countGrades a, b, c, d, and failing which all = 0. for example, int &a is the same as int a, what happens to &a also happens to a.
   // The pointer *failingcount in officehours stores the address of &lines in our main. So the failing students = 20, &lines will = 20.
   // nullptr skips any invalid arrays pointers so it doesn't fill random stuff.
   // The average returns a double because we declared it as double meaning allowed decimal points. we take the sum * 1.0/n to give us average.
   // The run I got
 [0] 84
[1] 60
[2] 62
[3] 99
[4] 78
[5] 17
[6] 21
[7] 26
[8] 32
[9] 53
[10] 13
[11] 64
[12] 33
[13] 70
[14] 13
[15] 77
[16] 98
[17] 6
[18] 39
[19] 44
[20] 87
[21] 62
[22] 80
[23] 6
[24] 41
[25] 57
[26] 64
[27] 76
[28] 61
[29] 11
[30] 41
[31] 45
[32] 71
[33] 55
[34] 44
[35] 50
[36] 72
[37] 17
[38] 76
[39] 57
[40] 23
[41] 41
[42] 21
[43] 56
[44] 64
[45] 34
[46] 33
[47] 62
[48] 92
[49] 72
A: 3
B: 3
C: 8
D: 8
Failing: 28
Average: 51.2
Students at index 5 needs to come to office hours 
Students at index 6 needs to come to office hours 
Students at index 7 needs to come to office hours 
Students at index 8 needs to come to office hours 
Students at index 9 needs to come to office hours 
Students at index 10 needs to come to office hours 
Students at index 12 needs to come to office hours 
Students at index 14 needs to come to office hours 
Students at index 17 needs to come to office hours 
Students at index 18 needs to come to office hours 
Students at index 19 needs to come to office hours 
Students at index 23 needs to come to office hours 
Students at index 24 needs to come to office hours 
Students at index 25 needs to come to office hours 
Students at index 29 needs to come to office hours 
Students at index 30 needs to come to office hours 
Students at index 31 needs to come to office hours 
Students at index 33 needs to come to office hours 
Students at index 34 needs to come to office hours 
Students at index 35 needs to come to office hours 
Students at index 37 needs to come to office hours 
Students at index 39 needs to come to office hours 
Students at index 40 needs to come to office hours 
Students at index 41 needs to come to office hours 
Students at index 42 needs to come to office hours 
Students at index 43 needs to come to office hours 
Students at index 45 needs to come to office hours 
Students at index 46 needs to come to office hours 
Office hours: 28

## Sample shape
This shows the shape of the report. Your fifty scores are random, so these numbers will not appear.

```text
[0] 91
[1] 58
...
A: 6
B: 9
C: 12
D: 8
Failing: 15
Average: 64.2
Student at index 1 needs to come to office hours.
...
Office hours: 15
```

`Failing` and `Office hours` match. The five counts add up to 50.

## Starter
`assignment-starter.cpp`. The fill, the printing, and the three calls are already wired. Fill in the function bodies. `lab-starter.cpp` is the same file.

## Deliverables
1. Course-visible GitHub repo
2. README — the short explanation, plus the run you got
3. Short demo video: the fifty scores, the five counts, and the office-hours lines, then what the references, the pointer, and the return each did
4. Canvas links

## Scope
No classes, `new` / `delete`, file I/O, or a menu. Strings and structs are week 13. This project does not need them.

## Integrity
- AI = tutor, not ghostwriter
- Fake ownership → zero
- Due: Monday night (not Sunday)
- Discussions (every week): first post Friday, replies Sunday
- Late: course policy (−10%/day unless stated otherwise)

## Rubric (100)

| Criterion | Pts |
|-----------|----:|
| Code submitted that does the work | 50 |
| Video explanation | 50 |
