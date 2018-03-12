---
title: "Milestone II Demo Feedback"
author: Muchen He
date: 2018-03-12
catergories: lecture
toc: true
toc_label: "Contents"
toc_icon: "bars"
---

<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

## Overview

Everything is generally good. Motor team has average of 82; controller team has an average of 84. Motor's team has been scaled to have an average of 84.

## Motor Model

In the equivalent circuit, there are three powers:
$$
P_\text{loss}=R_A I_A^2\\
P_\text{elec}=V_AI_A\\
P_\text{mech}=K_\tau I_A\omega
$$
Conservation of power:
$$
P_\text{elec}=P_\text{mech}\\
V_AI_A=\tau\omega\\
K_V\omega I_A=K\tau I_A\omega\\
K_V=K\tau
$$
Notice that the back EMF constant and the torque constant is the same given that they're in the same units. 

To model a motor, we need 6 parameters:

| Parameter | Description       |
| --------- | ----------------- |
| \\(R\\)       | Resistance        |
| \\(L\\)       | Inductance        |
| \\(K_V\\)     | Back EMF constant |
| \\(K_\tau\\)  | Torque constant   |
| \\(B\\)       |                   |
| \\(J\\)       |                   |

### Test

Here's our test:

1. apply V<sub>S</sub> of 9V
2. measure current drawn, in this example, say I<sub>A</sub>=1A
3. measure speed, say it is 2 rad/s

Now let's compute some parameters:

1. \\(V_A=V_S-I_A R_A=9-1(1)=8\\)V
2. \\(K_b=\frac{V_A}{\omega}=\frac{8}{2}=4 \frac{\text{Vs}}{\text{rad}}\\)
3. \\(K_\tau=4 \text{Nm/A}\\)
4. \\(B=\frac{\tau}{\omega}=\frac{K_\tau I_A}{\omega}=\frac{4}{2}=2\text{Nms/rad}\\)



For moment of inertia, calculate the moment of inertia for each component individually, then add them up.

For a cylinder with a hollow shaft with inner radius \\(r_1\\) and outer radius of \\(r_2\\), and mass of \\(m_1\\), the moment of inertia is given by:
$$
J=\frac{1}{2}m(r_1^2+r_2^2)
$$

## Impulse Response

Something like keep the motor turning and suddenly turn the motor off after some time.

1. Give some non 0 input and let it run for a while for the transient behavior to go away
2. Turn power off and measure the response
3. Disregard data before we turned off the power

Note that the theoretical response and the real response are different possibly due to **stiction**.




