# PageRank Analysis and Link Farm Simulation

This repository contains the implementation and analysis of the PageRank algorithm, focusing on the Stanford University web pages dataset. We explore the convergence of the PageRank vector using different methods and investigate the effects of creating new web pages and link farms to manipulate PageRank values.

## Project Overview

The project is divided into two main parts:

### 1. **PageRank Computation**
   - We compute the PageRank vector `π` using two different methods:
     - **Power Method** (Paragraph 5.1 of the tutorial)
     - **Solving the Linear System** (Gauss-Seidel method as described in Paragraph 5.2)
   - The transition matrix `G = αP + (1−α)/n * I` is constructed based on the connectivity matrix provided in the `Stanweb.dat` file.
   - **Parameters**:
     - Damping factor `α = 0.85` (and `α = 0.99` for comparison).
     - Stopping criterion `τ = 10^-8`.
     - Vector `a` for handling pages with no outgoing links.

### 2. **Link Farm Simulation**
   - We explore how adding new web pages (link farms) affects the PageRank of an existing page. Specifically, we create new pages and analyze different linking structures:
     - **Case 1**: A new page X with no in-links or out-links.
     - **Case 2**: Another page Y is added that links to page X.
     - **Case 3**: A third page Z is added, and we explore different ways to link the pages (X, Y, and Z) to maximize the PageRank of X.
     - **Case 4**: Page X (and potentially Y and Z) is linked to popular, older pages to see if this improves its PageRank.
   - We summarize the observations and discuss strategies for optimizing the PageRank of a new page through manipulation of link farms.

## Tasks and Methodology

### Part 1: PageRank Computation
   - **Power Method**: We iteratively compute the PageRank vector `π` using the power method with a damping factor of `α = 0.85` and stopping criterion `τ = 10^-8`.
   - **Gauss-Seidel Method**: We solve the linear system associated with the PageRank problem using the Gauss-Seidel iterative method.
   - **Comparison**: We compare the results of both methods in terms of accuracy and speed of convergence, and repeat the experiment with `α = 0.99`. Additionally, we analyze whether all components of `π` converge at the same speed.

### Part 2: Link Farm Simulation
   - **Adding Page X**: We add a new page X with no in-links or out-links to the existing web graph and observe how the PageRanks of the old pages are affected.
   - **Adding Page Y**: We add a second page Y that links to page X and observe how this impacts the PageRank of X and the other pages.
   - **Adding Page Z**: We explore different linking strategies for pages X, Y, and Z to maximize the PageRank of X.
   - **Linking to Popular Pages**: We add links from page X (and optionally from Y and Z) to popular pages in the old web graph and examine the effects on PageRank.
   - **Further Optimization**: We propose additional steps to raise the PageRank of X and discuss optimal link farm structures for this purpose.

## Instructions

### Prerequisites

- Python 3.x
- `numpy`, `scipy`, `matplotlib`
- `CVXOPT` package (for solving optimization problems)

### Dataset

The dataset used is `Stanweb.dat`, which contains the connectivity matrix for the Stanford University webpages.

### Running the Code

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/PageRank-LinkFarm-Analysis.git
   cd PageRank-LinkFarm-Analysis
   ```
