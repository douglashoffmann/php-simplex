# PHP Simplex

The simplex algorithm implemented in PHP. This library is developed as part of the programming assignments of the course ["Linear and Integer Programming"](https://www.coursera.org/course/linearprogramming) on [Coursera](https://www.coursera.org/).

**Work in progress.**

## Data

The data used for testing is provided as course material of ["Linear and Integer Programming"](https://www.coursera.org/course/linearprogramming) on [Coursera](https://www.coursera.org/). The dictionary format for a linear program in standard form

    max c^T x
    s.t. A x <= b
         x >= 0

is as follows:

    [1] m n
    [2] B_1 B_2 ... B_m
    [3] N_1 N_2 ... N_n
    [4] b_1 ... b_m
    [5] a_11 ... a_1n
    [6] a_21 ... a_2n
    ...
    [m + 4] a_m1 ... a_mn
    [m + 5] c_0 c_1 ... c_n
    
The numbers in brackets denote the line numbers such that there is a total of `m + 5` lines where `m` is the number of basic variables and `n` the number of non-basic variables of the dictionary. Further, `B_1` to `B_m` are the indices of the `m` basic variables and `N_1` to `N_n` are the indices of the non-basic variables. The following lines contain the vector `b`, the matrix `A` the current objective value of the dictionary `c_0` (mostly zero) and the vector `c`.

## License

Copyright 2014 David Stutz

The library is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

The library is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.