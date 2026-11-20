# University
This repo contains documents related to university courses, projects or insights.

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
