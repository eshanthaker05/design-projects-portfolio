# A2 – Truss Stress Analysis

## Objective

The objective of this assignment is to design a truss that fit the given constraints shown below. The truss must be designed using some type of steel, preferably A500 structural steel. 

<img width="370" height="175" alt="Screenshot 2026-09-02 144933" src="https://github.com/user-attachments/assets/ef21e821-9657-4817-89ff-2809dba25799" />

## Truss Geometry 

<img width="522" height="274" alt="unnamed" src="https://github.com/user-attachments/assets/03cd8669-b8a9-4eec-ada2-a3ec03503f68" />


I decided to go with the geometry shown above. I added joint E at the midpoint between Joints A and B, then connected them to Joint C and D. Joint A is a pin connection and Joint B is roller pin. The lengths of "a" and "b" are given to the right and P = 21 kN. 

<img width="375" height="303" alt="unnamed (2)" src="https://github.com/user-attachments/assets/533ba4f5-4def-4b35-b043-a0097ef94c1a" />

I calculated the lengths of each member in the image above. I also found the angles between CDE and DA and denoted them theta 1 and theta 2, respectively. I've listed the lengths on the right. 

## External Forces

<img width="338" height="391" alt="unnamed (3)" src="https://github.com/user-attachments/assets/75e67096-ecb4-47bb-9a38-49fdc90ea873" />

Next, I drew a free body diagram of the external forces, consisting of the forces at Points A and B and load P at Points C and D. Using this information, I calculated the values of By, Ay, and Ax. 

## Internal Forces 

<img width="301" height="430" alt="IMG_2951" src="https://github.com/user-attachments/assets/ba21445e-7daf-4813-9595-814f3d41f402" />
<img width="294" height="464" alt="IMG_2953" src="https://github.com/user-attachments/assets/d947d113-310b-4326-b9f2-718dc9beb2d6" />

Using the external force values, I calculated the internal forces. Using the method of joints, I found the internal forces of each point, starting from Point A and ending on Point C. I drew a free body diagram for each point and assumed each member was in tension at first. If its calculated value was negative, that just meant that the member was in compression, and I changed the free body diagram of the point accordingly. I've listed the internal forces on each member at the end as well as if they're in tension or compression. 

## Cross-Sectional Area and Weight

<img width="385" height="312" alt="unnamed (4)" src="https://github.com/user-attachments/assets/c2a3b67c-e1b2-4682-b91b-eb4430439bc9" />

Next, I calculated the cross-sectional area of the members of the truss. I listed the relevent known information at the top of the page. The work below is sectioned off by numbers to keep it organized and easy to read. In section 1, I convert the values for the internal force and the minimum yield strength into compatible units. I didn't know where to go from here, but after reading the listed pages from the textbook, I realized I could rearrange the stress equation to solve for the cross-sectional area. In section 2, I rearranged the formula and plugged in the values from section 1. In section 3, I converted the units of the area from m^2 to mm^2. Lastly, in section 4, I applied the safety factor of 3.5 to obtain a final cross-sectional area of 207.56 mm^2. 

<img width="520" height="284" alt="IMG_2955" src="https://github.com/user-attachments/assets/2b875a98-f677-4aa9-b35b-fa2ad87fa3a3" />
<img width="278" height="277" alt="IMG_2956" src="https://github.com/user-attachments/assets/c52f73ed-e605-45f5-b2ae-1d4f673f8557" />

To calculate the weight, I first listed the lengths of each member. Then, I multiplied each length by the cross-sectional area, taking into account the safety factor of 3.5, and found the volume in m^3. Lastly, I multiplied the volume by the density of A500 Steel to find the weights of each member. Adding these values up gave me the total weight of the truss in kg. 

## Pin Structure

<img width="309" height="384" alt="unnamed (5)" src="https://github.com/user-attachments/assets/07bf382b-4caf-4fdb-8f5d-304954b39c82" />

Next, I found the cross-sectional area of each pin using pin C. I used pin C specifically because it carries the biggest load of 7kN. The given information is listed at the top of this image. Again, I split my work into sections to stay organized. In section 1, I converted the values into proper units. In section 2, I used the formula found in the textbook, just like how I found the cross-sectional area for the members, to find the area of the pins. 

## Lessons Learned

-  I did not realize how much planning goes into the design process. For this project, the majority of my time was spent planning and calculating the truss instead of CAD modeling.
-  One of my main takeaways from this project is how to efficiently manage my time. This project was an eye-opener for me because I started it a few days before the deadline, which is a pretty early start for me at least, and I still did not manage to fully complete it. In total, I spent around 10 to 11 hours working on this and was unable to meet every requirement. In the future, I will take time management more seriously to avoid running into this problem again.
-  I learned how to meticulously document every step of the design process, even though it can be tedious at times. It's important because it lets others know your exact thought process throughout the project. In fact, there was a few times when I took a break from working on this assignment, only to come back and forget what I was doing. By going through my documentation, I was able to jog my memory and resume where I left off. 
