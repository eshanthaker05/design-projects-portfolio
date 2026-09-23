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

<img width="813" height="375" alt="Screenshot 2026-09-23 002413" src="https://github.com/user-attachments/assets/bf0e11ac-24a5-4646-9b57-4c26adbc87e2" />


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

insert feature A calcs here

I started with drawing the free body diagram of feature A and treated it like a cantilever beam. To convert the distributed load of P into a single load, I multiplied it by the assumed length and applied it to the midpoint. I then used this to find the reaction force in the y-direction. I assumed the reaction force in the x-direction to be zero since there are no other forces in that direction. Next, I calculated the moment by multiplying the single load P by half the length of feature A. 

After calculating the moment, I solved for the section moduli using the formula provided in Appendix A. From here, I plugged Z into the formula for diameter, which I found by multiplying the formula provided for radius in Appendix A by two. 

insert feature A stress + stiffness analysis here

Next, I conducted a stress analysis and stiffness analysis of Feature A. I started by calculating the max stress

## Resources 

[Titanium Mechanical Properties](https://www.azom.com/article.aspx?ArticleID=9299)
