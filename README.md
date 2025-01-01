# Temporary Simulation Environment

This repository contains a temporary simulation environment for testing and developing robot control algorithms using the UR5e robot model in a MuJoCo physics simulation.

## Overview

The simulation environment provides a simplified setup for:
- UR5e robot arm simulation
- Basic pick and place operations
- Motion planning and execution
- Block manipulation tasks

## Prerequisites

- Python 3.8 or higher
- MuJoCo physics engine
- Required Python packages (see `requirements.txt`)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/CLAIR-LAB-TECHNION/AIR_robots_sim.git
cd AIR_robots_sim
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required packages:
```bash
pip install -r requirements.txt
```

## Key Components

### SimEnv Class
- Main simulation environment
- Handles physics simulation
- Manages robot and object states

### MotionExecutor Class
- Executes robot movements
- Provides high-level movement commands
- Handles pick and place operations

## Common Issues and Solutions

1. **Robot Out of Workspace**
   - Ensure target positions are within workspace limits
   - Check z-height for pick and place operations

2. **Motion Planning Failures**
   - Verify start and goal positions are valid
   - Check for obstacles in the path
