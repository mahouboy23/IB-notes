---
tags : mod Physique
---
Created: 2025-10-03

# Chapter 1: Units, Measurements & Vectors
## 1.1 What is Physics
- **Physics**: Science of matter, energy, and their interactions.  
- Foundation of all sciences, engineering, and technology.  
- Provides laws that describe natural phenomena in **mathematical form**.  

**Goal of Physics**:  
Describe all phenomena using a few **fundamental laws** → expressed in equations between measurable quantities.

---

## 1.2 Measurement: Accuracy, Precision & Uncertainty
- **Precision**: Repeatability of measurement; limited by instrument’s smallest division.  
  - Meter stick with 1 mm → precision ±0.5 mm.  
- **Accuracy**: Closeness to true value (affected by systematic errors like miscalibration).  
- **Random errors**: Statistical fluctuations; reduced by repeating measurements.  
- **Uncertainty**:  
  $$M \pm \delta M, \quad \%unc = \frac{\delta M}{M}\times 100\%$$  

**Rules for combining uncertainties**:  
- $A \times B$ or $A \div B$: Add % uncertainties.  
- $A^n$: Multiply % uncertainty of $A$ by $n$.  

---

## 1.3 Units & Dimensions
- **Fundamental quantities**:  
  - Length $(L)$, Mass $(M)$, Time $(T)$, Temperature $(K)$, Current $(A)$, Amount $(mol)$, Luminous Intensity $(cd)$.  

- **SI Units**: $m,\,kg,\,s,\,K,\,A,\,mol,\,cd$  
- **Derived Units**:  
  - Velocity: $[LT^{-1}]$ → m/s  
  - Acceleration: $[LT^{-2}]$ → m/s²  
  - Force: $[MLT^{-2}]$ → Newton (N)  
  - Energy: $[ML^2T^{-2}]$ → Joule (J)  

**Dimensional Analysis**:  
- Equation must be dimensionally consistent.  
- Example:  
  $$T = 2\pi \sqrt{\frac{L}{g}} \quad [T] = [L^{1/2}L^{-1/2}T] = T$$  

---

## 1.4 Significant Figures
- Rules:  
  - Non-zero digits → significant.  
  - Leading zeros → not significant.  
  - Trailing zeros → significant only if decimal present.  
- **Operations**:  
  - Addition/Subtraction → keep least decimal places.  
  - Multiplication/Division → least sig. figs.  

---

## 1.5 Vectors
- **Scalar**: Magnitude only (mass, temp).  
- **Vector**: Magnitude + direction (displacement, velocity, force).  

**Vector notation**:  
$$\vec{A} = A_x\hat{i} + A_y\hat{j} + A_z\hat{k}$$  
$$|\vec{A}| = \sqrt{A_x^2 + A_y^2 + A_z^2}$$  
$$\tan\theta = \frac{A_y}{A_x}$$  

**Vector operations**:  
- Addition: tip-to-tail or component method.  
- Resolution into components:  
  $$A_x = A\cos\theta, \quad A_y = A\sin\theta$$  

---

# Chapter 2: Kinematics in One Dimension
## 2.1 Mechanics Overview
- **Mechanics**: Study of motion and forces.  
  - *Kinematics*: Describes motion without cause.  
  - *Kinetics*: Explains motion (forces).  
  - *Statics*: Objects at rest.  

---

## 2.2 Position & Displacement
- **Position**: $x(t)$ relative to origin.  
- **Displacement**:  
  $$\Delta x = x_f - x_i$$ (vector, direction matters).  
- **Distance**: Total path length (scalar).  

---

## 2.3 Velocity & Speed
- **Average speed**:  
  $$s = \frac{d}{\Delta t}$$  
- **Average velocity**:  
  $$v = \frac{\Delta x}{\Delta t} = \frac{x_f - x_i}{t_f - t_i}$$  
- **Instantaneous velocity**:  
  $$v = \lim_{\Delta t\to 0} \frac{\Delta x}{\Delta t} = \frac{dx}{dt}$$  

---

## 2.4 Acceleration
- **Average acceleration**:  
  $$a = \frac{\Delta v}{\Delta t} = \frac{v_f - v_i}{t_f - t_i}$$  
- **Instantaneous acceleration**:  
  $$a = \frac{dv}{dt} = \frac{d^2x}{dt^2}$$  

⚠️ Negative acceleration ≠ always slowing down → depends on direction of $v$.  

---

## 2.5 Constant Acceleration Equations
For $a =$ constant:  
1. $$v(t) = v_0 + at$$  
2. $$x(t) = x_0 + v_0t + \tfrac{1}{2}at^2$$  
3. $$v^2 = v_0^2 + 2a(x - x_0)$$  

**Free Fall**:  
- Acceleration due to gravity: $a = g = 9.8\,\text{m/s}^2$  
- Position (if dropped from rest):  
  $$x(t) = \tfrac{1}{2}gt^2$$  

---

## 2.6 Graphical Interpretations
- **Slope of $x(t)$ graph = velocity.**  
- **Slope of $v(t)$ graph = acceleration.**  
- **Area under $v(t)$ graph = displacement.**  
- **Area under $a(t)$ graph = change in velocity.**  

---

# Chapter 3: Kinematics in Two Dimensions
## 3.1 Motion in 2D
- In 1D: sign (+/–) gives direction.  
- In 2D: need **vectors**.  
- **Position vector**:  
  $$\vec{r} = x\hat{i} + y\hat{j}$$  
- **Displacement vector**:  
  $$\Delta \vec{r} = \vec{r}_f - \vec{r}_i$$  

---

## 3.2 Velocity in 2D
- **Average velocity**:  
  $$\vec{v} = \frac{\Delta \vec{r}}{\Delta t}$$  
- **Instantaneous velocity**:  
  $$\vec{v} = \frac{d\vec{r}}{dt} = v_x \hat{i} + v_y \hat{j}$$  
  with  
  $$v_x = \frac{dx}{dt}, \quad v_y = \frac{dy}{dt}$$  

- Direction: tangent to path.  

---

## 3.3 Acceleration in 2D
- **Average acceleration**:  
  $$\vec{a} = \frac{\Delta \vec{v}}{\Delta t}$$  
- **Instantaneous acceleration**:  
  $$\vec{a} = \frac{d\vec{v}}{dt} = a_x\hat{i} + a_y\hat{j}$$  
  where  
  $$a_x = \frac{dv_x}{dt}, \quad a_y = \frac{dv_y}{dt}$$  

---

## 3.4 Projectile Motion
- Resolve motion into **horizontal** and **vertical** components.  

**Horizontal (no acceleration):**  
$$x(t) = v_0\cos\theta \cdot t$$  

**Vertical (acceleration $-g$):**  
$$y(t) = v_0\sin\theta \cdot t - \tfrac{1}{2}gt^2$$  

**Time of flight**:  
$$T = \frac{2v_0\sin\theta}{g}$$  

**Range**:  
$$R = \frac{v_0^2}{g}\sin 2\theta$$  

**Max height**:  
$$H = \frac{v_0^2 \sin^2\theta}{2g}$$  

---

## 3.5 General Equations of Motion
- Always true:  
  $$\vec{v} = \frac{d\vec{r}}{dt}, \quad \vec{a} = \frac{d\vec{v}}{dt} = \frac{d^2\vec{r}}{dt^2}$$  

- For constant $\vec{a}$:  
  $$\vec{r}(t) = \vec{r}_0 + \vec{v}_0t + \tfrac{1}{2}\vec{a}t^2$$  
  $$\vec{v}(t) = \vec{v}_0 + \vec{a}t$$  
  $$v^2 = v_0^2 + 2\vec{a}\cdot(\vec{r}-\vec{r}_0)$$  

---
