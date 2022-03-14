# Metal B***hes

During the STUDIO I course, students had to explore:

Characteristic of all sensations and perceptions that is specific to vision. Radiation that is considered from the point of view of its ability to excite the human visual system.

The use of light in a development aluminum process, we explore two different phenomenons, the Reflection and de dispersion of  light, with the purpose of creating layers of color in the material.

## AIM

*Experiential spaces birthing different resonations and divergent spatial cognition.*

The addition of grinding textures derived from the artworks of Richard Serra creates a visual disposition of the panels of the Pavilion, hence creating illusions depending on the way light hits the texture. The scale of a Pavilion helps us understand the usability and scalability of the Molding+Grinding process better.

## DESIGN
The design was an exploration in trying to work with complex shapes but at the same time try and inculcate some geometric modularity to it, for instance the Sydney Opera house uses certain sliced geometries from a bigger simpler geometry; i.e. a sphere, for it’s form.

The concept of self-solidarity geometries with varied spatial cognition comes from Richard Serra, his work with large scale sheet-metal installations and other art has highly influenced our design decisions.

![concept](1.Intro/src/concept.jpg)
*Spatial Cognition study by artbykla*

![render](1.Intro/src/render.jpg)
*Architectural rendering for the VRS Pavilion*

## MANUFACTURING WORKFLOW

![workflow](6.Fabrication/src/workflow.png)
*Workflow Idealization*

### Tool

The grinding tool available to us is Prevost TDG S2200R. We explored this tool manually on three different metal surfaces, with three different grinding bits. The tool was then used to create a manual texture library for us to refer from and make design and production decisions. The Texture Library also contains different type of sheet metals: Raw Aluminum, Brass & Raw Steel.

![tool](2.Hardware/src/tool.png)
*Prevost TDG S2200R*

![material](2.Hardware/src/material.png)
*Raw Aluminum Texture Pattern Library – 1*

![material2](2.Hardware/src/material2.png)
*Raw Aluminum Texture Pattern Library – 2*

## End-Effector Design

The end-effector design began with looking at the angle at which the Prevost will be held, and the assembly. Regarding angle, the 90 degrees model was chosen because it resulted in less singularities and collisions in the grasshopper simulation.

![end-effector1](3.End-effector/src/end-effector1.jpg)
*End-Effector design iterations*

Regarding assembly, we created mock-ups using MDF to determine what would be the ideal way to install onto the robot. Given that it will be mounted onto the robot as the last step, we chose the design that places the Prevost 173mm below the center of the ABB’s end-effector. The final end-effector was in aluminum, taking these tested dimensions and assembly method.

![end-effector2](3.End-effector/src/end-effector2.gif)

![end-effector3](3.End-effector/src/end-effector3.jpg)

![end-effector4](3.End-effector/src/end-effector4.jpg)
*Aluminum End-Effector close-ups*

### Grinding Flat Surface

The end-effector was put into test on flat surfaces first. Through this testing, we built an understanding of the bits, constructed a simple library of texture-variations that resulted from the different speeds and angles.

![fabrication1](6.Fabrication/src/fabrication1.jpg)

![fabrication2](6.Fabrication/src/fabrication2.jpg)
*Testing parameters for simple strokes*

![fabrication3](6.Fabrication/src/fabrication3.jpg)
*Testing parameters for designed pattern*

The initial parameters in consideration were speed and angle. The tests, however, informed us of the different natures (or tolerances) of the bits, as well as the nature of the surface (flatness). These considerations would affect our next iteration on curved surfaces.

![fabrication4](6.Fabrication/src/fabrication4.jpg)

### Molding

![hardware1](2.Hardware/src/hardware1.png)

The molding was made by a process called metal stamping. In this process the punch draws the blank to form the shape while the blank holder controls the flow of metal into the die cavity.

We have two different molds, the first one was made with a high performance polyurethane and the second one was made with wood and MDF.

![hardware2](2.Hardware/src/hardware2.png)
*Mold v_1.0*

![hardware3](2.Hardware/src/hardware3.png)
*Mold v_2.0*

After the test with the first mold we noticed that the space between the bank holders and the shape needs to increase and we should find a way to avoid the aluminum movement in the punt movement, so we designed this mold to get the best result.

![hardware4](2.Hardware/src/hardware4.gif)
![results](6.Fabrication/src/results.png)
*Molding Results*

### Grinding Curved Surface

![fabrication6](6.Fabrication/src/fabrication6.png)

This is the final step of our production, as we put everything we have studied previously into testing. The robotic grinding on curved surfaces brought a number of unexpected challenges and called for improvisation such as re-adapting the end-effector for another function, milling.

The first biggest challenge we encountered was the discrepancy of curvature in the 3D model and the actual mold. The discrepancy caused potential crashing as well as inconsistent texture results.

### Initial Pseudocode

![pseudocode](4.Robot-Sinulation/src/pseudocode.png)

### Adapted Pseudocode

![pseudocode2](4.Robot-Sinulation/src/pseudocode2.png)

### Workflow Idealization

![workflow2](6.Fabrication/src/workflow2.jpg)

### Workflow Reality

![workflow3](6.Fabrication/src/workflow3.jpg)


### Surface Calibration explorations:
### 3D Scan using LiDAR

![fabrication7](6.Fabrication/src/fabrication7.png)

### Manual Point-Mapping

![fabrication8](6.Fabrication/src/fabrication8.png)

Within the constraint of – ø 3mm or ø 6mm, any bit could be used for the purpose of calibrating, marking, or even cutting the metal surface.

![fabrication9](6.Fabrication/src/fabrication9.png)

### Spring-back

Spring-back in the material helped the grinding process to address the inconsistent contact pressure.

![fabrication10](6.Fabrication/src/fabrication10.gif)
![fabrication11](6.Fabrication/src/fabrication11.gif)

### Grinding Test on Mold v_1.0

![fabrication12](6.Fabrication/src/fabrication12.png)
![fabrication13](6.Fabrication/src/fabrication13.png)

### GRINDING_VRS PAVILION

We took the understanding from the test mold:

1. safety measures
2. sheet spring-back 
3. manual surface calibration 
and proceeded to the next set of aluminum molds.

![fabrication14](6.Fabrication/src/fabrication14.png)

### The Pattern

The pattern is defined flat. It is then projected to the mold, translated into different bits and different plane rotations for the robotic grinding.

![fabrication15](6.Fabrication/src/fabrication15.png)

The stroke thickness is defined by the tilt.. We intended higher waves to have thicker strokes (thus, closer to 20°).

![fabrication16](6.Fabrication/src/fabrication16.gif)
![fabrication17](6.Fabrication/src/fabrication17.png)
![fabrication18](6.Fabrication/src/fabrication18.png)

For rotary burr, speed would determine the thickness and nature of the stroke. Defining the angle was irrelevant.

![fabrication19](6.Fabrication/src/fabrication19.gif)
![fabrication20](6.Fabrication/src/fabrication20.png)
![fabrication21](6.Fabrication/src/fabrication21.png)

### The Process

![process1](6.Fabrication/src/process1.png)

### Milling

The outline of the pieces had to be cut with higher precision. With the presence of ø 3mm and ø 6mm drill-bit, the tool upgraded to uphold the task of robotic milling.

![process2](6.Fabrication/src/process2.png)

### Callibrating for Milling

Milling required higher precision in surface calibration. Manual surface calibration, especially on curved surfaces, has limits to achieving this precision.

![process3](6.Fabrication/src/process3.gif)
![process4](6.Fabrication/src/process4.png)
![process5](6.Fabrication/src/process5.png)

## Takeaways

The aim is to raise accuracy and shrink time-consumption,, especially in the two areas:

![process6](6.Fabrication/src/process6.png)

## Installation

![installation](1.Intro/src/installation.png)

## Scalability

Imagining curved geometries in bigger scales, carrying textures to redirect light.

![further](1.Intro/src/further.png)


------

Metal B***hes is a collaborative of IAAC, Institute for Advanced Architecture of Catalonia developed at Master in Robotics and Advanced Construction in 2021 by

Students: Mit Patel, Yeo Jeong Kim, Andrea Najera 

Faculty: Raimund Krenmueller, Marielena Papandreou, Luciano Carizza


