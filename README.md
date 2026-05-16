# Cellular Automata: Synchronous vs. Sequential Update Schemes

## 1. Project Description

This project presents a computational study of 1D and 2D Cellular Automata (CA), focusing on the profound impact that different update schemes have on system dynamics. The primary goal of the analysis was to compare how patterns evolve when cells are updated simultaneously (synchronous) versus one at a time in a random order (sequential).

The project includes:

- Implementation of 1D Wolfram Elementary Cellular Automata (Rule 30 and Rule 110)
- Implementation of 2D Conway's Game of Life
- Implementation of the 2D Day and Night Automaton
- Application of periodic boundary conditions
- Spacetime diagram generation for 1D automata
- Time series analysis of active populations (`N_alive`) for 2D automata
- Spatial texture and convergence analysis across different initial densities

## 2. Automata Models

The simulations were conducted on three specific types of cellular automata, which are classic models for studying complexity, chaos, and emergent behavior in physics and computer science:

**1. Wolfram Elementary Cellular Automata (1D)**
- **Rule 30:** A Class III automaton known for generating chaotic, pseudo-random patterns.
- **Rule 110:** A Class IV automaton known for complex, localized, particle-like structures (Turing complete).

**2. Conway's Game of Life (2D)**
- A classic cellular automaton where cells survive, die, or are born based on the number of active neighbors in their Moore neighborhood. 

**3. Day and Night Automaton (2D)**
- A highly symmetric 2D totalistic automaton where the rules for life and death are balanced, leading to heavily oscillating "day" and "night" inversions.

## 3. Tech Stack and Methodology

### Tech Stack

- **Python**
- **NumPy** — grid creation, array manipulation, and random state generation
- **Matplotlib** — generating spacetime diagrams, time series plots, and grid snapshots

### Methodology

The workflow followed these main steps:

1. Initializing 1D arrays with single-cell and random binary sequences.
2. Initializing 2D grids with varying random densities (e.g., 10%, 30%, 50%).
3. Implementing custom neighborhood counting functions with periodic boundary conditions.
4. Simulating **Synchronous Updates**: All cells read the previous state and update simultaneously.
5. Simulating **Sequential Random Updates**: Cells are picked randomly and updated one-by-one, immediately affecting the neighbors evaluated after them.
6. Tracking and plotting the active cell count over time for comparison.
7. Generating visual snapshots at specific time steps to analyze spatial textures and structural stability.

## 4. Repository Contents

```text
├── plots/
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   ├── 4.png
│   ├── 5.png
│   ├── 6.png
│   └── 7.png
│
├── cellular_automata_code.ipynb
│
├── report.pdf
│
└── README.md
