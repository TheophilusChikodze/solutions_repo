# Problem 1
# Investigating the Range as a Function of the Angle of Projection


## Introduction and Motivation

Projectile motion is crucial in fields like sports, engineering, and defense. Understanding how launch angles affect range helps optimize performance in activities like basketball and javelin throwing, and informs designs in aerospace applications.

## Theoretical Foundation  

 Projectile motion follows Newton’s laws, with **horizontal motion** at constant velocity and **vertical motion** under gravity. The **range** depends on **initial velocity** and **angle of projection**, derived from kinematic equations.

 The key variables are: 
 
 * Initial velocity ($v0$)
 * Angle of projection ($θ$)
 * Gravitational acceleration ($g$)

The **range formula** is: 

$$R = \frac{v_0^2 \sin(2\theta)}{g}$$

## Range And Analysis
* Range is **maximized at 45°** in ideal conditions.

* Real-world factors like air resistance, gravity variations, and terrain require computational simulations for accuracy. 

* Higher velocity increases range, and lower gravity extends it, making this study crucial for sports, engineering, and aerospace applications.

## Practical Applications  

* Projectile motion is crucial in **sports**, where athletes optimize angles for maximum range (e.g., soccer, basketball, javelin).  

* In **military and defense**, accurate trajectory calculations improve targeting for artillery and missiles.  

* In **aerospace and engineering**, projectile principles guide rocket launches, spacecraft trajectories, and planetary landings, requiring computational simulations for precision.  



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
import numpy as np
import matplotlib.pyplot as plt

# Constants
g = 10  # Acceleration due to gravity (m/s²)
v0 = 20  # Initial velocity (m/s)

# Angle (45 degrees)
angle = 45
angle_rad = np.radians(angle)  # Convert to radians

# Time of flight calculation
t_flight = 2 * v0 * np.sin(angle_rad) / g

# Time intervals for the projectile motion
t = np.linspace(0, t_flight, num=100)

# Calculate x and y positions of the projectile
x = v0 * np.cos(angle_rad) * t
y = v0 * np.sin(angle_rad) * t - 0.5 * g * t**2

# Plot the trajectory
plt.figure(figsize=(8, 5))
plt.plot(x, y, label=f'Projectile at {angle}°', color="b")
plt.axhline(0, color="black",linewidth=1)  # Ground level
plt.axvline(x=max(x), linestyle="--", color="r", label=f"Range = {max(x):.2f} m")

# Labels and title
plt.xlabel("Distance (m)")
plt.ylabel("Height (m)")
plt.title(f"Projectile Motion at {angle}° with Initial Velocity {v0} m/s")
plt.legend()
plt.grid(True)
plt.show()
```
![alt text](image-2.png)

## Conclusion

This study demonstrates that the range of a projectile is significantly influenced by the launch angle, with **45°** yielding the maximum range under ideal conditions. By exploring projectile motion through theoretical calculations and visualizations, we gain valuable insights applicable to sports, engineering, and defense. While the model assumes ideal conditions, real-world factors such as air resistance and terrain can alter the trajectory. Future studies could expand on this by incorporating these factors for more accurate predictions.

## Source
[Colab Python Computation](https://colab.research.google.com/drive/1tRIRwlVz-um7t8zBhD_DcY86myED9WIK?usp=sharing)

