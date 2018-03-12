---
title: "Milestone I Demo Feedback"
author: Muchen He
date: 2018-02-05
catergories: lecture
toc: true
toc_label: "Contents"
toc_icon: "bars"
---

## Logistics

- The score for motors are higher -> The score for control is scaled
- Self assessments need to be more concise, specific, and measurable

## Demo

- Prioritize **show** first, then explain
- Organization is vital (use PowerPoint if necessary)
- Show the best features clearly (design freeze)

## Control

- Keep in mind about the spacing of the encoders
- Obtain ALL of the motor parameters (especially mechanical parameters)
  - Extremely important for later on to find paramters on the custom made motor
  - Electrical
    - R, L, C
  - Mechanical:
    - J, B, K (don't need to unless we're actually adding spring)
  - Electromechanical:
    - Torque constant
    - Back EMF constant

## Motor

- Windings are done nicely and cleanly
- In the future when using laminated cores, make sure there is minimum airgap
- (Potential gotcha) When using metal windings, the cross section of the core is rectangular, but the winding is curved; thus the insulation near the corners of the core are worn. This can cause the current to all go through the core and render the rotor useless.
- Cylindrical commutators are common. Commutators in general needs more work
- Most motors are in a test bench (good), Make sure the parts of the test bench are contrained (fix them together)
- Most brushes are not mechanically mounted. Making sure the brushes are making just enough contact with the commutator without introducing too much friction
- Know if the motor will self-start (for fixed commutator brushes)
- Make sure the base of the test bench is not flexible and flimsy

## Couple of More Things

### Control

- Derivative term (using finite difference derivative): (Pf-Pi)/(change in time)
  - If the (discrete) signal is slower than the sampling time, the velocity over time will appear like an impulse train
  - Some filter (such as averaging) is required
  - Faster control frequency is better, but will cause problem with derivative term
- Make sure ISR is short and as fast as possible
  - Bloated ISR will impose lower control frequency
  - Never want ISR to be interrupted 
- A nice milestone is to have a real open-loop (no feedback) step response similar to the simulated step response
- Then do a close loop step response with PID, and compare it with the simulated step response 

### Motor

- Problems with cylindrical commutator
  - If the commutator is not perfectly round, the brushes are bouncing around 
  - Short gap cause sparking and bouncing brushes
- Try disk commutator
  - Put brushes near the center of the disk (low speed, low friction)
  - Make disk out of PCB (put spot of solderable spot for winding connection)
- [`Quickfield.com`](http://Quickfield.com) shows magnetic field when you put windings around magnetic material; shows saturation.
- Glue won't work for laminating metal; paint works well
  - Use paint to laminate
  - Use nuts, bolts, and washers to clamp them overnight
- Generally bad idea to glue the shaft with rotor
  - Drill a hole and use a *set screw*

### MileSTONE II

- Build a closed motor for use 