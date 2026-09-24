# A5 – [Bracket Design ]

## Objectives

-  Conduct stress analysis to determine appropriate dimensions for structural features.

- Generate free body diagrams (FBDs) to visualize forces and constraints for each feature.\

- Identify and document known and unknown variables, assumptions, and algebraic models for stress calculations.

- Perform stiffness analysis to establish minimum required dimensions based on deflection constraints.

- Compare stress and stiffness analyses to ensure structural integrity and compliance with given constraints.

- Create detailed multiview sketches illustrating dimensions derived from both stress and stiffness analyses.

- Reflect on and document key engineering lessons learned throughout the process.

## Description 


Detail design a bracket, using the concept design in Appendix B, to hold a horizontal force applied symmetrically by a strap outline in resource #1. The bracket’s dimensions are designed with different fit classes. Each dimension of the T beam is part of the fit:

“a” intention for use where accuracy is not essential

“b” is about the closest fits that can be expected to run freely

“c” is where accurate location and minimum play is desired

Design using a safety factor of 4 and applied load in between 500 lbf < F < 800 lbf. Choose one of three metals, aluminum 6061 T6, Steel (ASTM A36), or Titanium (Ti-6Al-V4). Furthermore, state assumptions and approximations about the design in order to use fundamental strength of materials analysis. For example, use the proper stress analysis and deflection analysis where appropriate. Assume no failure due to direct shear stress. 

Note: If the bracket is designed symmetrically a lot of work would be cut.

<img width="407" height="188" alt="Screenshot 2026-09-23 002413" src="https://github.com/user-attachments/assets/bf0e11ac-24a5-4646-9b57-4c26adbc87e2" />


## Design Specifications

Safety Factor (SF) = 4

Chosen Load (P) = 700 lbf

a = 0.498 in (+0.000in / -0.001)

b = 0.9992 in (+0.000 / -0.0005)

c = 1.499 in (+0.000 / -0.001)

Max Deflection = 0.005 in 

## Material

I decided to use Titanium (Ti-6Al-V4) for no real reason other than the fact that "titanium" sounds cool. Some important mechanical properties of this material are listed below.

Young's Modulus (E): 15,954,151.2 psi

Yield Strength (Sᵧ) = 120,091 psi

Allowable Strength (σ) = σᵧ/SF = 30,022.8 psi

Density = 0.160 lb/in^3 

Assume no failure due to direct shear stress

## Feature A

### Knowns / Assumptions

Treat like a cantilever beam (Appendix D)

L = 1.25 in (assumption based on the 0.75 in width of Uline Strap)

P = 700 lbf

### Unknowns 

Reaction Force (Ra)

Moment (Ma)

### Calculations 

<img width="244" height="302" alt="Screenshot 2026-09-23 203417" src="https://github.com/user-attachments/assets/36ee6938-5261-4448-bfd8-862bcfdc2301" />


I started with drawing the free body diagram of feature A and treated it like a cantilever beam. To convert the distributed load of P into a single load, I multiplied it by the assumed length and applied it to the midpoint. I then used this to find the reaction force in the y-direction. I assumed the reaction force in the x-direction to be zero since there are no other forces in that direction. Next, I calculated the moment by multiplying the single load P by half the length of feature A. 

After calculating the moment, I solved for the section moduli using the formula provided in Appendix A. From here, I plugged Z into the formula for diameter, which I found by multiplying the formula provided for radius in Appendix A by two. 

<img width="237" height="251" alt="Screenshot 2026-09-23 203428" src="https://github.com/user-attachments/assets/50c3471e-f305-4d66-801b-17c7008cebc1" />


First, I conducted a stress analysis for Feature A. I started by calculating the maximum stress. I then used this value to find the required section modulus. Since my required section modulus is less than the trial section modulus value I calulated earlier, I can safely proceed with the trial section modulus from before. Using that value, I calculated the radius of Feature A. 

I moved onto conducting a stiffness analysis. I started with the deflection formula and rearranged to find the moment of inertia, which I found by plugging in all the known values. Next, I rearranged the moment of inertia formula for a circular beam to find the radius. 

The radius calculated from the stress analysis and the radius calculated from the stiffness analysis are the same value, which means the design I've chosen is well-optimized. If they weren't the same, I would go with the greater radius value. 

## Feature B

### Knowns / Assumptions

Solid box beam

Treat like an axial loaded bar (Appendix D)

F = 875 lbf (Ra carried over from Feature A)

L = 0.5 in (assumption based on visual length of Feature B in Appendix C)

### Unknowns

Reaction Force (Rb)

Cross-Sectional Area (Ab)

Width (w)

Thickness (b)

### Calculations

insert feature B calculations here

I began by drawing the free body diagram for Feature B. Force (Fa) is essentially the reaction force (Ra) from my calculations from Feature A. Using this, I found the reaction force (Rb). I disregarded the reaction force in the x-direction because there are no forces in that direction. 

My next step was to find the cross-sectional area. I conducted a stress analysis using the allowable stress and Rb and found the minimum required cross-sectional area. I then conducted a stiffness analysis and plugged in the values I already know. I assumed the length based on how Feature B in Appendix C compared to Feature A. In the end, I found the cross-sectional area requirement from the stress analysis to be greater, so I went with that value. 

Lastly, I found the width and thickness of Feature B using the cross-sectional area. I assumed the beam to be a box beam, meaning its width and thickness are equal. 

## Feature C

### Knowns / Assumptions

Treat like a simply supported beam with a concentrated load at the center (Appendix D)

P = 875 lbf (Rb carried over from Feature B)

L = 1.5 in (assumption)

Thickness (b) = 1.0 in (assumption to match length with Feature A)

### Unknowns 

Reaction Forces (Rc1, Rc2)

Height (h)

### Calculations 

insert feature C calculations

First, I drew the free body diagram of Feature C. Force (Fb) is essentially the reaction force (Rb) from my calculations from Feature B. Since this is a simply supported beam, there are reaction forces (Rc1, Rc2) on both ends of the beam and they are equal to each other according to the Machinery's Handbook (pg 251). I used Fb to solve for the total reaction force (Rc), then divided in two to find the individual reaction forces. I disregarded any reaction forces in the x-direction since there are no applied forces in that direction.  

insert feature C calculations

I then conducted both stress and stiffness analyses to find the height. I obtained the stress and deflection formulas from the Machinery's Handbook, then rearranged to solve for Zreq and I, respectively. In the end, I found the height determined from the stiffness analysis to be greater than that of the stress analysis. 


## Lessons Learned

I spent a long time doing the stress analysis for Feature A because I didn't know the difference between the trial section modulus and the required section modulus. I also kept confusing myself when calculating for max stress. In the end, I figured out the difference. To my understanding, the required section modulus is the minimum value needed to withstand the max stress. Since my trial section modulus was greater than the required value, I was able to continue my calculations with that original trial section modulus value. 

[Titanium Mechanical Properties](https://www.azom.com/article.aspx?ArticleID=9299)
