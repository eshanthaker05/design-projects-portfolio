# A7 – [FEA on Bracket]

## Objectives

- Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.

- Ensure high stiffness, strength, and lightweight optimization through iterative design.

- Conduct multiple FEA simulations, refining geometry based on results.

- Perform static stress analysis, including constraints, loading, and meshing selection.

- Interpret data by identifying max stress, displacement, and safety factors.

- Optimize the design by modifying geometry to enhance performance.

- Document the entire process with images, calculations, and insights.
  
- Reflect on key engineering lessons learned and time spent.
  
## Known Values

The following values are known/given from A5: 

**Material:** Titanium (Ti-6Al-V4) 

**Young's Modulus (E):** 15,954,151.2 psi

**Yield Strength (Sᵧ):** 120,091 psi

**Allowable Strength (σ):** σᵧ/SF = 30,022.8 psi

**Density:** 0.160 lb/in^3

**Applied Load (F):** 700 lbf

**Safety Factor:** 4

**Max Deflection** = 0.005 in

Assume no failure due to direct shear stress

## FEA Setup 

For my first test, I decided to use my original design and see how close it got to the 7% convergence under FEA analysis. To set up my FEA constraints, I hit Applications>Simulate>Home>Displacement. I selected the back plane to constrain, as shown in the image below. 

<img width="338" height="218" alt="Screenshot 2026-10-20 230736" src="https://github.com/user-attachments/assets/403bb0f5-1f51-43ee-bb8c-f8bca848f87f" />

Next, I added the distributed force of 700 lbf onto Feature A. I hit Force/Moment and inputted the load onto Feature A, making sure to change units to lbf. I hit Ok and my resulting model can be seen in the image below. 

<img width="338" height="214" alt="Screenshot 2026-10-20 231912" src="https://github.com/user-attachments/assets/8a3ffa28-df22-4450-9bef-39f81a97b751" />

I didn't change the material of my model, as outlined in the instructions for this assignment. 

## Design 1








