---
title: "Engineering Reports vs. Slide Deck"
author: Muchen He
date: 2018-02-28
catergories: lecture
toc: true
toc_label: "Contents"
toc_icon: "bars"
---
# Engineering Reports vs. Slide Deck

## Demo 2

- 7 Minutes

- Show what the project can do

- Prove that it does what you claim

- Show evidence of design work (lab notebooks)

- Show design process (experiements, previous versions, etc)

- Show anything not easily shown on the slides

- Plan the presentation

---

## How Are They Used

### Engineering Report

- Will not be read immediately and in entirety

- For reference since it has unlimited detail

- For arbitrary audience so we must provide context and background

### Slide Deck

- Will be read immediately and in entirety

- It is a response to a request for proposal (RFP)

- Maximum information absorbed in minimum time

- The readers are identified and specified; prior knowledge is assumed

## Rule of Thumb

- Include line figures for showing concepts

- Include design drawings such as CAD models and PCB designs

- Include photos

- Include equations and values of any calculated work

## Slide Requirements

- Maximum of 20 slides

Some of the slides to include are:

- Title slide

- Problem description

- Design steps

- Results

- Summary slide

For handing in, include the slide deck as a PDF (optionally put 2 slides per page). Also include attachments such as source codes.

### Title Slide

Include team members, IDs, and maybe even a logo!

### Problem Description

We assume basic knowledge of the problem. The problem description consists of requirements, constraints, and goals (RCGs). The RCGs must be measurable. RCGs must be identified as satisfied or unsatisfied.

### Design Content

The design content can be classified into two categories: SimuLink and Controller.

#### Simulation

The simulation part consists of the model and which component in the model can be neglected. For example, if friction is small enough, you might justify that it can be neglected from the model.

Content should also include parameter identification. This include steps, calculations, and values.

Include PID controller design. Explain how the starting values are obtained. Explain how the PID gains are tuned, simulated, and implemented.

#### Controller

For the actual system, elaborate on the logic of the controller. Use flowcharts or pseudo-code to explain it visually.

Also talk about the timing analysis of the system. This include control frequency or time used for ISRs. Use diagrams and show measurements.

Show how the 'derivative problem' is gotten around. Any equations or filters used?

#### Motor

For stator design, justify the design for the poles and windings. Elaborate on any process used to analyize the stator such as checking for saturation.

For the commutator, what is the design, cylinder or disk? What about brushes?

For mechanical parts, how does the magnet support, shaft support, bearings, motor mounts fit together?

#### Sensor

For the encoders, is off the shelf part or custom encoder wheel used? What about features such as homing?

#### Others

##### Experiments

Show earlier versions and any challenges that came up. Also hsow any mistakes and lessons learned.

Some other things we can include:

- Microcontroller

- Custom digital circuits

- Mechanisms

### Results

Now that we have shown the design process, in response to the RCGs, we show the present.

Make sure to include measured values and plotted data. For intance, show step response and make sure they're on the **same graph**.

It would be good to show videos of successful experiemnts. A video is also good as an insurance policy for the demo.

### Evaluation

#### Control Evaluation

Show that the simulation quality is good by superposing the responses of the simulations and the real system. Good if they match. Some of the things to show:

- OL step response

- CL step response

- Tuned response

For performance, it's important to show:

- Overshoot

- Rise / settle time

- Control frequency

#### Motor Evaluation

For the motor, determine:

- Max speed

- Stall torque

- Total mass

- J & B coefficients

For the encoders, show possible resolution and maximum speed allowed to operate at.

### Summary Slide

- No new information

- Repeat the most impactful figures from slide deck

- Provide best graphics for discussions / Q & A

- Indicates slide deck is finished

Note that it's generally not a good idea to put "Questions?" header as the last slide. Better off burning a positive image that centers around a talking point.

