# A2 – Truss Stress Analysis

## Objective


## Analyze
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

(10pt) Part 2 – Pin Connections
Identify the expected failure mode of the pin.

Support your answer with data from credible, known sources.
Propose a design modification to reduce the likelihood of this failure

## Communicate

