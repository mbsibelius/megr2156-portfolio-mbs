# A3 – [Topic]

## Objective
- Use axial deflection modeling to design its dimensions
- Use parametric design to determine a bars length
- Introduce you to FEA (Finite Element Analysis)
- Introduce you to linking dimensions to appropriate parameters in CAD.
- Compare and contrast the different analysis

## Analyze
Watched videos to learn how to parametrically design and conduct FEA
Chose a diameter and wrote down equations to calculate min and max length for a fixed diameter. Chose to use min length.
Chose to start with the largest Young's modulus first.
Made a custom material to fit the properties of aluminum given. Did not input shear modulus or Poisson's ratio.
Made global variables for each property as well as the length of the bar using the direct tension equation.

(20%) Topic: Modify Design Parameters

Instructions:

Cycle through #2, change each of the design parameters, which include load and diameter. Keep the material and the fixture the same.

Decreased Load to 300 lbs; kept 1 in diameter.

Looking at the original equation that I used to calculate the length of the bar, a decreased load would create a longer length.

Increased Diameter to 5 in and kept 500 lbs

Similar to the first answer an increased diameter would increase the length of the rod because the length of the rod would 

Before you calculate, take a guess if the length will increase, decrease, or stay the same. (You will not be penalized for guessing incorrectly.)

## Decide
(5%) Report the axial deflection from your parametric hand-calculation and from your FEA. Calculate the percent difference between the two.
From FEA, the displacement is 9.017*10^-3 in
If there is a meaningful discrepancy, identify at least one likely source (e.g., assumptions in the hand-calc, boundary conditions, mesh density, material property inputs).
If the two values are essentially the same, explain why you'd expect them to agree for this geometry and loading (e.g., no stress concentrations, simple axial loading, coarse mesh still adequate for a uniform cross-section).
Either way, state which result you'd trust more for this design and why.
(5%) Now imagine a fairly substantial pin hole on the left side of the bar. Look up the stress concentration factor (Kt) for a hole in a flat bar in tension (Peterson's charts or Machinery's Handbook). Using your FEA's nominal stress away from the hole, estimate the peak stress at the hole and state whether it would still pass your safety factor. (Don’t redo the FEA!)
(5%) Lessons Learned document mistakes made and actual time spent from start to finish.


## Communicate 
