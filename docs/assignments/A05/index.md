# A5 – [Topic]

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
### Feature A Stress
Feature A was modeled as a cantilever beam that is fixed on end. 

![feature A calculations for stress](featureACalculationsStress.png)
### Feature B Stress
Feature B was modeled as an axially loaded bar.

![featurea B calculations for stress](featureBCalculationsStress.png)
### Feature C Stress
Feature C was modeled as a beam supported on both ends with a point load in the middle.

![feature C calculations for stress](featureCCalculationsStress.png)
### Feature D Stress
Feature D was modeled as an axially loaded bar.

![feature D calculations for stress](featureDCalculationsStress.png)
### Feature E Stress
Height did not affect stress, so width was calculated.
![feature E calculations for stress](featureECalculationsStress.png)




used this link for finding transition fits and clearance fits: https://www.cobanengineering.com/Tolerances/ANSILocationalCleranceFits.asp

## Deflection Calculations



### Feature B Deflection
used thickness from feature b stress calculation since length of the the feature did not affect the stress experienced by the feature. Calculated for max length. Will go with length used in stress calculations

### Feature E Deflection
height did not impact the bending stress, but affects deflection, so width was used from deflection calculation. From equation, we can see that a shorter feature height would lead to a shorter deflection. Therefore height of feature e was set to 


height of part will be set to thickness of 

### CAD
I decided to go with the largest possible 
For feature B the length was set to the radius
### link design

### Feature A
bearing stress calc: https://www.valuedes.co.uk/bearing-contact-worked-example.html
stress concentration:
https://www.valuedes.co.uk/stress-concentration.html

## Decide


## Communicate

### Links used

ASTM A36 steel material properties: https://pandapipe.com/blog/a36-steel-material-properties/
Fits and tolerance measurements: https://www.cobanengineering.com/Tolerances/ANSILocationalCleranceFits.asp

