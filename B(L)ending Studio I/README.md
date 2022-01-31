# Robotic-Craft-Light-Metals
In this project we research the automatization of manufacturing metal profiles. More specifically the bending of structural profiles to precisely achieve a desired curve. In this project we explore the bending of aluminum profiles which are ideally shaped for lightweight reinforced structures in automotive and aerospace industries.

The properties of this thin material allow for easier manufacturing, manipulation and transportation processes.

![](1.Intro/1. aluminum sailboat structure.png)

##1. Metal shaping methods

Almost any metal manufacturing process can be either manually, motorized or automatically operated.


Manual		>		Motorized		>		Automatic

![](1. Intro\2. slip roll machine.png) ![](1. Intro\3.bending motorized.png) ![](1. Intro\4. bending automatic.png)

In our case we wanted to develop an automatic process on aluminum angle bending, that implied a motorized process with a predictable result on the manufacturing from the design phase.

On the following table, there is a comparison among the operational dimensions (in 1, 2 or 3 directions) of manufacturing 3 different shapes of metals.

![](1. Intro\5. operation-table.png)

The dotted cases are still to be fully industrially developed to get the desired automatic process. Therefore, we are focused on the dynamic or non-regular deformation in 2 directions on metal angles and profiles.

More exactly, we chose the “L” shaped angles, with identical wall lengths to ensure the biggest structural strength with the minimum amount of material with symmetrical results, also giving us the chance to test the deformation on both sides.

##2. Computation & Workflow

Fixing all other parameters, we variate the increment distance and study its relation to the change in the degree of curvature.

![](1. Intro\Computation-workflow\1.png) ![](1. Intro\Computation-workflow\3.png)

Varying only the increments, we get record the curvatures for each iteration and plot them:

![](1. Intro\Computation-workflow\2.png)

Using linear regression, we find the relationship between Increment Distance and Curvature:

![](1. Intro\Computation-workflow\DataGraphFinal.png)

We find that the slope m = 26.48
 Increment Distance = 26.58 * Radius of Curvature

![](1. Intro\Computation-workflow\Kangaroo Animation 3.gif)
![](1. Intro\Computation-workflow\Screenshot 2022-01-13 110718.png)
![](1. Intro\Computation-workflow\Screenshot 2022-01-13 110558.png)
![](1. Intro\Computation-workflow\Screenshot 2022-01-13 110740.png)
![](1. Intro\Computation-workflow\Robot big pic.png)

These were the different results we came up with after using the same parameters along the process in one of the tests:

![](1. Intro\Computation-workflow\Screenshot 2022-01-13 111005.png)

The robot used to bend a rod which would replicate the desired curve to be bent.

![](1. Intro\Computation-workflow\Frame_00080.png)

We used a physical paper template to compare all the curvatures on one single grid.

![](1. Intro\Computation-workflow\Screenshot 2022-01-13 112015.png)

##3. Design and Fabrication

Our design intent was to create an organic modular shape that could interact with the reflection of the light where our metal structure would become the skeleton of our shape.

Our first decision was to start from a double curved shape that would deform the structure symmetrically in two directions.

![](6. Fabrication\6. double curvature surface.png)
Double curvature surface

Then we defined the main structure that would adapt to the original surface or skin, where we needed 2 identical horizontal profiles, tied with 2 straight vertical profiles on the sides and 6 curved profiles in between (10 pieces in total).

![](6. Fabrication\7. reflecting structure and metal structure.png)
Reflecting skin over the metal structure
![](6. Fabrication\8. exploded view.png)
Exploded view of the structure

Then we defined the final dimensions of our design making it big enough to generate interesting curves in our design disregarding its weight as the material offered an excellent advantage.

The final piece would not be much bigger than 1 meter long by 40 cm width and 36 cm deep.

![](6. Fabrication\9. measurements.png)
General dimensions
![](6. Fabrication\10. scale.png)
Human scale

###Structure and joints

The final structure would be built in 20x20 “L” shaped profiles made of aluminum 1050T alloy. This specific aluminum will give an even lighter condition and easier manufacturing in bending and assembling processes.

![](6. Fabrication\11. metal structure.png)

10 pieces
2x	400 mm (straight)
2x	485 mm
2x	612 mm
2x	687 mm
2x	1160 mm (top and bottom)

32 rivets
D4,2mm holes
d4mm rivets
M4x10 bolts and M4 nuts and washers


The 10 pieces of the structure would be joined together with 4mm rivets (2 on every joint) as shown below.

![](6. Fabrication\12. rivets.png)

###Fabrication processes

In the profiles manufacturing we followed the next steps:

![](6. Fabrication\13. marking profiles.png)
![](6. Fabrication\14.shrinking profiles.png)
![](6. Fabrication\15. comparing with the template.png)
![](6. Fabrication\16. marking any error.png)
![](6. Fabrication\17. hammering the error.png)

For the structure assembly, we first joined the structure with bolts, nuts and washers to test the prototype and the additional materials of the skin.


![](6. Fabrication\18. taping the structure.png)
![](6. Fabrication\19. marking the holes.png)
![](6. Fabrication\20. drilling holes.png)
![](6. Fabrication\21. filing holes.png)

###Testing with light and reflection

On our lighting test we worked on both a reflective material and direct illumination.
The material we used as the skin test is a PVC and cotton based fabric with a mirror effect layer that while wrinkling it along the structure would give an interesting contrast over the aluminum skeleton, but not consistent enough.

![](6. Fabrication\22. skin test.png)

Additionally, we tested a different lighting with direct illumination from RGB LED stripes hidden behind the aluminum structure, but this required a full research on programming the different colors and positions of this light. Below there are some examples in white light.

![](6. Fabrication\23. light test.png)

##4. Potential and next steps

![](1. Intro\Computation-workflow\big picture render_3_edit.png)
