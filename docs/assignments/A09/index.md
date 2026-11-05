# A9 – Pulley System Design

## Objective

The purpose of this assignment is to design a pulley system to transfer power between two parallel axes that follows a given set of requirements. 

### Requirements

- Parallel axes must be seperated by a center distance of 4 - 6 inches (6 in. chosen)

- Both pulleys must have a diameter of 3 inches

- Rotational speed must be between 1000 - 2000 rpm (1700 rpm chosen)

- Static belt tension must be between 4 - 6 lbf (5 lbf chosen)

- Pulleys must be made from aluminum, ABS, or steel and may include groove and shaft diameter (ABS chosen)

- Minimum safety factor of 3

- Assume the belt is made from polyurethane rubber with a yield strength of 3.25 MPa (471 psi) at 20% strain

- Geometric constraint:

<img width="445" height="198" alt="Screenshot 2026-11-04 125000" src="https://github.com/user-attachments/assets/11ff2fe2-0ed2-4c5c-9e9a-068a5b3b967c" />


## Pulley

<img width="381" height="494" alt="IMG_0006" src="https://github.com/user-attachments/assets/2af2822e-77df-4958-b504-3998e44bbabb" />

I began by drawing a free body diagram of the left pulley. Next, I listed all the knowns and unknowns below it. Then, I used the formulas provided during lecture to calculate the tight and loose tensile forces, diameter of the belt, and the circumference of the belt. I assumed that there would be no slippage, resulting in a friction coefficient of 1. 

## Shaft

<img width="382" height="492" alt="IMG_0007" src="https://github.com/user-attachments/assets/bf83c872-bedf-4937-ab59-237ff9c90321" />


Next, I moved onto the shaft specifications. I began by drawing the free body diagram. Next, I listed the knowns and unknowns. Then, I used the formulas provided in lecture to calculate the minimum diameter and cross-sectional area. The shaft is made of 1060 hardened steel, so I had to gind the yield strength of this material online.  

## Journal Bearing 

<img width="382" height="492" alt="IMG_0008" src="https://github.com/user-attachments/assets/1aeef946-f098-4aae-87db-04777dfd29dd" />

Then, I moved onto the journal bearing specifications. I began by drawing the free body diagram. Next, I listed the knowns and unknowns. The bearing length I chose was 2.0 inches. I then calculated the pressure, surface linear velocity, and PV ratting using values I found in previous sections. I compared these new values to Table 4 on page 2442 of the Machinery's Handbook to find a suitable material and went with Acetal. I chose this material because its listed load capacity, surface speed, and PV limit all exceed my calculated values, but aren't outlandishly greater than my calculated values to minimize costs.  

## Frame 

<img width="383" height="494" alt="IMG_0009" src="https://github.com/user-attachments/assets/f409a605-0012-4c02-ad86-48e5809fa17f" />

I designed my frame based on the concept shown in Appendix A. For the front view, I used the given 3 inch diameter of the pulleys and the chosen 6 inch center distance. I added extra lengths on the side for support. For the side view, I used the chosen 2 inch length of the jounrnal bearing, then added a little extra length for support. For the material, I chose acetal since I already known it can withstand the calculated loads. 

## Engineering Lessons Learned

This assignment taught me how to apply stress analysis, solid mechanics, and basic physics in an interconnected project, like a pulley system. Specifically, I learned how the formulas provided in the lecture, when combined, can be used to find belt specifications like its diameter and circumference. 

**Total Time Spent:** 5 hours

## References 

<img width="741" height="285" alt="Screenshot 2026-11-04 205516" src="https://github.com/user-attachments/assets/562e8a5e-3095-4e85-baa1-a18f6a31d4c8" />

