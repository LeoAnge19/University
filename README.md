# University
This repo contains documents related to university courses, projects or insights.

# Q-Learning for Competitive Agents: Attack & Defense in a Grid-World
BSc thesis – Computer and Control Engineering, Sapienza University of Rome (2025)
Supervisor: Prof. Antonio Pietrabissa · Co-supervisor: Danilo Menegatti, PhD
## Overview
Two agents learn opposing strategies in the same environment: an Attacker that must
destroy a target cell and a Defender that must protect it. The project explores
non-cooperative multi-agent reinforcement learning (MARL) with tabular Q-learning.
## Environment
- Grid-world with obstacles (collisions simulate robot damage)
- Actions: 4-directional moves + detonation
- Reward shaping: bonus for effective attack/defense, penalties for collisions and ineffective detonation
## Method
- Tabular Q-learning, ε-greedy policy with decaying exploration, 1000 training episodes
- Alternating training of Attacker and Defender against each other
- Proximity sensor model enabling targeted, effective actions
- Robustness: randomized initial positions of both agents
## Results
- Convergence of Q-tables; learned policies and optimal paths visualized on the map
- The sensor improves both attack precision and defensive pressure
- Strategies remain effective across different initial configurations

# Finite Element Dynamic Analysis of a Truss Bridge
Course yearwork – Dynamics of Mechanical Systems, Politecnico di Milano (A.Y. 2025/26)
## Overview
Structural dynamics study of a steel truss bridge using a 2D finite element beam model.
## Tasks
1. FE mesh valid in 0–30 Hz (safety factor 1.5 on max element length) – 42 nodes, 123 DOF, 67 beams
2. Natural frequencies and mode shapes (5 modes: 2.32 – 26.46 Hz)
3. Frequency response functions (0–30 Hz, 0.01 Hz step)
4. Response to seismic vertical ground motion at the supports
5. Resonance analysis for a train of moving concentrated loads at constant speed
6. Structural modification: −15% peak vertical acceleration with limited added mass

# Cascaded Speed Control of the Milan "Carrelli 1928" Tram
Course project – Dynamics of Electrical Machines and Drives, Politecnico di Milano (A.Y. 2025/26)
## Overview
Modeling and closed-loop speed control of a historic tramway vehicle (25 t fully loaded,
up to 42 km/h). The four series-excited DC traction motors are modeled as one
equivalent separately excited DC machine.
## Control architecture
- Outer speed loop (ω_c ≈ 1.5 rad/s) → torque / armature-current reference
- Inner armature current loop (ω_c = 200 rad/s) with back-EMF feedforward
- Field current loop (ω_c = 20 rad/s) with field-weakening logic above base speed
- Anti-windup, rate-limited speed reference, bandwidth separation of one decade
## Mission profile
10 km route with speed steps (v_r/2, v_r, v_max) and 0 / +5% / −5% gradients.
## Results
- Speed tracking with 1–2% overshoot, negligible deviation on gradients
- Back-EMF clamped at nominal value in field weakening (i_e: 5 A → ~2.6 A)
- Armature current limited at 156 A; regenerative braking down to ~−125 A
