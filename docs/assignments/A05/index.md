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

Length (L) = 1.25 in (assumption based on the 0.75 in width of Uline Strap)

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

Fb = 875 lbf (Ra carried over from Feature A)

Length (L) = 0.5 in (assumption based on visual length of Feature B in Appendix C)

### Unknowns

Reaction Force (Rb)

Cross-Sectional Area (Ab)

Width (w)

Thickness (b)

### Calculations

<img width="249" height="287" alt="Screenshot 2026-09-24 041055" src="https://github.com/user-attachments/assets/1e49d71e-1469-4825-915e-ae5de6a9bd17" />

I began by drawing the free body diagram for Feature B. Force (Fa) is essentially the reaction force (Ra) from my calculations from Feature A. Using this, I found the reaction force (Rb). I disregarded the reaction force in the x-direction because there are no forces in that direction. 

My next step was to find the cross-sectional area. I conducted a stress analysis using the allowable stress and Rb and found the minimum required cross-sectional area. I then conducted a stiffness analysis and plugged in the values I already know. I assumed the length based on how Feature B in Appendix C compared to Feature A. In the end, I found the cross-sectional area requirement from the stress analysis to be greater, so I went with that value. 

Lastly, I found the width and thickness of Feature B using the cross-sectional area. I assumed the beam to be a box beam, meaning its width and thickness are equal. 

## Feature C

### Knowns / Assumptions

Treat like a simply supported beam with a concentrated load at the center (Appendix D)

Fc = 875 lbf (Rb carried over from Feature B)

Length (L) = 1.5 in (assumption)

Width (w) = 1.0 in (assumption to match length with Feature A)

### Unknowns 

Reaction Forces (Rc1, Rc2)

Height (h)

### Calculations 

<img width="249" height="290" alt="Screenshot 2026-09-24 041102" src="https://github.com/user-attachments/assets/fe1513bf-c15a-45d4-9440-f18a1cf352a0" />

First, I drew the free body diagram of Feature C. Force (Fb) is essentially the reaction force (Rb) from my calculations from Feature B. Since this is a simply supported beam, there are reaction forces (Rc1, Rc2) on both ends of the beam and they are equal to each other according to the Machinery's Handbook (pg 251). I used Fb to solve for the total reaction force (Rc), then divided in two to find the individual reaction forces. I disregarded any reaction forces in the x-direction since there are no applied forces in that direction.  

insert feature C calculations

I then conducted both stress and stiffness analyses to find the height. I obtained the stress and deflection formulas from the Machinery's Handbook, then rearranged to solve for Zreq and I, respectively. In the end, I found the height determined from the stiffness analysis to be greater than that of the stress analysis. 

## Feature D

### Knowns / Assumptions

Solid box beam (assumed based on Appendix C)

Load from Feature C reaction force is centered

Fd = 437.5 lbf (Rc2 carried over from Feature C

Length (L) = 1.5 in (assumed to match Feature C)

Width (w) = 1.0 in (assumed to match Feature C)

### Unknowns

Height (h)

### Calculations 

<img width="248" height="291" alt="Screenshot 2026-09-24 041110" src="https://github.com/user-attachments/assets/84d18130-10c6-4c68-aabd-6cfe073bd1f2" />

I started by drawing the free body diagram and solving for the reaction force. Next, I conducted a stress analysis and found the required height. Then, I conducted a stiffness analysis and solved for the cross-sectional area. Using this value, I solved for the required height. The height obtained from the stress analysis is greater, so I went with that one. 

## Feature E

### Knowns / Assumptions 

Rectangular cantilever beam

Length (L) = 1.5 in (assumed to match Feature D)

Width (w) = 0.5 in (assumed based on visual width in Appendix C)

Fe = 437.5 lbf (Fd carried over from Feature D)

### Unknowns 

Height (h)

### Calculations

<img width="245" height="290" alt="Screenshot 2026-09-24 041124" src="https://github.com/user-attachments/assets/e5c5c36c-78f3-40f0-a738-ca59b4f0be36" />

I started by drawing the free body diagram and solving for Fe. Next, I conducted the stress and stiffness analyses and found that the height obtained from the stress analysis is greater than the one from the stiffness analysis. 

## Multiview Sketches

### Stress 

insert here

### Stiffness

insert here

## Lessons Learned

I spent a long time doing the stress analysis for Feature A because I didn't know the difference between the trial section modulus and the required section modulus. I also kept confusing myself when calculating for max stress. In the end, I figured out the difference. To my understanding, the required section modulus is the minimum value needed to withstand the max stress. Since my trial section modulus was greater than the required value, I was able to continue my calculations with that original trial section modulus value. 

By the time I finished calculations for Feature C, I had a pretty decent understanding on stress and stiffness analyses and how they can be used to find the dimensions of a beam, depending on the beam type. Also, I realized that I did a bunch of unnecessary steps in Feature A, further confusing me. 

### Governing Failure Mode

For Feature A, the radius obtained from stress and stiffness are practically the same. This means that the dimensions for this feature work very well given the maximum deflection and the mechanical properties of the material. 

### Error Propagation

During feature C, I noticed that I had miscalculated a few values during Feature B, resulting in my numbers to be slightly off. I recalculated them and continued working. 

### Assumption

I assumed the length of Feature A to be 1.25 inches. This assumption had an effect on the dimensions of every feature afterwards. If this length was a different value or if it is incorrect, the dimensions of all the other features would need to be adjusted. 

In total, I spent around 10 hours on this assignment. 


[Titanium Mechanical Properties](https://www.azom.com/article.aspx?ArticleID=9299)
