# A10 – Lead Screw Design

## Objective
The objective of this assignment is to design and build a mechanically driven tensile tester. The tester must be capable of applying up to a 2 kN axial load. It must also have a controllable crosshead speed  
from 1mm to 50mm per minute and be designed with a safety factor of 4. The leadscrew must be at least 18 inches and it's preferred to be short enough to fit on a workbench.

Below is the concept image given.

![leadscrewconcept](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/leadscrewconcept.png)

## Lead Screw Selection

### Thickness

These are the knowns and unknowns for the lead screw:

![knowns](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/known.jpg)

Here is the FBD and numerical solving for the screw. The required force is split along two screws, but they need a safety factor of four.

![FBD](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/FBD.jpg)

The provided resources show leadscrews made with steel or stainless steel. The minimum yield strength for steels is around 205 MPa, so I will use that to calculate minimum diameter.

![dmin](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/dmin.jpg)

### Rotational Speed

Here are the knowns and unknowns for to determine the rotational speed based on a range of vertical speeds.

![known2](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/known2.jpg)

This is a free body diagram demonstrating how the nut translates around the screw. I made a mistake here for lead, it's 1/TPI, not TPI.

![FBD2](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/FBD2.jpg)

These are the calculations, I just chose 0.1 as as the lead since 10 threads per inch seemed common. The lead screw will operate from 0.394 to 19.68 RPM.

![RPM](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/RPM.jpg)

### Torque 

The coefficient of friction between steel and bronze was assumed to be 0.16, using this [Coefficient of Friction Reference Chart](https://www.schneider-company.com/coefficient-of-friction-reference-chart/) as a reference.

Here are the knowns and unknowns to find the Torque:

![known3](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/known3.jpg)

This is a rough free body diagram for the torque and the required formula.

![FBD3](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/FBD3.jpg)

I plugged in the values and found the torque to be 5.459 Newtons times meters. 

![T](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/T.jpg)

### Lead Screw Selection

The lead screw I selected has a part number 98935A911 on mcmaster.com. It's 24 inches long and has a 64,000 psi tensile strength, which equates to 441 MPa. I used 205 MPa in my earlier calculations, but it was for yield strength, which is always lower. ASTM A108 has a minimum yield strength of 195MPa which is slightly lower than my calculations. Considering the safety factor of 4 and the larger than necessary diameter, this lead screw shouldn't deform. 

![leadscrews](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/leadscrews.PNG)

## Nut Selection

These are the known forces for the nut.

![known4](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/known4.jpg)

This is the FBD for the nut and the required equations.

![FBD4](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/FBD4.jpg)

This is my calculation for the bending stress. I used 10 threads in the calculation because that was the first flange nut I saw with the same thread type.

![nutstress](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/nutstress.jpg)

This is the nut I ended up choosing, it has part number 95120A111 on McMaster-Carr. Other nuts made of the same material have a tensile strength of 35,000 psi, or 241 Mpa which put it well above the calculated stress. 

![mcnut](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/mcnut.PNG)

## Crosshead Design

For the crosshead design, I used a length in the range found in "Design, Manufacture, and Testing of an Open Source Tensile Testing Machine for Hands on Learning". I decided to use reasonable lengths and test if they would meet the requirements. It will be made from aluminum. 

![known5](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/known5.jpg)

Here is a diagram of the crosshead and the formulas I'll use.

![FBD5](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/FBD5.jpg)

These are the calculations for the dimensions I chose. The initial thickness caused too much deflection, so I increased it to 40mm.  

![crosshead](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crosshead.jpg)

Here is a drawing of the crosshead. It's missing tolerances for the fit, but it will be added later.

![crossdrawing](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crossdrawing.PNG)

## Cost Analysis

| Item Number | Quantity | Name | Cost/Item | Total Cost | Purchase Link |
|:---:|:---:|---|---:|---:|---|
| 1 | 2 | 1/2"-10 Acme Lead Screw | $6.95 | $13.90 | [Purchase](https://www.mcmaster.com/98935A911/) |
| 2 | 2 | 932 Bronze Flanged Nut | $125.72 | $251.44 | [Purchase](https://www.mcmaster.com/95120A111/) |
| 3 | 4 | Aluminum Frame Material | $12.25 | $48.98 | [Purchase](https://www.lowes.com/pd/Mecale-23-6-in-4040-Aluminum-Extrusion-T-Slot-Linear-Rail-4-Pack-6063-T5-Anodized-Profile-Black/5021607235) |
| 4 | 1 | 6060 Aluminum Crosshead | ~$10.00 | ~$10.00 | N/A |
| | | | **Total Cost** | **$324.32** | |

## Parametric Modeling

I started the CAD modeling by creating the crosshead.

![crosscreo](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crosscreo.PNG)

I extruded it and added space for the flange.

![crosscreo2](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crosscreo2.PNG)

I imported the crosshead, flanges, and leadscrews into an assembly.

![crosscreo3](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crosscreo3.PNG)

I mated all of the parts.

![crosscreo4](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crosscreo4.PNG)

I cut the aluminum supports to size and added them to the assembly.

![crosscreo5](https://raw.githubusercontent.com/DillonK-spec/megr2157-portfolio/main/docs/assignments/A10/crosscreo5.PNG)

### CAD File

[Download CAD File](https://github.com/DillonK-spec/megr2157-portfolio/raw/refs/heads/main/docs/assignments/A10/tensiletester.zip)

## Takeaways

This project was my first experience making an assembly in SolidWorks. I had trouble converting the downloaded files to millimeters and had to scale them manually. I got to read and browse the web a lot for this project, which added to the time I spent. Overall, I spent around 13 hours making this tensile tester.


### Credits
Dillon Knight - Calculations, Design, Cost of Leadscrew, nuts, and crosshead.
