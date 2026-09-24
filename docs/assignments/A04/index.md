# A4 – [Motor Mount]

## Objective

Design a motor mount using the (Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox) HERE which attaches to the rigid wall A. For both features, first design for yield strength and then design for a maximum deflection of .30 mm at the free end. You may select ABS, PETG,  or PLA as a motor mount material. 

## Analyze

### Research
Before designing this mount, I did some initial research into what design considerations I should have when designing motor mounts by looking at the article linked at the bottom of the page. Looking at all the references and the materials we could make this mount from, I also looked at an article about designing 3d printed motor mounts specifically. The article is linked below. In order to make the model more accurate, I ignored the instruction to ignore the mass of the motor and calculated all values with the mass of the motor. I modeled the mass of the motor as a distributed load the size of its largest diameter given from the drawing provided by the website. I chose ABS as my material for the mount.

![image of motor measurements](motorDimensionsA4.png)

In my initial sketch of the design, I decided that the mount would be 30mm wide and calculated for the thickness of the mount in all stress and deflection calculations. For all calculations, a factor of safety of 3 was used. 

![inital sketch of motor mount](initialDesignSketch.png)

### Feature 1

My first calculations were done to find the thickness with respect to the yield strength of ABS. As a challenge, I decided to try to accurately determine the thickness of feature 1 by treating the feature as a rectangular plate with a transverse hole in it. I used the chart below to find the stress concentration factor. The size of the hole was set to 18.3mm.

![stressConcentrationFactor Chart](stressConcentrationFactor.gif)

![figure 1 bending stress plate calculation](figure1BendingStressCalc1.png)

![figure 1 bending stress as a beam](figure1BendingStressCalc2.png)

Then I calculated the thickness of feature 1 to minimize the deflection to a minimum of 0.00030mm.

![figure 1 deflection](figure1DeflectionCalc3.png)

Because the thickness of feature 1 that minimizes deflection is larger than the thickness that can handle the yield strength of the mount. The final thickness of feature 1 was set to be 13.1 mm.

### Feature 2

When calculating the thickness of the mount with respect to yield strength, feature 2 was modeled as a cantilever beam with a moment on the end. The same 30 mm width of the mount was used in all calculations. For feature 2, when calculating with respect to yield strength, only the bending stress of a cantilever beam was used in the calculations.

![figure 2 bending stress](figure2BendingStressCalc.png)

![figure 2 deflection](figure2DeflectionCalc.png)

Same with feature 1: the thickness of feature 2, when calculated, trying to minimize deflection could also handle the yield strength of the mount. The final thickness of feature 2 was set to 24.0 mm.

### Final Sketch

The final design of the mount was drawn according to the thicknesses calculated. The length of feature 1 was set to 30 mm, and the length of feature 2 was set to the length of the mount. In feature 1, I placed a counterbore for the 2 mm offset that is on the face of the axle side of the motor.

![final design sketch](finalDesignSketch.png)

### CAD Model

Before creating any sketches, I first made the material of the mount according to the material properties sheet provided by SpecialChem. I opted to only include the properties listed by SpecialChem and not assign values to the rest.

![material properties of ABS](materialPropertiesA4.png)

![parametric equations](parametericEquations.png)

Then I created global variables for all the measurements I set in the final sketch of the motor mount. Before creating the sketch of the side profile of the mount.

![front profile sketch](initialSketchFrontProfile.png)

I dimensioned the sketch with respect to each feature's measurements using the global variables I created. Then I extruded the mount and dimensioned it using the length of feature 1.

![extruded front profile](extrudeFrontProfile.png)

After extruding the side profile of the mount. I created the hole for the front face of the motor with a counterbore for the 2mm offset and a hole sized to 6.3mm for the shaft of the motor.

![motor hole feature](motorHoleFeaturee.png)

Afterwards, I created the holes to attach the face of the motor to the mount. First, I created the hole and set its diameter to 3.4mm 



For the sake of the assignment and my time, I decided to calculate deflections without considering the holes put into the design. 

used this for calculating bending stress:
https://mechanicalc.com/calculators/stress-concentration/

Material properties taken from:
https://www.specialchem.com/plastics/guide/acrylonitrile-butadiene-styrene-abs-plastic

## Decide


## Communicate

#### Links to articles used:
  Designing motor mounts article:
https://www.automate.org/motion-control/tech-papers/design-considerations-for-gearmotor-applications
  Designing 3d printed mounts article:
https://www.tinkercad.com/things/avvN77l4yc1-tt-gear-motor-mount

