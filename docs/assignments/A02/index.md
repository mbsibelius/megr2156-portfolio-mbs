# A2 – Truss Stress Analysis

## Objective
- Design a lightweight planar truss using A500 steel or an alternative material.
- Create free body diagrams (FBDs) for joints and critical pins.
- Calculate the required cross-sectional area of truss elements with a safety factor.
- Determine pin sizes based on shear forces with a safety factor.
- Solve equations symbolically and numerically for both truss and pin design.
- Estimate the total weight of the truss and pins.
- Create a CAD model with accurate dimensions and connections.
- Compare CAD weight predictions with hand calculations.
- Document key engineering lessons learned from the process.

## Analyze

#### df

The initial research for this truss analysis started with looking at the diagram given and finding out the material properties of A500 steel. Due to having a late start to this assignment I did not spend much time analyzing the situation and went with the first design that came to my mind. I placed a point in the middle of the top member and connected points D and C to it labeling it point E.
then through google I found a document with yield strength, density, and bulk modulus on it.

https://www.youtube.com/watch?v=M5iuXqwEf7c&t=1s
https://www.trussanalysis.com/free?cat=custom&cnodes=0%7E0%7Er%7E0%7E0_1.2%7E0%7Ep%7E0%7E0_0.4%7E-0.3%7Ef%7E0%7E-20_0.8%7E-0.3%7Ef%7E0%7E20_0.6%7E0%7Ef%7E0%7E0&cmems=0%7E4%7E178%7E140000_0%7E2%7E178%7E140000_2%7E4%7E178%7E140000_2%7E3%7E178%7E140000_3%7E4%7E178%7E140000_3%7E1%7E178%7E140000_1%7E4%7E178%7E140000

## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._
(10pt) Part 1 – Truss Members
Each truss member is under either tension or compression and may fail due to the applied loading. For each member:

Identify the expected failure mode (yielding, fracture, or buckling)

  Looking at the truss analysis document, we can see that members BE, EC, and CA(0, 4, and 5) are under tension and members BD, DE, and EA (1, 2, and 6) are under compression. However, member 3 (DC) is the only zero-force member and would not fail under load. Members BE, EC, and CA would fail through yielding before they fracture. Members BD, DE, and EA would fail under buckling
  
State whether the material is ductile or brittle.
  According to the document attached, Grade B ASTM A500 Steel has a carbon content less than or equal to 0.30%, making it more ductile.

Support your choice using stress comparisons and simple reasoning.
  According to the document attached, the yield strength of each member is 315 MPa. For members under tension, the largest amount of normal stress experienced is 90 MPa. With my current model, all members under compression would buckle under load. Using Euler's buckling formula, members BD, DE, and EA have critical loads of 6.41 kN, 12.3 kN, and 4.450 respectively. All of which are well below the loads they experience, according to my analysis.

Propose a design modification that could reduce the likelihood of this failure.
In order to prevent each member from failing due to buckling, I would change the cross-sectional area to a square with a length of 13.34 to increase the critical load on the smallest member to 14.6 kN.

 Part 2 – Pin Connections

In order to figure this out I compared the shear capacity of the pin to the bearing capacity of the member. Using the equations provided from the video linked here https://youtu.be/VHd_eSXwbIc. From the calculations the pins have a lower capacity of 48 kN compared to the bearing capacity of  59.2 kN. Using the NDS yield modes the pin would fail in mode 1 where the capacity of the bearing is greater than the capacity of the pin. In order to reduce the likelihood of this mode of failure I would increase the diameter of the pins.
https://www.structuremag.org/article/design-of-bolted-connections-per-the-2015-nds/

## Communicate

