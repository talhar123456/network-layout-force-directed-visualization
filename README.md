# network-layout-force-directed-visualization
This repository provides implementations of network layout algorithms using force-directed methods, including both basic and simulated annealing approaches. The project focuses on visualizing network structures and optimizing node placements through energy-based techniques.

## Features

- **Force-Directed Layout**: Implement a force-directed layout algorithm that simulates molecular forces to arrange nodes in a network.
- **Simulated Annealing**: Optimize network layouts by introducing a thermal contribution to the forces and decreasing it over time.
- **Energy Calculation**: Compute and visualize the total energy of the network and track the energy trajectory through iterations.

## Implementation Details

### Force-Directed Layout

- **Initialization**:
  - Implement `init_positions()` to assign random initial positions and set up node forces and charges.

- **Layout Computation**:
  - **Force Calculation**: Implement `calculate_forces()` to compute pairwise forces and total forces for each node.
  - **Node Displacement**: Update node positions using `displace_nodes()` based on computed forces.
  - **Energy Computation**: Calculate the total energy using `compute_energy()`.

### Simulated Annealing

- **Annealing Layout**:
  - Implement `simulated_annealing_layout(iterations)` to add a random thermal force to nodes, gradually decreasing it over iterations.
  - **Optimization Rationale**: Helps in avoiding local minima and achieving a more optimal layout by reducing thermal noise over time.

### Applying the Layout Algorithms

- **Script Execution**:
  - Create `layout_main.py` to apply the layout algorithms to test files like `star.txt`, `star++.txt`, and `dog.txt`.
  - Perform 1000 iterations for both basic and simulated annealing algorithms.
  - Report final energies and visualize node layouts.
  - Compare energy trajectories between the basic and simulated annealing methods.

## Getting Started

### Prerequisites

Make sure you have Python and the following libraries installed:

- `numpy`
- `networkx`
- `matplotlib`

Install these dependencies using pip:

```bash
pip install numpy networkx matplotlib
