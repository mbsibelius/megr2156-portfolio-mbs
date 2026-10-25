# A5 – [Bracket Design]

## Objective
Conduct stress analysis to determine appropriate dimensions for structural features.
Generate free body diagrams (FBDs) to visualize forces and constraints for each feature.\
Identify and document known and unknown variables, assumptions, and algebraic models for stress calculations.
Perform stiffness analysis to establish minimum required dimensions based on deflection constraints.
Compare stress and stiffness analyses to ensure structural integrity and compliance with given constraints.
Create detailed multiview sketches illustrating dimensions derived from both stress and stiffness analyses.
Reflect on and document key engineering lessons learned throughout the process.

## Analyze
Before calculating anything, I used the Pandapipes material properties sheet for ASTM A36 steel; the website used is linked below. To get the dimensions for the clearances, I treated the T- beam as a shaft and the bracket as a hole. Measurement B was classified as LC1, A as RC1, and C as LC1 according to ANSI standards.

![clearances and fits of bracket](bracketFitment.png)

All calculations were done with both minimum and maximum values for force.
### Feature A Stress
Feature A was modeled as a cantilever beam that is fixed at one end. 

![feature A calculations for stress](featureACalculationsStress.png)
### Feature B Stress
Feature B was modeled as an axially loaded bar.

![feature B calculations for stress](featureBCalculationsStress.png)
### Feature C Stress
Feature C was modeled as a beam supported on both ends with a point load in the middle.

![feature C calculations for stress](featureCCalculationsStress.png)
### Feature D Stress
Feature D was modeled as an axially loaded bar. The length of the part was defined by the clearance requirement, so the thickness of the part was calculated. 

![feature D calculations for stress](featureDCalculationsStress.png)
### Feature E Stress
The width of the part was defined by the clearance requirement length of the part calculated did not affect stress, so the thickness was calculated. The feature was treated as a beam supported on one end with an evenly distributed load.

![feature E calculations for stress](featureECalculationsStress.png)

### Sketch of part according to stress
All final dimensions were chosen according to the maximum force experienced by the part. All dimensions are defined to the thousandths place.
![Sketch of part Stress](deflectionSketch.png)

## Deflection Calculations

All features were modeled the same as stress calculations.

### Feature A Deflection

![feature A calculations for deflection](featureACalculationsDeflection.png)
### Feature B Deflection
Calculated for the length of Feature B instead of thickness since the length of the feature did not affect stress. Used thickness from Feature B stress calculations.

![feature B calculations for deflection](featureBCalculationsDeflection.png)
### Feature C Deflection

![feature C calculations for deflection](featureCCalculationsDeflection.png)
### Feature D Deflection

![feature D calculations for deflection](featureDCalculationsDeflection.png)

### Feature E Deflection
![feature E calculations for deflection](featureECalculationsDeflection.png)
Height did not affect the bending stress, but it did affect deflection, so width was used in the deflection calculation. From the equation, we can see that a shorter feature height would lead to a shorter deflection. Therefore, the height of feature e was set to 

### Sketch of Part According to Deflection

![sketch of part according to deflection](stressSketch.png)



### Link design
Before all calculations, the hole fitments were determined. According to the specifications, the size of the hole for the bracket would be classified as RC7, and the 1" hole would be classified as an FN1 fit.
The sizes of both holes only need accuracy up to 0.0001", which would only require broaching to achieve their desired dimensions according to the table below. To calculate the cross-sectional area of the link, bending stress was used to determine the thickness of the link, and the length was decided through axial stress. Stresses for both holes were calculated.
![table of manufacturing processes](!)

![calculations of link](linkCalcluations.png)

![calculations of link](linkCalcluations1.png)

![calculations of link](linkCalcluations2.png)

![calculations of link](linkCalcluations3.png)

The final thickness of the hole was decided based on the hole that attaches to the bracket. The final length was set to whichever hole required a longer length. 

![calculations of link](linkCalcluations4.png)

![calculations of link](linkCalcluations5.png)

![calculations of link](linkCalcluations6.png)

![calculations of link](linkCalcluations7.png)

![calculations of link](linkCalcluations8.png)

The final length of the link was only set to be the length of the span from the 1" hole for the sake of uniformity.

## Decide

### Feature Modeling.
For features A, B, and C, they were all modeled and calculated per the instructions of the assignment. For Feature D, it was modeled as an axially loaded bar because the only dimension that could be changed was the thickness of the feature, with C governing the length of the entire bracket. Feature E was modeled as a beam with an evenly distributed load on the bottom of the beam, because the height of the part was the only ungoverned dimension. The uniformly distributed load was chosen because its entire bottom surface contacts the body it assembles with.


## Communicate

### Lessons Learned

#### Governing failure mode Feature C

For Feature C, stress governed the final dimension of the feature, requiring 1.050" as opposed to 0.386" for stiffness.  

#### Error propagation:

When calculating with minimizing deflection, an initial mistake in calculating the radius of Feature A created an error in calculating the length of Feature B. 

#### Assumption sensitivity:
An initial assumption I made was that modeling feature E as an axially loaded block would end up calculating the height of the feature. Treating feature E as an axially loaded block would only change the thickness of the overall part or the length of the feature, but would not affect the height of the feature.

### Links used
Bearing stress calc: https://www.valuedes.co.uk/bearing-contact-worked-example.html
Stress concentration:
https://www.valuedes.co.uk/stress-concentration.html
ASTM A36 steel material properties: https://pandapipe.com/blog/a36-steel-material-properties/
Fits and tolerance measurements: https://www.cobanengineering.com/Tolerances/ANSILocationalCleranceFits.asp

