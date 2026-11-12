# A10 – Lead Screw Translating System

## Objective

- Develop a lead-screw–driven crosshead 

- Ensure accurate, repeatable load application to 2 kN with minimal crosshead deflection and misalignment.

- Provide robust specimen gripping, simple calibration provisions (mechanical), and safe, ergonomic operation.

## Leadscrew: Brendan

To find the correct leadscrew, we needed to calculate the minimum diameter, rotational speed, and maximum torque. The calculations for this are shown below. 

<img width="378" height="504" alt="IMG_3366" src="https://github.com/user-attachments/assets/175b7396-303a-4b1c-ab2b-8d467f5ddf40" />

<img width="378" height="504" alt="IMG_3367" src="https://github.com/user-attachments/assets/ce14503d-3d4c-45e9-8956-33158416f0ae" />


## Nut and Flange: Eshan 

To find the correct nut flange, we analyzed the inner forces and calculated the allowable stress. Listed below are our calculations. 

<img width="379" height="486" alt="IMG_0020" src="https://github.com/user-attachments/assets/947a959d-6d54-4f62-b454-551e11e70bf0" />

## Crosshead: Eshan

To find a crosshead, we first ran a stress analysis and calculated a height value. Next, we ran a deflection analysis and found another height value. The greate value of the two is the true height of the crosshead since it can withstand the necessary forces. Lastly, we created a multiview sketch of the crosshead. 

<img width="377" height="488" alt="IMG_0021" src="https://github.com/user-attachments/assets/e4ff455c-7a36-4983-ae98-d107e5b54f26" />

<img width="375" height="473" alt="IMG_0022" src="https://github.com/user-attachments/assets/f2710334-a16d-47e2-a5bd-02eebd2613c9" />

<img width="380" height="490" alt="IMG_0023" src="https://github.com/user-attachments/assets/25e9d038-5bc0-46f0-b1f1-9e79fc4d4b26" />

## Tabulating Costs: Eshan

| Item number | Quantity | Name | Cost per Item | Total Cost | Purchase Link |
|-------|-------|-------|-------|-------|-------|
|   1    |    2    |Leadscrew    |14.48  |28.96           |[94330A110](https://www.mcmaster.com/94330A110/)|
|   2    |    2    |Flange Nut   |178.60  |357.20          |[97790A110](https://www.mcmaster.com/97790A110/)|
|   3    |    4    |Frame        |10.82  |43.28           |[47065T107](https://www.mcmaster.com/47065T107-47065T418/)|
|   4    |    8    |Mount Bolt   |0.49   |24.47 (50 pack) |[92196A537](https://www.mcmaster.com/92196A537/)|
|   5    |    8    |Mount Nut    |0.08   |8.28 (100 pack) |[94895A110](https://www.mcmaster.com/94895A110/)|
|        |         |             |          |$462.19          |                                  |

## Parametric Modeling: Brendan

### Crosshead design

The only part we had to build ourselves in this project was the crosshead. The crosshead serves as the main bracket that holds the lead screw in place. 

I began the design by parametrically modeling some dimensions;

<img width="767" height="137" alt="Screenshot 2026-11-11 214932" src="https://github.com/user-attachments/assets/983b197c-b1d4-4ec7-a058-73497944dd22" />

Utilizing these dimensions, I began the base geometry of the crosshead.

<img width="401" height="216" alt="Screenshot 2026-11-11 215159" src="https://github.com/user-attachments/assets/d2333ccf-12bf-4d33-aa52-65e1307b613c" />

<img width="386" height="466" alt="Screenshot 2026-11-11 215646" src="https://github.com/user-attachments/assets/61fa223c-5ff2-426b-992c-2587c14fdec7" />

I assigned the material of Aluminum 6061-T6 to the crosshead as we calculated for. The two main bore holes seen above are the holes in which the lead screws would go through in our final assembly.

### Editing the Flange Nut

After carefully analyzing the flange nut we found, I noticed there were not screw holes found anywhere that will affix the flange nut to the crosshead itself. This meant that I was forced to make some screw holes on the flange nut I downloaded.

<img width="461" height="350" alt="Screenshot 2026-11-11 225401" src="https://github.com/user-attachments/assets/e5cd370c-887a-40dc-8978-abf97b1bcd92" />

<img width="408" height="313" alt="Screenshot 2026-11-11 231632" src="https://github.com/user-attachments/assets/83d724ca-37a6-4136-85c9-4ad9cb5f6142" />

I utilized a 45 degree angle of spacing for the screw holes rather than at a typical 90 degree angle to account for the fact that the flange has flat machined edges on two sides. I implemented a standard to ANSI Inch #10-24 clearance holes.

<img width="421" height="342" alt="Screenshot 2026-11-11 234510" src="https://github.com/user-attachments/assets/e6bd9c3a-588e-450b-9147-d0c3522c73d6" />

### Back to Crosshead Design

I utilized the same tactic with creating the four screw holes on the flange nut as on the crosshead. I drew a construction circle around the already extruded cut, and spaced out the four circles at 90 degree angles from one another, starting at a typical 45 degree angle.

<img width="384" height="157" alt="Screenshot 2026-11-11 232954" src="https://github.com/user-attachments/assets/b243c195-9249-482f-bf75-2be319051ae4" />

<img width="371" height="151" alt="Screenshot 2026-11-11 233606" src="https://github.com/user-attachments/assets/3c2a9625-59ba-44eb-a209-13bbd58100e9" />

I mirrored across a center plane so that the holes were identical around both bores.

<img width="547" height="302" alt="Screenshot 2026-11-11 233938" src="https://github.com/user-attachments/assets/d39ff6ef-b539-4454-b193-c8d55bc1c6bb" />

### Importing downloaded files

I went to the attached links and made a separate file for each given part;

<img width="421" height="342" alt="Screenshot 2026-11-11 234510" src="https://github.com/user-attachments/assets/db49250d-2680-4a65-af9d-ac2fe0b952fe" />

<img width="423" height="384" alt="Screenshot 2026-11-11 234527" src="https://github.com/user-attachments/assets/f84925e6-8706-4092-8351-1465ffdcc843" />

<img width="321" height="386" alt="Screenshot 2026-11-11 234544" src="https://github.com/user-attachments/assets/bcff175e-1982-4df1-9a2a-c606882e6a75" />

<img width="331" height="386" alt="Screenshot 2026-11-11 234705" src="https://github.com/user-attachments/assets/182b6e0e-8420-4daf-943b-a7c2b0580b4c" />

<img width="471" height="351" alt="Screenshot 2026-11-11 234715" src="https://github.com/user-attachments/assets/d99ce6ef-d66f-453a-8098-d5b2c864cfce" />

### Assembling pieces together

The final step was to take all the downloaded and designed parts and assemble them into an incomplete lead screw mechanism. I was prompted to use 8 of the screws, one nut, one of the T-frames, our design crosshead, 2 leadscrews, and 2 of the flange nuts.

<img width="422" height="321" alt="Screenshot 2026-11-11 235415" src="https://github.com/user-attachments/assets/dd7215b2-1874-4cd9-bcce-2cc58e89be0f" />

<img width="469" height="298" alt="Screenshot 2026-11-11 235814" src="https://github.com/user-attachments/assets/a038e563-393b-4cf8-9ff8-74303f6dc903" />

I then started to mate the parts together similar to the example image:

<img width="464" height="393" alt="Screenshot 2026-11-12 000633" src="https://github.com/user-attachments/assets/38a7268e-ace6-4be4-bb79-a9af3b3befbe" />

<img width="456" height="379" alt="Screenshot 2026-11-12 001127" src="https://github.com/user-attachments/assets/f3bfb14e-eb75-4c94-a7f6-d588c3c419c3" />

<img width="351" height="369" alt="Screenshot 2026-11-12 002423" src="https://github.com/user-attachments/assets/81d62873-6302-40e8-9f46-dd32d81af730" />

<img width="400" height="370" alt="Screenshot 2026-11-12 004429" src="https://github.com/user-attachments/assets/4e9af0ab-4a4b-4387-9765-bae0752583e6" />

This lead screw setup is incomplete as it is missing some key components for a practical application. However, given the setup and parts we were instructed to use, this is the best assembly I could arrange. For a safety check, I validated that there were no interfering parts within my assembly:

<img width="251" height="408" alt="Screenshot 2026-11-12 004636" src="https://github.com/user-attachments/assets/09489e8b-7f01-4979-8aa0-8178b46ed3e8" />

## Lessons Learned 

In this assignment, we learned how to use multiple analysis methods to find an appropriate value, such as when we found the height of the crosshead. We also learned how to convert linear speed into rotational speed, and then use that to find the torque of an object.

[Frame](https://drive.google.com/file/d/14XVI5ntT0tfzCydKs530lmVxSxqJgEG4/view?usp=drive_link)

[Head Screw](https://drive.google.com/file/d/1vg9_WwzWNuM6-6GrR3DbrcCxveKbjZ0h/view?usp=drive_link)

[Lead Screw](https://drive.google.com/file/d/1xgFifHAhNzByHLya4EZVP99iGBfSN8f8/view?usp=drive_link)

[Nut](https://drive.google.com/file/d/1PCONorYVgFMwPnoFBVAn4ZsiIRcxUvXt/view?usp=drive_link)

[Lead Screw Assembly](https://drive.google.com/file/d/1z4NWNmupRmRS37gG9rCgUP_-69lqLKnU/view?usp=drive_link)


