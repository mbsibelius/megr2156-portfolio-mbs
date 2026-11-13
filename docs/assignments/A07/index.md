# A7 – [FEA on Bracket]

## Objective

- Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.
- Ensure high stiffness, strength, and lightweight optimization through iterative design.
- Conduct multiple FEA simulations, refining geometry based on results.
- Perform static stress analysis, including constraints, loading, and meshing selection.
- Interpret data by identifying max stress, displacement, and safety factors.
- Optimize the design by modifying geometry to enhance performance.
- Document the entire process with images, calculations, and insights.
- Reflect on key engineering lessons learned and time spent.

## Analyze
The goal of this method is to modify the design to achieve the highest stiffness, strength, and lightest weight possible.

### Bracket

#### Design 1
Constraints were applied to the roof set the distributed force along where the strap is and defined it as a distributed mass

2 iterations and passed 7% convergence Check
Inner loop time: 1 hour 30 min
Stress significantly higher than expected. Feature B was not modeled accuratley and stresses were higher than expected.

#### Design 2
Required 3 iterations & higher mesh count
Failed in the same areas as design 1.
Deflection behaved the same
Reduction in thickness of Feature C led to feature D experiencing more stress and deflecting more. Stress concentrations exceed ultimate strength of 58015 psi.
Design 2 redesign was able to reduce stress by 62.52% and deflection by 69.95%. however minimum deflection
Factor of safety study was set to automatic.

#### Design 3
Design 3 had the same problems as design 2 and did not meet minimum deflection. Stress concentrations in the same area but maximum stress had gone done 26.94% and deflection reduced by 28.402% with Max stress being 88120 psi, and max deflection being 0.01816 in
FOS increased 36.111% to 0.49

#### Design 4
Passed convergence check after 2 iterations.

Design 4 saw a 54.36% decrease in max stress compared to design 3 with a max stress of 33330 psi located around the intersection of the chamfer and fillet of feature B. Maximum deflection decreased down to 0.1852. Mass was reduced down to 0.49 lbs. and a FOS of 1.1 was achieved. 

### Bracket Link


#### Design 1
for the bracket link I designed both holes to be experiencing and modeled the fixtures as such. original calculations did not account for interference and instead treated both holes as experiencing only bearing stress. However, the 1 in hole and shaft system should've been modeled with interference pressure and bearing stress from the strap. Using the formula from the lecture contact pressure was calculated to be 7088.89 psi. Calculations for interference pressure Claude's, Google Gemini, and ChatGPT's answers. All three agreed on a contact pressure of 3545.46 psi contact pressure. 

Convergence Checks passed

Design 1 experienced max stress of 93390 psi and a max deflection of 0.004698 in. Stress was concentrated around the sides of the 1 in hole interface and deflected the most towards the bottom of it. It experienced a minimum factor of safety of 1

Design 1 weighed 0.37 lbs

Time taken: 1 hour 20 min


#### Design 2
Max stress experienced by the part dropped significantly by 76.31% and experienced a max stress of 22590 psi concentrated similarly to design 1 and deflected similarly to design 1. Significant weight increase to 0.66lbs occurred from uniformly increasing diameter around the link.

Time taken: 50 min
Convergence check passed with 2%

### Design 3

Maximum stress was reduced down to 18540 psi with the same concentrations as previous design. maximum deflection decreased to 0.0005989 in deflecting in the same region as previous design. FOS increased to 2.006.

Time Taken: 1 hour 20 min


### Design 4
All goals were met on Design 4. Maximum stress decreased to 0.4771 psi and concentrated around the midpoint of the hole of feature A. Maximum deflection decreased significantly to 1.308 nano in and displaced the most outside the outer diameter of feature A. FOS increased to 15 and met the minimum factor of safety required.

Time Taken: 3 Hours

## Decide

#### Bracket

### Design 1 Redesign
I chose to keep the same general design of the bracket to see how l
Initially Feature B was modeled inaccurately as a rod in tension. In this 1st redesign I modeled feature B as a cantilever beam with moment applied to the free end. Based on the deflection equation I chose to increase thickness  and decrease the length of feature B to minimize deflection & lower stress. Thickness was increased 100% and length was reduced 25%.

To minimize mass I opted to reduce the thickness of feature C & E by 50%

Factor of safety was kept the same
Parametric Equations were modified to modify geometry.
I chose to keep the same general design of the bracket to see how little I could change from my initial design.

### Design 2 Redesign
Both designs goal is to minimize changes to concept bracket as little as possible
In order to better distribute the load throughout the bracket and reduce the deflection on the end of the tip, I opted to add a rib connecting the bottom of feature A up to the top face feature c. The thickness of the rib was set to have the same thickness as feature C. The angle was set 10 degrees in order to minimize mass and still provide stiffness.
In order to keep the length of feature B I opted to add a Symetric fillet connecting the bottom face of feature C to the front face of feature B. 
To minimize stress experienced by feature D and reduce deflection thickness was increased by 0.1 in. Additionally Length of bracket was increased by 0.1 in. To conserve mass feature C's thickness was reduced by 0.20 in.

Time it took to complete Design 2-3 of Bracket: ~3 hours

### Design 3 Redesign
To better distribute stress concentration around feature B radius of fillet added in design 3 increased to connect to the front face of the bracket with additional Fillets added to the side. Added fillets reach from feature B's right and left hand side to the outside of the bracket. The angle of the rib added in design 3 was flipped to create an angle from the bottom of feature A. Rib Angle was removed and instead extends 0.25 in out to increase material around feature B and distribute stress concentration. Chamfer was added around circumference of feature A connecting to feature B to distribute stress concentrations. Feature E, D, and C thickness was reduced to reduce masss.

To model the forces experienced by the bracket more accurately I fixed the top of feature C along with the bottom face of feature E. 

### Bracket Link

#### Setting constraints
I considered the hole connecting to feature A to be fixed in the 

#### Design 1 Redesign
1 in hole failed before transmitting load to the rest of the link. More material needs to be added to the 1 in hole and to conserve weight length between distance between holes was set to fixed length of 0.75 in. Outer diameter of hole was increased to 1.81in to better handle the stress concentrations and minimize the deflection of the part.

Thickness of link was kept the same.

#### Design 2 Redesign
Constraints were not changed from original. To reduce mass I decreased the wall thickness around the hole of feature A to the original 1.20 in diameter, in addition to decreasing the spacing between holes to 0.25 in. 
Thickness was recalculated with contact pressure from interference in mind and with respect to yield stress. For the sake of simplicity thickness was increased by 0.256 in from hoop stress calculation of 1 in hole. To better distribute stress concentrations around the inside surface of the 1 in hole. Additionally the ultimate strength variable was replaced with yield strength of the part to increase the FOS of the link.

### Design 3 Redesign
Loads placed on 1" hole diameter were changed to a uniformly distributed load directed away from feature A and towards the 1 in hole  contacting only the bottom half of the surface. Additionally constraints were placed on the entire surface of the hole considering the pin makes full contact with the entire surface of the hole. Feature A's constraints were modified to fix the only top half of the surface of the hole contacting feature A, considering the small clearance of the running fit.

To reduce mass of the link outer diameter was reduced down to  1.22 in and dimensioned to both of the links outer diameter. Additionally fillets with a radius equal to wall thickness were added to the front and back faces of the link. Lastly sketch was modified to cut out material from the space between the links.


## Communicate

#### Lessons Learned

#### Prompts used
- what is the contact pressure of a shaft and hole with an interference of 0.0008 in, a hub with an outer diameter of 1.2 in, a 1 in shaft, and a hole sized to 0.9992 in. Both shaft and hole are made of the same material with an elastic modulus of 29007457 psi.

