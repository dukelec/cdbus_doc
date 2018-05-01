

## CDBITE Module Connection Solution - Solderless, Low Cost, Small Volume

<img alt="adapter_cdbite" src="img/cdbite_demonstration.gif">

### PCB Considerations

 - First confirm the distance between the two sides of the needle tip, because when inserting the module, only one side of the thimble will be pushed in first. At this time, a small amount of space shall be left on the other side so that the module can be put in smoothly;
 - In order to prevent the solder from entering the interior of the thimble, both ends of the pad are separated from the two ends of the needle tube by a certain distance, and corresponding positions of the needle head are also to be slotted to prevent siphon from occurring;
 - There will be a small groove near the head of the needle tube. In order to prevent the groove from breaking, both sides need to be fixed by soldering;
 - Paste too much will climb up, not beautiful, so the width of the pad is best slightly smaller than the diameter of the needle, while the paste opening is not continuous, should be divided into multiple sections to reduce solder paste volume.

<img alt="cdbite_pcb" src="img/cdbite_pcb.png">

<img alt="cdbite_with_models" src="img/cdbite_with_models.png">

### Prepare Thimble Fixture

If there is no fixture, the placement of the thimble will be time-consuming, and the thimble will easily deviate from its original position during soldering, and it will not be neat after soldering.

The simplest fixture fabrication method is to use a stencil commonly used for circuit board mounting. The thickness of the stencil can exceed the height of the tip (for example, the tip of a 0.48 mm diameter needle has a tip height of 0.24 mm, and a stencil with a thickness of 0.3 mm can be selected).

The outer frame of the fixture is different from the PCB layout, and it is formed by sliver-shaped openings splicing (the rectangular pad is used in the figure). There is a little distance at the joint to prevent the main body from falling off. After receiving the stencil, it is cut by hand grinding, then you can obtain the fixture.

The fixed position of the thimble and the positioning hole are also formed by the paste openings.

The size of the fixture should not be too large to avoid interference with other SMD components (or add additional openings for them).

When stencil documents are issued, it is important to clearly indicate their purpose. It is best to personally confirm the final production documents.

<img alt="fixture_in_pcb" src="img/fixture_in_pcb.png">

<img alt="fixture_real" src="img/fixture_real.jpg">


### Production Process

1. Depositing solder paste on the PCB by using conventional stencil;
2. Placement of other SMD devices other than thimble;
3. First insert the positioning pin into the fixture, and then put it together to the PCB target position;
4. Put thimbles in turn into fixed fixture;
5. Place the entire circuit board containing fixtures into the reflow oven, or manually use a hot-air soldering station (usually seeing a small amount of tin on the side of the needle tube represents soldering completion);
6. Carefully remove the fixture, because the flux is sticking, it is easier to remove it by pulling it up from the corner;
7. The final work is completed after soldering the remaining connectors.

<img alt="fixture_in_use" src="img/fixture_in_use.jpg">

### License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

Author: Dukelec. Product descriptions and instructions for this part must retain this name: CDBITE.
 
