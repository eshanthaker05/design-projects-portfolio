# A11 – Motor Selection Design

## Group : Brendan Spinner, Eshan Thaker, Noel Negron

## Motor Selection & Attachments - Brendan

### Picking the Motor 

For the first analysis, I was to calculate for all relevant motor parameters and choose a motor that fits within my calculations. 

<img width="3024" height="4032" alt="IMG_3428" src="https://github.com/user-attachments/assets/3bf87b67-931d-490b-871a-c71056cb26d3" />

The minimum calculated raising torque per leadscrew was found to be 1.30 N * m. To give each leadscrew some tolerance for any friction influence, I increased the minimum torque per leadscrew to about 1.43 N * m. Based off of these specifications, I chose the NEMA 23 Bipolar Stepper with a 10:1 Planetary Gearbox. The specific parameters of this motor are listed above. The speed-torque curve reveals the full operating margin of the motor at specific RPMs based off of a specific torque value.

### Motor Mount Bracket & Housing

For this next analysis section I calculated for dimensions that will be sufficient for the motor selected above.

<img width="3024" height="4032" alt="IMG_3429" src="https://github.com/user-attachments/assets/d0a79118-e02d-44b3-813b-ea6625d186f5" />

For the bracket, I used a machined 6061-T6 Aluminum U-channel / standoff motor mount bracket bolted directly to the top T-slot frame plate using a 4-hole M6 bolt pattern. The shear force per bolt from motor torque was calculated to be 10.21 N, the bearing stress on the bolt wall is 68.75 MPa, and the minimum thickness was found to be 0.025 mm.

### Selecting a Coupler

For this next section, I was to design a rigid/clamping hollow cylindrical shaft coupler machined from 6061-T6 Aluminum. 

<img width="3024" height="4032" alt="IMG_3430" src="https://github.com/user-attachments/assets/42c5ebf6-9f96-40e1-bfaf-16fac69dcd9d" />

Given the calculated values, the minimum outer diameter that would serve as a sufficient is 12.46 mm. However, to make the dimension well within the safety factor range, choosing an outer diameter closer to 25mm would be much safer.

## Analyze & Design a Frame - Brendan & Eshan

### Bracket to Affix Standoffs - Brendan

This section required me to analyze and construct an optimal bracket that would connect the vertical standoffs of the frame to the very top of the frame.

<img width="3024" height="4032" alt="IMG_3431" src="https://github.com/user-attachments/assets/41d98505-9bf2-42a2-86e4-7be7d3483450" />

The chosen T-slot extruded columns we chose were the 80/20 15-Series McMaster 47065T418. The numerical joint load per column was calculated to be 1000.7 N. The safety factor of the connector was also well within its safety range at about 35 times the failure value.

### Analyzing the top of the frame - Eshan

For the T-slotted frame, we went with the 5537T102 frame since it has a height and width of 40 mm and has a material strong enough to withstand the loads calculated in the previous sections. We defined the boundaries to be the two opposing sides of the frame, since that’s where it will be attached to the tensile tester. We added two 1000 kN loads onto where the leadscrew attaches and added the moments on either side. 

With the constraints set, we ran an FEA analysis and obtained the Von Mises below. We can see that the highest stress value is 1.87 Mpa and the lowest stress value is 0.24 Mpa. Our material is strong enough to withstand this stress. One possible way we can optimize this design is by increasing the thickness of the outer edges of the imported frame since that’s where the majority of the stress is concentrated. 

<img width="522" height="262" alt="Screenshot 2026-11-19 025426" src="https://github.com/user-attachments/assets/c3ec7518-c2f9-4533-8bab-ce97d4c9e3d1" />

### Analyzing the vertical components of the frame - Eshan

For the vertical components, we followed the same steps as we did for the top of the frame. In the image below, you can see the Von Mises in which the highest stress value is 40.93 MPa and the lowest stress value is 0.024 MPa. One possible way we can optimize this is by adding further support on the end with the higher load to reduce the overall stress. 

<img width="520" height="282" alt="Screenshot 2026-11-19 031143" src="https://github.com/user-attachments/assets/3199483e-3eff-4628-b08d-19e4cfe5f739" />



## Designing Floating Bearing Mount - Noel

<img width="1179" height="2096" alt="8A695E43-5FBF-46FA-91A7-42DF4508AF4C" src="https://github.com/user-attachments/assets/5cae38e0-7d42-40e6-8e6c-91b95ceaba11" />

<img width="1179" height="2096" alt="99AD6301-5A93-4CDA-AEFA-FD1B0338CCFB" src="https://github.com/user-attachments/assets/54668c74-e950-4a9e-af9f-59c56eb835a6" />

Creating the floating bearing mount was a little confusing at first, as there were little to no instructions on how it was supposed to be done. With the reference of the bearing mount in the appendix, I created a bearing that matched the first frame design as well as I could get it to match, while defining each dimension and justifying why it must be there for the entire assembly. I chose a RC3 fit with a 0.40-0.71 inch range for the major diameter (0.500”) of the ½”-10 ACME lead screw. The material I chose for the floating bearing mount was 6061-T6 aluminum; same as the other frame.

## Bills of Material & Labor Costs - Noel

<img width="550" height="850" alt="Screenshot 2026-11-19 005201" src="https://github.com/user-attachments/assets/2db74311-f210-4c47-8eea-4432073c1b68" />

The bill of materials was not very difficult to craft, as there were general sizes of aluminum of each respective part that fits the specified dimensions of each part. The screw and M6 bolts were easy to find as well, and there was an exact T-slot on McMaster that was ideal for our assembly.

## Lessons Learned - Noel

Overall, this two-part assignment taught us the importance of tolerances, materials, and fits throughout the different phases of the assignments. Finding the right lead screw for our motor, and identifying the specific dimensions of the mounts, and analysing each part emphasized the importance of accuracy and precision when it comes to an assembly, as if one part is off, then the entire assembly will not fit together. Throughout this assignment, we prioritized teamwork and communication as we delegated different parts of each assignment to one another and trusted them to do it right and be responsible for their own work. This assignment took around 10 hours between all of us to complete.
