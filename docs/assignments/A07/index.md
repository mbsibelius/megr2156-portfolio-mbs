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
Goal high stiffness, high strength, light weight


### Bracket

#### Design 1
set the distributed force along where the strap is and defined it as a distributed mass 

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

##### Design 4
Passed convergence check after 2 iterations.

Design 4 saw a 54.36% decrease in max stress compared to design 3 with a max stress of 33330 psi located around the intersection of the chamfer and fillet of feature B. Maximum deflection decreased down to 0.1852. Mass was reduced down to 0.49 lbs. and a FOS of 1.1 was achieved. 

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

## Communicate


### Reflection

