# A6 – [Bracket Drawing]

## Objective
- Create a parametric model and a detailed engineering drawing from the project A5 sketch and dimensions.

## Analyze
Before creating sketches, all dimensions calculated from the stress analysis of the bracket were made to be global variables with respect to each feature. All dimensions used were from the stress analysis of the part.

### Sketches & Features

![project A6 globalVariables](globalVariablesA6.png)

![feature A sketch](featureASketch.png)

![feature A feature](featureAFeature.png)

![feature B sketch](featureBSketch.png)

![feature B feature](featureBFeature.png)

![Bracket Sketch](bracketSketch.png)

![Bracket feature](bracketFeature.png)

![parametric equations](parametricEquations.png)


### Bracket Drawing

![Bracket Drawing](ProjectA6.JPG)

### Link 
All link dimensions were taken from stress calculations, with only one dimension modeled parametrically.

![link equations](linkEquations.png)

![link sketch](linkSketch.png)

![link feature](linkFeature.png)

![link drawing](ProjectA6Link.PNG)

## Decide

Tolerances were displayed bilaterally for all dimensions to have a desirable value that fits within the clearances/interferences of all fits.

### Bracket Drawing
Tolerances applied to critical features are specified to X.XXX or X.XXXX units due to the required clearances for each fit. However, features D and E's thickness is specified to X.XXX to meet stress requirements. Other non-critical features are done to X.XX to minimize costs where possible.

### Link Drawing
The dimensions of the 1-inch hole were adjusted to ensure a proper fit for FN1. The dimension of the hole was made with the assumption that the minimum shaft diameter is 1.0000". The bracket hole diameter was set to 0.754 with a tolerance of ±0.0034 to maintain RC7 clearances with respect to the class standard X.XXX tolerances.

## Communicate

### Reflection
Initially, all global variables were set to the values from the hand calculations. All feature dimension values were assigned from equations derived by hand, and I added Force, Ultimate Strength, and Factor of Safety values. After correction, the only value that changed from initial calculations was the thickness of Feature B. No problems occurred after correction, and both the model and drawing reflected the new value after changing it. Below are the corrected values, equations, and drawing.

![global variables corrected](globalVariablesA6Corrected.png)

![parametric Equations Corrected](parametricEquationsCorrected.png)

![project A6 drawing corrected](ProjectA6Corrected.PNG)

For the width of Feature C, the dimensions were made to the X.XXX and are a functional surface. Feature C width requires precision to the 3rd decimal place because the dimensions of a & b of the rigid body have to meet a certain clearance. However, for the diameter of Feature A, the dimensions were made to X.XX place and were a non-critical feature. The dimensions were made to be in the X.XX tolerance class in order to meet the minimum required cross-section to handle the load applied. 

When it came to dimensioning the link, I thought the most important information to communicate was the clearances of both holes with respect to the sheet standard tolerances of the shaft instead of the shaft's respective class. 

### Lessons Learned
When it comes to dimensioning tolerances according to ANSI standards, I think the easiest way to communicate tolerances is not bilaterally but through minimum and maximum dimensions. Deciding whether the values calculated earlier represent a minimum/maximum size or a specified range. Tolerancing and 


### Links of parts
Bracket: https://drive.google.com/file/d/10mQg6InxneZ2nzuYpJTkJsqIUi-GlR_o/view?usp=drive_link
Bracket Link: https://drive.google.com/file/d/10mQg6InxneZ2nzuYpJTkJsqIUi-GlR_o/view?usp=drive_link



