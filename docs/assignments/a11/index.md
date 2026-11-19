# A11 – Motor Selection

## Objective
In this project, we will continue designing a tensile tester that can withstand a 2kN load. We will be selecting motors to drive the leadscrews, designing motor mounts, and then creating a frame. Our group includes Dillon Knight, Marvin Sibelius, and Sean Chadwick.

## Specifications

Maximum tensile load: 2,000 N

Number of leadscrews: 2

Leadscrew length: 24 inches

Leadscrew diameter: 1/2 inch

Leadscrew lead: 0.1 in/rev

Required travel speed: 1–50 mm/min

Factor of safety: 4

Leadscrew material: ASTM A108

## Motor Selection (Dillon)

Each leadscrew requires 5.459 N·m of torque. Since each leadscrew will be driven by its own motor, both motors must be capable of producing at least this amount of torque. Each motor must also operate over an output speed range of approximately 0.394–19.685 RPM.

A DC gearmotor is being considered because the leadscrews require relatively high torque at low speeds. A motor with an output speed near 20 RPM and a continuous torque rating of at least 5.459 N·m would be suitable.
I found a motor rated for 6 N*m and 28RPM [Here](https://cautop.com/mall/show-1993526.html)

I used Excel to generate theoretical speed and power values based on torque. 10 N*m is the peak torque listed, and my Excel formula for speed was “(33*(1-A2/10))*2*PI()/60,”  which linearly decreased the speed from 33 to 0 and converted RPM to Rad/s.

![excelcurve](excelcurve.png)

This is the generated graph showing the relationship between torque, speed, and power.

![speedtorquecurve](speedtorquecurve.png)

The max power output is around 5 N*m and 15 RPM.
## Motor Mount Design (Sean)

The goal of this part of the assignment is to find how thick the motor mounts need to be. Our design features two different motors, which meant we would have 2 brackets.

![2a](2a.PNG)

Here, I stated all of the variables we knew and every variable that needed to be found. The force, torque, and dimensions of the holes/bracket were known, except for the thickness of the bracket, which is what we are solving for.

![2b](2b.PNG)

I drew a Free Body diagram of the bracket in question to get a good layout of the bracket and the spacing of each hole, as well as drawing out where each force and moment will be acting.

![2c](2c.PNG)

I then solved for the thickness algebraically. I solved for both sizes of holes, using two separate diameters.

![2d](2d.PNG)

Plugging in the numerical values, I got a minimum thickness of .74mm, which is not going to be our thickness of the plate, as that is thin and will ultimately lead to a less accurate plate. Plate thickness was chosen to be ¼ in to increase stiffness and strength with minimal weight gain.
### CAD Motor Mount (Marvin)

![2bracketCad](2bracketCad.png)

![2bracketModel](2bracketModel.png)

## Coupler Design (Sean)

The next part of the project was designing a coupler that would mate the motor shaft and the leadscrew. I followed a similar process as the previous section in getting it to work. This will tell us the thickness of the wall of the coupling, and I will test that against what is available commercially to make sure it is strong enough.

![3a](3a.PNG)

I started off by listing out all of the known and unknown variables. I knew the torque, the inner diameter, and the S-y value of the stainless steel. I was trying to find the outer diameter, the polar moment, and the overall outer radius.

![3b](3b.PNG)

This is the free-body diagram of the coupling with the two separate shafts connected to it.

![3c](3c.PNG)

I solved it first using algebra. The main hold-up in this section was that my formulas spit out a quartic, which I had to use a calculator to solve instead of traditional methods taught in school. I used a special method in order to estimate the value of the minimum outer diameter.

![3d](3d.PNG) 

After plugging in the values, I got a minimum outer diameter of 10.5 mm, which left me with a wall thickness of only .25 mm, which was well within the tolerances of the coupling selected. I went with part number 2463K403 on McMaster

## Mount design (Sean)

The purpose of this section of the project was to spec out the mounts that connected the crossmember and the vertical frames. 

![4a](4a.png)

I started off by listing out my knowns  and unknowns for the task. I knew all of the outside forces and torque, but needed to figure out what the forces and stresses looked like on the bar itself to see if it rotated too much. I also specced out the different types of mounts from McMaster and ended up choosing a mount to use its dimensions.

![4b](4b.png)

This is the free-body diagram for the mounts and the crossmember.

![4c](4c.png)

This is where I solved it symbolically for the stress caused by torque and the stress caused by normal force.

![4d](4d.png) 

After plugging in the values, I got 83.7 MPa. This is the maximum stress that this material can withstand. This is about 8 times higher than the peak load with a Safety factor of 4 applied to it, so it told us that it will be perfect for the project, as there wasn't a weaker option that would be cheaper. I chose part 5537T66 from [mcmaster](https://www.mcmaster.com/5537T66/)


## Horizontal Member Verification(Marvin)

![horizontalBracketFixtures](horizontalBracketFixtures.png)

![horizontalBracketForces](horizontalBracketForces.png)

![horizontalBracketRefinedMesh](horizontalBracketRefinedMesh.png)

![horizontalBracketMaxDisplacement](horizontalBracketMaxDisplacement.png)

![horizontalBracketMaxStress](horizontalBracketMaxStress.png)

![horizontalBracketWarping](horizontalBracketWarping.png)

Max stress: 2.155 GPa
Max displacement: 1.376 mm
Factor of Safety: 0.042

Largest displacement at the load line and additional twisting around the areas where the motor mounts to the top of the frame. The horizontal member experienced larger deflection on the side unsupported by mounts. Max displacement is well over the intended design. The load path of the axial machine might warp towards the side of the cross member unsupported by bracket. To improve the part's stiffness, I would provide better cross-bracing from the top of the frame to the vertical member and position it closer to the load path of the machine. To save weight, I think I would opt to change the aluminum extrusion used to a lighter version offered by McMaster.

## Vertical Member Verification(Marvin)

![verticalBracketFixtures](verticalBracketFixtures.png)

![verticalBracketForces](verticalBracketForces.png)

![verticalBracketMesh](verticalBracketMesh.png)

![verticalBracketMaxDisplacement](verticalBracketMaxDisplacement.png)

![verticalBracketMaxStress](verticalBracketMaxStress.png)

![verticalBracketFOSs](verticalBracketFOSs.png)

Max stress: 51.50 MPa
Max displacement: 0.02433 mm
Factor of Safety: 0.042

Warped the most around the area not supported by the bracket chosen during the design stage. The load path was not as intended due to an incorrect orientation of the cross members and the vertical members. Member did not deflect as expected
The frame was constructed incorrectly, with the horizontal member only connecting to the vertical member through a bracket fixture, and showed up through FEA. The most important change to the frame would be to orient the horizontal member on top of the vertical member so forces are distributed better to the vertical members of the machine.

## Assembly(Marvin)

![A11assemblyDrawing](A11assemblyDrawing.PNG)

## Mounting Bearing (Dillon)

An RC3 running fit was used for the floating bearing mount at the bottom of the leadscrew. For the 0.5-inch diameter leadscrew, the hole has a tolerance of +0.0007”/-0.00,” and the shaft has a tolerance of -0.0006”/-0.001”. The mounts are placed directly under the leadscrew. 

![bearingplate](bearingplate.jpg)

This bearing plate will be 0.5” thick and use 0.1/4”-20 bolts at each corner.

![bearingPlate](bearingPlate.PNG)

## Bill of Materials (Dillon)

| Item Number | Quantity | Name | Cost/Item | Total Cost | Purchase Link |
|:---:|:---:|---|---:|---:|---|
| 1 | 2 | 1/2"-10 Acme Lead Screw | $6.95 | $13.90 | [Purchase](https://www.mcmaster.com/98935A911/) |
| 2 | 2 | 932 Bronze Flanged Nut | $125.72 | $251.44 | [Purchase](https://www.mcmaster.com/95120A111/) |
| 3 | 4 | Aluminum Frame Material | $12.25 | $48.98 | [Purchase](https://www.lowes.com/pd/Mecale-23-6-in-4040-Aluminum-Extrusion-T-Slot-Linear-Rail-4-Pack-6063-T5-Anodized-Profile-Black/5021607235) |
| 4 | 1 | 6060 Aluminum Crosshead | ~10.00|~10.00 | N/A |
| 5 | 2 | DC Worm Gear Motor | $18.05 | $36.10 | [Purchase](https://cautop.com/mall/show-1993526.html) |
| 6 | 2 | Motor Mounting Brackets | $8.00 | $16.00 | N/A |
| 7 | 2 | Leadscrew Couplers | $12.00 | $24.00 | N/A |
| 8 | 8 | 1/4-20 Bolts | $0.80 | $7.99 | [Purchase](www.amazon.com/dp/B07MQXL594)|
| 9 | 8 | 1/4-20  Nuts | $0.16 | $4.99 | [Purchase](https://www.amazon.com/dp/B0CSY9G7TW)|
| 10 | 2 | Floating Bearing Mounts | $6.00 | $12.00 | N/A |
| | | | **Total Cost** | **$324.32** | |

### Labor Costs

An hourly rate of $35 was used to calculate engineering labor costs. The total labor cost was determined by multiplying the hours spent on each task by the hourly rate.

| Task | Hours | Rate | Total Cost |
|---|---:|---:|---:|
| Leadscrew Selection and Calculations | 2 | $35 | $70.00 |
| Crosshead Design | 2 | $35 | $70.00 |
| Motor Selection | 1.5 | $35 | $52.50 |
| Motor Mount and Coupler Design | 2 | $35 | $70.00 |
| Frame Design | 2 | $35 | $70.00 |
| FEA Analysis | 3 | $35 | $105.00 |
| Floating Bearing Mount Design | 1 | $35 | $35.00 |
| CAD Assembly and Drawings | 3 | $35 | $105.00 |
| Documentation | 5 | $35 | $175.00 |
| Total | 21.5 | | $752.50 |


Length of horizontal frame was changed to reflect

### Drawings (Marvin)

![A11assemblyDrawing](A11assemblyDrawing.PNG)

![bearingPlate](bearingPlate.PNG)

![crosshead](crosshead.PNG)

![motorMountingBracket](motorMountingBracket.PNG)

## Lessons Learned

### Dillon Knight
This project gave me a lot of experience regarding the output of electric motors. I learned how to create a speed and torque graph in Excel and use it to understand power. Another application of this project that taught me was listing the parts and labor. The project cost a little more than I thought it would.
Time Spent: 4 hours


### Sean Chadwick
The biggest lesson that I learned was in the area of setting up free body diagrams. After having to redo the free body diagram for the frame design portion of choosing mounts, I realized that the complexity of the free body diagram will determine how long the project will take and how accurate it will be. I got better at spec’ing out parts using mcmaster-carr and utilizing that to my advantage when designing certain parts.
Time Spent: 5 hours


### Marvin Sibelius
Time Spent: 6 hours
The biggest lesson that I learned is that more complex geometries require more time to properly constrain and model forces for FEA. I learned that when possible, it is important to have a solid idea of how your part is fixed before committing to an FEA study. I learned that planning an assembly would save significantly more time in making an assembly in SolidWorks. I learned that it is important to communicate between team members so you can have a better understanding of their engineering decisions.

### Link To Folder of Parts & Drawings
- https://drive.google.com/drive/folders/14NOOHz9R6fuN6NelSo4oPWweM5v9AqLG?usp=sharing

