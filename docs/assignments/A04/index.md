# A4 – [Motor Mount]

## Objective

The goal of this assignment is to design a mount mount for a brushed 24V DC gear motor with a 99.5:1 Planetary Gearbox. The motor will be attached to a rigid wall, A, using two features. For both features, first design for yield strength, then design for a maximum deflection of 0.30 mm at the free end. The mount can be made up of either ABS, PETG, or PLA. During the design process, ensure a safety factor of 3 and neglect the weight of the motor. The applied load, P, is 300 N. 

<img width="448" height="282" alt="Screenshot 2026-09-16 151347" src="https://github.com/user-attachments/assets/dea8f482-6429-41ba-9fe0-402623175950" />

## Feature 1

I decided to use PLA for the material of my motor box since it has the greatest Young's modulus, making it the most rigid of the three materials. Listed below are some of the mechanical properties of PLA. 

<img width="407" height="271" alt="Screenshot 2026-09-16 154312" src="https://github.com/user-attachments/assets/e26b6936-82ad-42e0-8949-62712112cd2c" />

### Knowns

Length of Motor: 92.6 mm (I used the maximum dimensions from the tolerance ranges provided in Appendix A)

Diameter of Motor: 22 mm (From Appendix A)

Load (P) = 300 N

Safety Factor: 3

Max Deflection: 0.30 mm 

Yield Strength (Sy) = 60 MPa

Young's Modulus (E) = 3.6 GPa

### Unknowns

Beam Width (b) = ?

Beam Length (l) = ?

Beam Height (h) = ?

Maximum Bending Stress (σ) = ? 

### Calculations

<img width="248" height="318" alt="Screenshot 2026-09-17 014718" src="https://github.com/user-attachments/assets/c7b6487a-e18e-47c4-8c95-f99e676fb75c" />

In the calculations shown above, I assumed the thickness and length of feature 1 based on the dimensions given in Appendix A. I added the positive tolerances onto the dimensions to obtain the maximum possible length and thickness of the mount.

<img width="248" height="331" alt="Screenshot 2026-09-17 014740" src="https://github.com/user-attachments/assets/ae77b210-7690-41d6-9957-911fb9497634" />

Using the values found in the previous page, I calculated height based on allowed stress as well as the maximum deflection. I then took the higher height value of the two to ensure it meets the required deflection and stress constraints.

### Feature 2 

This feature will also be made of PLA material for the same reasons as feature 1, but also to avoid overcomplicating things. 

### Knowns

Load (P) = 300 N

Safety Factor: 3

Max Deflection: 0.30 mm 

Yield Strength (Sy) = 60 MPa

Young's Modulus (E) = 3.6 GPa

Allowable Stress (σ) = 20 MPa

### Unknowns 

Width (b) = ?

Length (l) = ?

### Calculations

<img width="245" height="320" alt="Screenshot 2026-09-17 034259" src="https://github.com/user-attachments/assets/11a65212-5c1f-4dfb-8a9f-717f4ea7a97d" />

<img width="245" height="331" alt="Screenshot 2026-09-17 014740" src="https://github.com/user-attachments/assets/198c5a63-c216-453f-875b-b449dbd7f6b3" />

I followed the same steps I took for feature 1 to calculate the dimensions for feature 2. I used the same thickness assumption as I did in feature 1. When calculating the height, I got two very different values, for which I'm not entirely sure why. I decided to go with the larger value just to be on the safe side. 

## Isometric Sketch

<img width="243" height="265" alt="Screenshot 2026-09-17 034128" src="https://github.com/user-attachments/assets/b04a8b3c-2c80-42f6-bfe1-1e1b502420ad" />

The isometric sketch is provided above. Notice how the height of feature 2 is much bigger than the other dimensions. This is because I used the greater calculated value from my feature 2 calculations. 


## Communicate

### CAD Model



[Mechanical Properties of PLA](https://www.sciencedirect.com/science/article/pii/S2405844024140972#sec2)

<img width="354" height="167" alt="Screenshot 2026-09-16 164735" src="https://github.com/user-attachments/assets/c342ac1a-73c5-4642-a68c-78692beca72d" />

Appendix A

<img width="198" height="302" alt="Screenshot 2026-09-16 164955" src="https://github.com/user-attachments/assets/eb8af350-2318-4850-9e76-70eda9efb908" />

Appendix B




