# A3 – [Parametric and FEA]

## Objective

The objective of this assingment is to design and test a bar given various constraints. The load on the bar must lie between 300 lbf and 500 lbf. The axial deflection must not exceed 0.009 inches. The value of Young's Modulus must lie between 8.5*10^6 psi and 11.5 x 10^6 psi.


## Parametric Design 

### Calculations

I began the design process by choosing the cross-sectional area and the force of the load on the beam. For the cross section, I decided to have an area of 0.5 in^2 and for the load, I went with 340 lbs. 

<img width="625" height="597" alt="Screenshot 2026-09-10 013534" src="https://github.com/user-attachments/assets/b0aa26b1-cf37-4ee0-81a0-bbdcc6d58c2f" />

At the top, I drew a diagram of what the beam looks like with the force, F, applied. I listed all the known variables and useful formulas for this project. The axial deformation value, e, was obtained through Creo Parametric and the equation for Young's Modulus was given in the Machinery's Handbook. 

<img width="621" height="275" alt="Screenshot 2026-09-10 013540" src="https://github.com/user-attachments/assets/567ba273-5c61-41a2-ae1d-39fc1b1609df" />

Using the known information, I calculated the diameter and length of the beam. I also listed the chosen force and area for reference. 

### Creo Parametric Design

<img width="528" height="486" alt="Screenshot 2026-09-10 003447" src="https://github.com/user-attachments/assets/db1483d1-fcb2-46e0-88d9-80e2bd71f1db" />

Next, I inputted the known and calculated information into the parameters tab in Creo Parametric, as shown above. After hitting ok and regenerating the model, Creo generated the beam shown below. 

<img width="479" height="286" alt="Screenshot 2026-09-10 005022" src="https://github.com/user-attachments/assets/eb287ba9-6ab3-405d-ac06-790d8f900d68" />

## FEA

### Deflection Map

My next task was to generate a deflection map in finite element analysis. To do this, I hit Simulate > Results > Home > Open. This opened up a new file for the deflection map, which I saved as A3_Deflection_Map. 

<img width="547" height="511" alt="Screenshot 2026-09-10 025331" src="https://github.com/user-attachments/assets/e8abf6e9-0f94-4e75-91ec-a2556d9c76fa" />

<img width="547" height="745" alt="Screenshot 2026-09-10 025353" src="https://github.com/user-attachments/assets/0d347f78-2cb5-4eb4-b532-d45aaa3a6ecc" />

I then modified the settings of the map as shown by the two images above and hit "Ok and Show," generating the image shown below. 

<img width="639" height="318" alt="Screenshot 2026-09-10 023648" src="https://github.com/user-attachments/assets/3629f9ef-93e7-4a37-84b4-124755f5dc65" />

My simulated deflection map is shown above. The red end of the beam signifies that it experiences the highest deflection. As the color changes to cooler colors, the beam experiences less and less deflection. 

### Von Mises Stress Curve

To generate the Von Mises stress curve, I followed the same steps as before when generating the deformation map, except I changed a few settings when saving the new file. From the deflection map page, I hit Home > Open. I saved the new file as A3_Von_Mises. 


<img width="550" height="507" alt="Screenshot 2026-09-10 032011" src="https://github.com/user-attachments/assets/b55a6c4d-5ba2-4db7-8c56-453abf5d778b" />
<img width="553" height="766" alt="Screenshot 2026-09-10 030353" src="https://github.com/user-attachments/assets/0090020f-8931-4987-bdbd-875e03651445" />

The settings I selected in the Results Window Definition tab for the Von Mises stress map are shown above. I then hit "Ok and Show," generating the image below. 

<img width="639" height="340" alt="Screenshot 2026-09-10 032117" src="https://github.com/user-attachments/assets/22dca560-1ab3-4144-9f28-e7a5b5bd27f6" />
<img width="639" height="340" alt="Screenshot 2026-09-10 032129" src="https://github.com/user-attachments/assets/be36c9bc-e56a-463b-824c-107d73a3bf93" />

The generated Von Mises stress curve is shown above. The first image shows the full length of the beam. Because of how zoomed out it is, I decided to include a close-up image of the constrained end of the beam. The cooler colors at the end indicate that there is lower stress in the area compared to the warmer shaded regions. 

According to the Von Mises stress curve, the maximum stress is 358 psi, which is significantly lower than 40 ksi strength of aluminum. To calculate the safety factor, I did: SF = failure strength / applied stress. Plugging in the numbers: 40,000 psi / 358 psi gives me a safety factor of 111.7. 

## Design Reflection

The axial deformation I calculated at the start was 0.009 inches and the axial deformation obtained through Creo Parametric is 0.0028 inches. The percent difference between these two is 105.1%. Looking back, I think the low amount of significant figures used in Creo Parametric might have contributed to this difference. When calculating it by hand, I don't round until the very end. This slight change might have compounded and resulted in the high percent difference seen above. Due to this, I'd trust my own hand calculations move since they use more significant figures during calculations. 

## Lessons Learned 

Unlike last time, I actually began this project a little earlier, though not as earlier as I'd like. This let me spend more time and effort on the process of this project, instead of just rushing to finish. Aside from time management skills, I learned a lot about how to simulate stresses and deformations in Creo Parametric, something I've never done before. In total, I spent around 7 hours on this project. 

[Download CAD File](https://drive.google.com/file/d/1nciBFJbLIHV3qH5qD0ySbsG3rDXLyJ4t/view?usp=drive_link)


