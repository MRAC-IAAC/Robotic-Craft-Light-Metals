# B(L)ending Studio
In this project we research the automatization of manufacturing metal profiles. More specifically the bending of structural profiles to precisely achieve a desired curve. In this project we explore the bending of aluminum profiles which are ideally shaped for lightweight reinforced structures in automotive and aerospace industries.

The properties of this thin material allow for easier manufacturing, manipulation and transportation processes.

![aluminum-siailboat](src/aluminum-sailboat-structure.png)

## 1. Metal shaping methods

Almost any metal manufacturing process can be either manually, motorized or automatically operated.


            > Manual		>		Motorized		>		Automatic

![machinery](1.Intro/src/machinery.png)

In our case we wanted to develop an automatic process on aluminum angle bending, that implied a motorized process with a predictable result on the manufacturing from the design phase.

On the following table, there is a comparison among the operational dimensions (in 1, 2 or 3 directions) of manufacturing 3 different shapes of metals.

![operation-table](1.Intro/src/operation-table.png)

The dotted cases are still to be fully industrially developed to get the desired automatic process. Therefore, we are focused on the dynamic or non-regular deformation in 2 directions on metal angles and profiles.

More exactly, we chose the “L” shaped angles, with identical wall lengths to ensure the biggest structural strength with the minimum amount of material with symmetrical results, also giving us the chance to test the deformation on both sides.

### Shrinking and Stretching
Definition: A tool for deforming metal, consisting of mechanically shrinking or stretching a specific area.

![shr-str](1.Intro/src/shr-str.png)

* Mechanical Behaviour

![mechanical-behavior](1.Intro/src/mechanical-behavior.png)

* Parameters

![operation-table](1.Intro/src/parameters.png)

## 2. Computation & Workflow

### Testing

![testing](2.Robot-Simulation/src/testing.png)

Goals:
- Compare shrinking and stretching results
- Test its regularity with constant repetition
- Test incremental variations and compare to curves

Test: 
- Sheet metal thickness: 0.8 and 1.3 mm
- 14 different increment values (5 - 35 mm)
- 3 depths: 6, 12 and 18 mm
- Length: 15 cm
- Aluminum 1050T 
- ‘L’ section profiles (20x20mm)

### Manual Testing Results

![manual-testing](2.Robot-Simulation/src/manual-testing.png)

- Force variable fixed by blocking the ending angle
- Better results on shrinking, also preferable for structure facade
- 0.8 mm aluminum required less mechanism stress
- Best depth 18 mm

## Process

Fixing all other parameters, we variate the increment distance and study its relation to the change in the degree of curvature.

![increments](2.Robot-Simulation/src/increments.png) ![increments2](2.Robot-Simulation/src/increments2.png)

### Computation

Varying only the increments, we get record the curvatures for each iteration and plot them:

![increments3](2.Robot-Simulation/src/increments3.png)

Using linear regression, we find the relationship between Increment Distance and Curvature:

![linear-regression](2.Robot-Simulation/src/linear-regression.png)

We find that the slope m = 26.48
 Increment Distance = 26.58 * Radius of Curvature

![curve1](2.Robot-Simulation/src/curve1.png)
![curve2](2.Robot-Simulation/src/curve2.png)
![curve3](2.Robot-Simulation/src/curve3.png)
![curve4](2.Robot-Simulation/src/curve4.png)

After testing 4 rods under the same conditions of equal increments, depth and force of cutting, we realise that the tool is not repeatable and we get very different curves.

![curve5](2.Robot-Simulation/src/curve5.png)

### Robotics

If we can confidently bend something else repeatably, then the robot can create a dynamic template by replicating the desired curves.

![robot-template](2.Robot-Simulation/src/robot-template.jpg)

We fix the 2 edges of the polycarbonate rod, setting it’s boundary conditions as fixed, record its shape, and import it shape to Grasshopper and check if we’re able to replicate the curvature by simulating it with Kangaroo.

![paper-layout](2.Robot-Simulation/src/paper-layout.png)

![robotic-templates](https://youtu.be/TVY--9p6iUU)

## 3. Design and Fabrication

Our design intent was to create **an organic modular shape that could interact with the reflection of the light** where our metal structure would become the skeleton of our shape.

Our first decision was to start from **a double curved shape** that would deform the structure symmetrically in two directions.

![double-curvature](6.Fabrication/src/double-curvature.png)

*Double curvature surface*

Then we defined the main structure that would adapt to the original surface or skin, where we needed 2 identical horizontal profiles, tied with 2 straight vertical profiles on the sides and 6 curved profiles in between (10 pieces in total.

![reflecting-and-meta-structure](6.Fabrication/src/reflecting-and-meta-structure.png)
*Reflecting skin over the metal structure*

![exploded-view](6.Fabrication/src/exploded-view.png)
*Exploded view of the structure*

Then we defined the final dimensions of our design making it big enough to generate interesting curves in our design disregarding its weight as the material offered an excellent advantage.

The final piece would not be much bigger than 1 meter long by 40 cm width and 36 cm deep.

![general-dimensions](6.Fabrication/src/general-dimensions.png)
*General dimensions*

![scale](6.Fabrication/src/scale.png)
*Human scale*

### Structure and joints

The final structure would be built in 20x20 “L” shaped profiles made of aluminum 1050T alloy. This specific aluminum will give an even lighter condition and easier manufacturing in bending and assembling processes.

![metal-structure](6.Fabrication/src/metal-structure.png)

**10 pieces**
2x	400 mm (straight)
2x	485 mm
2x	612 mm
2x	687 mm
2x	1160 mm (top and bottom)

**32 rivets**
D4,2mm holes
d4mm rivets
M4x10 bolts and M4 nuts and washers


The 10 pieces of the structure would be joined together with 4mm rivets (2 on every joint) as shown below.

![rivets](6.Fabrication/src/rivets.png)
*Riveted joint*

### Fabrication processes

In the profiles manufacturing we followed the next steps:
![fabrication1](6.Fabrication/src/fabrication1.png)


For the structure assembly, we first joined the structure with bolts, nuts and washers to test the prototype and the additional materials of the skin.

![fabrication2](6.Fabrication/src/fabrication2.png)

### Testing with light and reflection

On our lighting test we worked on both a reflective material and direct illumination.

The material we used as the skin test is a PVC and cotton based fabric with a mirror effect layer that while wrinkling it along the structure would give an interesting contrast over the aluminum skeleton, but not consistent enough.

![skin-test](6.Fabrication/src/skin-test.png)
*Test of reflective material*

Additionally, we tested a different lighting with direct illumination from RGB LED stripes hidden behind the aluminum structure, but this required a full research on programming the different colors and positions of this light. Below there are some examples in white light.

![light-test](6.Fabrication/src/light-test.png)
*Test of lighting*

## 4. Potential and next steps

We are still scratching the surface of roboticizing the custom metal forming process. Starting with understanding metal bending in 2D, this knowledge is imperative to be able to extend this process into 3D surfaces and beyond.

![future1](1.Intro/src/future1.png)
*Technology curve projection*

Furute iterations could include sensors for feedback and correction or AR guided tools.

![future2](1.Intro/src/future2.png)
*Laser correction*
