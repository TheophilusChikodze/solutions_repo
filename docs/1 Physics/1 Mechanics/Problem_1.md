# Problem 1
# Investigating the Range as a Function of the Angle of Projection

## Theoretical Foundation  

 Projectile motion follows Newton’s laws, with **horizontal motion** at constant velocity and **vertical motion** under gravity. The **range** depends on **initial velocity** and **angle of projection**, derived from kinematic equations.

 The key variables are: 
 
 * Initial velocity ($v0$)
 * Angle of projection ($θ$)
 * Gravitational acceleration ($g$)



The **range formula** is: 

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$
\
It is **maximized at 45°** in ideal conditions. Real-world factors like air resistance, gravity variations, and terrain require computational simulations for accuracy. Higher velocity increases range, and lower gravity extends it, making this study crucial for sports, engineering, and aerospace applications.

## Practical Applications  

Projectile motion is crucial in **sports**, where athletes optimize angles for maximum range (e.g., soccer, basketball, javelin).  
In **military and defense**, accurate trajectory calculations improve targeting for artillery and missiles.  
In **aerospace and engineering**, projectile principles guide rocket launches, spacecraft trajectories, and planetary landings, requiring computational simulations for precision.  



## Calculating Range at Different Angles  

Using the **range formula**:  

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

Projectile range for angles **35°** and **45°**, with an initial velocity of **20 m/s** and gravity **\( g = 10 \) m/s²**.  

#### Example 1: **Angle = 35°**  

$$
R = \frac{20^2 \sin(70°)}{10}
$$

$$
R = \frac{400 \times 0.9397}{10}
$$

$$
R = \frac{375.88}{10} = 37.6 \text{ m}
$$

#### Example 2: **Angle = 45°** (Optimal Angle)  

$$
R = \frac{20^2 \sin(90°)}{10}
$$

$$
R = \frac{400 \times 1}{10}
$$

$$
R = \frac{400}{10} = 40 \text{ m}
$$

These results show that **45° gives the maximum range**, while **35° has a slightly shorter range**.


### Python script to compute and plot the range 

```python






