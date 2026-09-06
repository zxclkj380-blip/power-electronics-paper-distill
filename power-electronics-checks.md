# Power-electronics checks

Apply these audits before accepting a method card.

## 1. Plant and operating domain

- Identify topology, energy-storage elements, switching/averaged model, grid-forming or grid-following mode, and operating mode.
- State whether results assume islanded/grid-connected operation, balanced three-phase conditions, small angle, dominant R/X ratio, constant DC source, linear load, or a fixed network.
- Do not infer omitted SCR, source impedance, fault, harmonic, or saturation conditions.

## 2. Sign and coordinate audit

- Record current direction, voltage polarity, power sign convention, dq orientation, phase sequence, and error definition.
- Expand at least one controller equation against its declared error definition. Flag, rather than repair, inconsistent signs.
- For virtual impedance, verify the signs of `R i`, `ωLJi`, and `L di/dt` in the selected coordinates.

## 3. Units and causality audit

- Check units for gains, energy, damping, impedances, frequency, and per-unit conversions.
- Check that every differentiator, filter, observer, or algebraic loop is causal and has an implementation path.
- State sampling, delay, switching, and filtering only when reported.

## 4. Stability and passivity audit

- Identify the exact state, storage function, equilibrium, input/output ports, and parameter domain of each proof.
- Do not translate local linear stability into global, switching, saturated, delayed, or fault stability.
- For virtual resistance, examine whether total output impedance retains the required real-part/damping margin. Negative resistance needs its own proof.

## 5. Constraints and implementation audit

- Locate current limiters, voltage-reference limits, modulation bounds, DC-link limits, anti-windup, and rate limits.
- If a paper only shows similar currents, do not claim a strict current bound.
- Treat omitted sensors, delays, computational cost, and protection behavior as unknown.

## 6. Evidence audit

- Match baseline and proposal operating points, ratings, loads, controller bandwidths, and constraints.
- Distinguish simulation, HIL, real-time control, prototype, and field evidence.
- Record scenarios and metrics, not only plot impressions.
