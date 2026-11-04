# Homework 7: Mixed Integer Programming

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is the repository for Homework 7 for [BEE 4750](https://envsys.viveks.me/), taught at [Cornell University](https://cornell.edu) in Fall 2026 by [Vivek Srikrishnan](https://viveks.me).

If enrolled in the class, a PDF of the completed notebook, **with all cells evaluated**, should be submitted to Gradescope *no later* than the due date, at 9:00pm. 50% will be deducted for late submissions, which can be accepted up to 24 hours from the original deadline.

## Learning Objectives

After completing this assignment, students will be able to:

* model a fixed cost, an either/or choice and a conditional decision with binary variables;
* find the best set of on/off decisions for a small problem with `JuMP`;
* explain why an LP relaxation bounds a mixed integer program;
* trace branch and bound by hand, including when a node can be pruned.

## Repository Overview

The repository consists of the following files:

- `hw07.ipynb`: Jupyter Notebook for the homework assignment. This is the only file you should need to edit.
- `hw07.pdf`: PDF version of the homework assignment, if you don't want to rely on the Jupyter Notebook.
- `Project.toml`, `Manifest.toml`: Julia environment files. These should just work, but feel free to add other packages as needed using the `Pkg` package manager. This is the only other file that you might end up making changes to, though you should do this using `Pkg`, not directly.
- `hw07.qmd`: Source file for Jupyter notebook generation. You shouldn't need to or want to touch this; everything is in the `.ipynb` file.
- `LICENSE`: This material is licensed using the MIT license. You can ignore this for working on the problem set.
- `README.md`: This file. You shouldn't need to touch this.
- `.gitignore`: This tells `git` what files to ignore. You shouldn't need to touch this.
- `.devcontainer/`: Settings for opening this repository in GitHub Codespaces (see the course website's assignment workflow page). You shouldn't need to touch this.

## Dependencies

This notebook was written using Julia 1.11.5. Problem 1.5 uses `JuMP.jl` with the `HiGHS.jl` solver. `Plots.jl` is included in case you want to draw the branch-and-bound regions in code.

## Prerequisites

1. [Install Julia](https://julialang.org/downloads/) before beginning this assignment. This notebook was developed with version 1.11.5, but any 1.11.x should work (there could be some issues with other versions, depending on what's changed).
2. If necessary, [install git](https://happygitwithr.com/install-git.html) and [create a GitHub account](https://github.com).
3. [Clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). I recommend doing this in a dedicated `BEE4750/` folder, which can also house homework assignment repositories and lecture notes. You can clone directly into the `BEE4750/` folder.   For Windows (or from another graphical interface), just create a `BEE4750` folder, then a `hw` folder inside of that, then clone into that folder. Or to clone into a `BEE4750/hw` folder, from a command prompt:
    ```bash
    cd BEE4750/
    mkdir hw
    cd hw/
    git clone https://github.com/bee-envsys-cornell/hw07.git
    ```
