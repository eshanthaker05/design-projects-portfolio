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

To set up my FEA constraints, I hit Applications>Simulate>Home>Displacement. I selected the planes show below to constrain under the assumption that the artifact will be held up using a sliding hook. 

<img width="375" height="256" alt="Screenshot 2026-10-21 173211" src="https://github.com/user-attachments/assets/6a53468b-0cbc-4c6f-90de-a3480d071678" />

Next, I added the distributed force of 700 lbf onto Feature A. I hit Force/Moment and inputted the load onto Feature A, making sure to change units to lbf. I hit Ok and my resulting model can be seen in the image below. 

<img width="338" height="214" alt="Screenshot 2026-10-20 231912" src="https://github.com/user-attachments/assets/8a3ffa28-df22-4450-9bef-39f81a97b751" />

For the material, I hit Material Assignment>More(next to Materials)>Standard Materials>Nonferrous Metals>Ti-Al-V Alloy>Select. I am using the same material I used when originally modeling this bracket, as outlined in the instructions of this assingment.

## Design I

### Coarse Mesh

I set the max element size to 2.4 inches for the first mesh model as seen below. I wanted to create a mesh with bigger elements, but Creo was limiting my maximum element size to about 2.49 inches. I could not get around this for the life of me so I decided to use 2.4 inches for element sizes.

<img width="261" height="415" alt="Screenshot 2026-10-21 222407" src="https://github.com/user-attachments/assets/e0e8f641-01d4-48d8-b057-232966803113" />


To run the analysis, I hit Analyses and Studies>File>New Static>Green Flag>Yes. Once it was complete, I pulled up the results for the stress test and the deflection tests and marked the points at which the values were the highest. The values can be seen in the images below. 

<img width="378" height="263" alt="Screenshot 2026-10-21 192710" src="https://github.com/user-attachments/assets/e670d3cc-811a-4521-bf97-130f9e21d9a0" />

<img width="378" height="263" alt="Screenshot 2026-10-21 192814" src="https://github.com/user-attachments/assets/f9453681-ecf8-4b24-ab08-a48818efd9b8" />

Using the simulated maximum stress value and the known yield strength, I calculated the factor of safety to be 0.56. This is much lower than the required factor of safety value of 4 listed in the instructions of A5. I found the number of elements by hitting AutoGEM>Create as well as the mesh model as seen in the image below. 

<img width="314" height="153" alt="Screenshot 2026-10-21 191258" src="https://github.com/user-attachments/assets/93a3349f-9ee4-4c75-8674-dfa5d7c05ce5" />

The values found from this first mesh model are listed below: 

**Max Stress and Location:**	2.126 * 10^5 psi

**Max Deflection and Location:** 	6.315 * 10^-2 in 

**Mass:**	9.153 *10^-2 lb

**Safety Factor:** 	0.56

**Number of Elements:**	164

### Medium Mesh 

For the medium mesh model, the size of the elements was lowered from 2.4 inches to 1 inch to increase the total number of elements. 

<img width="375" height="412" alt="Screenshot 2026-10-21 200541" src="https://github.com/user-attachments/assets/30332963-8206-43ea-8de2-63ded0eea809" />

The steps listed above were repeated to obtain the stress and deflection models, which can be seen in the images below. The maximum values for each model are highlighted. 

<img width="378" height="263" alt="Screenshot 2026-10-21 202041" src="https://github.com/user-attachments/assets/66a74270-6cf2-4f3e-8bf5-875ec01f924a" />

<img width="378" height="263" alt="Screenshot 2026-10-21 202106" src="https://github.com/user-attachments/assets/ea3c56d6-145b-445d-b8b6-0746c7bb7a5b" />

Using the new simulated maximum stress value, the factor of safety was calculated to be 0.002. This value is significantly lower than factor of safety found in the first mesh model, making me skeptical about if I was doing this correctly. I repeated this step a few times and got the same value so I decided to continue with a third mesh model and compare all three values. The number of elements was found using the same steps listed in mesh model #1 and can be found below. For some reason, the number of elements went down, even though the element size was decreased. I decided to move onto the third mesh model because I had spent way too much time trying to fix this problem. 

<img width="443" height="226" alt="Screenshot 2026-10-21 222307" src="https://github.com/user-attachments/assets/df04c6b7-c5a9-47c0-8f4d-95e701f583ca" />

**Max Stress and Location:** 3.062 * 10^7 psi

**Max Deflection and Location:** 6.315 * 10^-2 in

**Mass:** 9.153 *10^-2 lb

**Safety Factor:** 0.002

**Number of Elements:** 159

 I then found the percent difference between these values and the values obtained with the coarse mesh using the following formula
 
 % Difference = (New-Old)/Old * 100

 The percent difference for the stress, deflection, and safety factor are listed below

 **Stress % Difference:** 14302.63%

 **Deflection % Difference:** 0%

 **Safety Factor % Difference:** -99.64%

 Looking at these, numbers, I don't really trust them so far the fine mesh model, I'll be comparing my new values to the original values found with the coarse mesh. 

### Fine Mesh 

For the fine mesh, the size of the elements was lowered from 1 inch to 0.1 inches as shown below. 

<img width="265" height="417" alt="Screenshot 2026-10-21 222751" src="https://github.com/user-attachments/assets/fcbcd227-9053-4d48-92d2-1e889728e546" />

When finding the number of elements this time, the number significantly increased as shown in the mesh model below. 

<img width="446" height="239" alt="Screenshot 2026-10-21 223018" src="https://github.com/user-attachments/assets/efd0b334-16eb-477c-bdae-c15ff2277b2d" />

I followed the same steps as above to obtain the stress and defelction models, which can be seen in the images below with their maximum values hightlighted. 

<img width="346.5" height="237.5" alt="Screenshot 2026-10-21 223243" src="https://github.com/user-attachments/assets/bc4a122d-5cce-4698-9b3d-514bcb0b948c" />

<img width="346.5" height="208.5" alt="Screenshot 2026-10-21 223258" src="https://github.com/user-attachments/assets/d5dd8a67-1949-48e8-bf77-7b340d99e15d" />

The new calculated factor of safety, along with the rest of the values obtained with the fine mesh are listed below. 

**Max Stress and Location:** 3.707 * 10^5 psi

**Max Deflection and Location:** 6.489 * 10^-2 in

**Mass:** 9.153 *10^-2 lb

**Safety Factor:** 0.32

**Number of Elements:** 7889

I then found the percent difference between these values and the values obtained from the coarse mesh, which are listed below. 

 **Stress % Difference:** 74.37%

 **Deflection % Difference:** 2.76%

 **Safety Factor % Difference:** -42.86%

 These values, especially the stress % difference, seem a lot more reliable to me. I decided to go with the fine mesh model values for my final Design 1 values. 

## Design II

When changing the geometry, the goal was to minimize the stress, deflection, and mass on the bracket. Keeping that in mind, I reduced the length of Feature A by 0.5 inches. In the stress models from Design I, the most amount of stress was experienced on Feature B, so by minimizing the length of Feature A, the moment on Feature B would decrease, resulting in lower stresses. The new geometry of the bracket is shown below. 

<img width="390" height="272.5" alt="Screenshot 2026-10-21 232035" src="https://github.com/user-attachments/assets/344d7681-2b70-404b-84f2-f68c92a23198" />

The total mass of the bracket decreased to 7.36 * 10^-2 lbs since the volume of Feature A was reduced. 

### Coarse Mesh 

Originally, I wanted to use the same element size that I used in Design I for all my mesh models. However, Creo limited my maximum element size to under 2.28 inches this time. I do not know why it keeps restricting me using seemingly random numbers. All my attempts to get around this have not worked. I decided to use an element size of 2.2 inches for this mesh model as seen below. 

<img width="266" height="412" alt="Screenshot 2026-10-21 233117" src="https://github.com/user-attachments/assets/86658abf-b073-4c3e-9bce-ca0253ad144f" />

Using this element size, I obtained the number of elements, as shown below. 

<img width="412" height="221" alt="Screenshot 2026-10-21 233247" src="https://github.com/user-attachments/assets/f8b26728-98a0-4b1f-a4e7-356f54e18a58" />

Next, I obtained the maximum stress and deflection values by following the same procedure as before as shown in the images below. 

<img width="350.5" height="220" alt="Screenshot 2026-10-21 233517" src="https://github.com/user-attachments/assets/70b0600b-11fd-4c1f-acf4-1e36e1d9624c" />

<img width="379" height="250" alt="Screenshot 2026-10-21 233547" src="https://github.com/user-attachments/assets/f026104a-5344-428e-b59e-ebc796e484d1" />

The values obtained from this coarse mesh model are listed below, including the factor of safety calculated from the simulated maximum stress value. 

**Max Stress and Location (psi):**	126300

**Max Deflection and Location (in):** 0.02325

**Mass (lb):** 0.0736

**Safety Factor:** 	0.951

**Number of Elements:**	156

### Medium Mesh 

To create the medium mesh model, I set the element size to 1.3 inches as seen below because I wanted the difference between element sizes between coarse and medium meshes to remain the same between Design I and Design II. 

<img width="270" height="411" alt="Screenshot 2026-10-21 234738" src="https://github.com/user-attachments/assets/570ff155-3f5e-41b9-989d-b06bb1b0411d" />

I then found the number of elements as shown below. Somehow, the number of elements is lower when the element size decreases as displayed in Design I. I'm pretty sure I'm making a mistake somehow, somewhere but when I repeat the exact same procedure for the fine mesh, everything seems fine so I'm entirely sure where I'm messing up.

<img width="396" height="219" alt="Screenshot 2026-10-21 234908" src="https://github.com/user-attachments/assets/4602811b-9c79-4bb5-8a21-9689e76ddaae" />

Moving onto the stress and deflection models, I obtained them the same way I've been obtaining them throughout this assingment and can be seen in the images below. 

<img width="366" height="223.5" alt="Screenshot 2026-10-21 235030" src="https://github.com/user-attachments/assets/27e11931-074c-42bd-8f87-3a62d12adcfc" />

<img width="317.5" height="211.5" alt="Screenshot 2026-10-21 235042" src="https://github.com/user-attachments/assets/475de149-4fb1-441d-9833-cf82bebd27e9" />

The values obtained from this coarse mesh model are listed below, including the factor of safety calculated from the simulated maximum stress value. 

**Max Stress and Location (psi):** 121200

**Max Deflection and Location (in):** 0.02365

**Mass (lb):** 0.0736

**Safety Factor:** 0.099

**Number of Elements:** 143

I then found the percent difference between these values and the values obtained from the coarse mesh, which are listed below. 

**Stress % Difference:** -4.04%

**Deflection % Difference:** 1.72%

**Safety Factor % Difference:** 4.21%

Since the percent difference between my values from the coarse mesh and the medium mesh are within 7% of each other, the stress, deflection, and safety factor are converging and I don't need to conduct a fine mesh analysis. 

## Design III

For my third and final design, I decided to double the length and half the height of Feature B. Before this modification, the width, length, and height of Feature B were 0.53 in, 0.170 in, and 0.500 in, respectively. After the modification, the new the width, length, and height of Feature B are 0.53 in, 0.300 in, and 0.250 in, respectively. By doing this, I am able to reduce the volume of Feature B from 0.0451 in^3 to 0.0398 in^3 while halving the height. This will lower the overall mass of the bracket while strengthening Feature B. The modified bracket is shown below. 

<img width="388.5" height="268.5" alt="Screenshot 2026-10-22 001922" src="https://github.com/user-attachments/assets/8c657298-8c43-4315-a76c-4c988ae3c403" />

### Coarse Mesh 

As expected, the maximum element size allowed by Creo has decreased. For this mesh analysis, I set the element size to 2.1 inches as shown below. 

<img width="265" height="412" alt="Screenshot 2026-10-22 002052" src="https://github.com/user-attachments/assets/e637fe79-8e3d-49b3-bd79-c53b3f7839b2" />

Using this, I found the number of elements, as seen in the image below. 

<img width="445.5" height="224" alt="Screenshot 2026-10-22 002121" src="https://github.com/user-attachments/assets/715b9a0e-032e-456d-bdb7-5d76f44eb35f" />

Next, I obtained the stress and deflection models with their maximum values highlighted, as shown in the images below. 

<img width="276" height="180.5" alt="Screenshot 2026-10-22 002224" src="https://github.com/user-attachments/assets/03af1ed6-b4db-4a74-9162-87139b606fc9" />

<img width="307.5" height="210.5" alt="Screenshot 2026-10-22 002237" src="https://github.com/user-attachments/assets/383b9b77-1039-425e-a727-5bd8a17008ff" />

The values obtained from this coarse mesh model are listed below, including the factor of safety calculated from the simulated maximum stress value. 

**Max Stress and Location (psi):** 40420

**Max Deflection and Location (in):** 0.0029

**Mass (lb):** 0.0704

**Safety Factor:** 2.97

**Number of Elements:** 147

As seen by these values, the stress, deflection, and mass have all decreased compared to Design II. Also, the factor of safety has risen significantly. 

### Medium Mesh 

This time, I decided to reduce my element size to 0.5 inches, as shown below. 

<img width="267" height="413" alt="Screenshot 2026-10-22 004156" src="https://github.com/user-attachments/assets/6e21bd84-3a23-4d6b-a443-4c6cced13065" />

For once, this resulted in a greater number of elements in the modeled mesh, as seen in the image below. 

<img width="425.5" height="233" alt="Screenshot 2026-10-22 004211" src="https://github.com/user-attachments/assets/730fb0b8-c936-4641-8cb9-f740a8da71a6" />

Next, I moved onto the stress and deflection models and highlighted their maximum values which can be seen in the images below. 

<img width="357.5" height="226" alt="Screenshot 2026-10-22 004300" src="https://github.com/user-attachments/assets/800e29ae-c0e0-4caa-80e0-2c9e1fd796c5" />

<img width="214" height="250.5" alt="Screenshot 2026-10-22 004310" src="https://github.com/user-attachments/assets/6b43df4c-a56a-43a0-8d13-6ef09342f75e" />

The values obtained from this medium mesh model are listed below, including the factor of safety calculated from the simulated maximum stress value. 

**Max Stress and Location (psi):** 42070

**Max Deflection and Location (in):** 0.003037

**Mass (lb):** 0.0704

**Safety Factor:** 2.85

**Number of Elements:** 193

The stress has decreased while the deflection has slightly increased. I then found the percent difference between these values and the values obtained from the coarse mesh, which are listed below. 

**Stress % Difference:** 4.08%

**Deflection % Difference:** 1.39%

**Safety Factor % Difference:** -3.92%

Since the percent difference between my values from the coarse mesh and the medium mesh are within 7% of each other, the stress, deflection, and safety factor are converging and I don't need to conduct a fine mesh analysis. 

## Reflections 




