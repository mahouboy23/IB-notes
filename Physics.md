---
tags : mod Physique
---
Created: 2025-10-03

[[Exercise physics]] 
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
# Chapter 4: Force and Motion
## 4.1 Introduction
- **Force ($\vec{F}$)**: An interaction that causes an object to accelerate (a push or a pull).  
- The **vector sum of all forces** acting on an object is the **net force** or **resultant force**:  
  $$\sum \vec{F} = \text{net force}$$
- The study of how forces produce motion is called **dynamics**.  
- **Contact forces** act through physical touch (e.g., tension, normal, friction).  
- **Long-range forces** act at a distance (e.g., gravity, magnetic, electrostatic).  

---

## 4.2 Unit of Force
- **Definition (SI):**  
  The force that accelerates a mass of 1 kg by $1\,\text{m/s}^2$ is **1 newton (N)**.  
  $$1\,\text{N} = 1\,\text{kg·m/s}^2$$

**Other systems of units:**

| System | Force | Mass | Acceleration |
|:-------|:-------|:------|:--------------|
| SI | Newton (N) | kilogram (kg) | m/s² |
| CGS | dyne | gram (g) | cm/s² |
| British | pound (lb) | slug | ft/s² |

**Conversions:**
- $1\,\text{N} = 10^5\,\text{dyne} = 0.2255\,\text{lb}$  
- $1\,\text{dyne} = 1\,\text{g·cm/s}^2$  
- $1\,\text{lb} = 1\,\text{slug·ft/s}^2$  

---

## 4.3 Newton’s Laws of Motion
### Newton’s First Law (Law of Inertia)
> An object remains at rest or moves with constant velocity unless acted on by a net external force.

If  
$$\sum \vec{F} = 0 \quad \Rightarrow \quad \vec{v} = 0 \ \text{or constant}$$  

- Defines **inertial reference frames** — frames in which an object experiences zero net force and thus constant velocity.

---

### Newton’s Second Law (Fundamental Law of Dynamics)
> The acceleration $\vec{a}$ of an object is directly proportional to the net force $\sum \vec{F}$ and inversely proportional to its mass $m$.

$$\sum \vec{F} = m\vec{a}$$  

- Valid for $v \ll c$ (non-relativistic speeds).  
- Direction of $\vec{a}$ is the same as that of $\sum \vec{F}$.  

---

### Newton’s Third Law (Action-Reaction)
> When body A exerts a force $\vec{F}_{BA}$ on body B, body B exerts a force $\vec{F}_{AB}$ on body A equal in magnitude and opposite in direction:

$$\vec{F}_{BA} = -\vec{F}_{AB}$$  

- These forces act on **different objects**, so they do **not** cancel each other.

---

## 4.4 Particular Forces
### 1. Weight and Mass
- **Mass ($m$):** Measure of the amount of matter in a body; scalar quantity.  
- **Weight ($\vec{W}$):** Force due to Earth’s gravity:  
  $$\vec{W} = m\vec{g}$$  
  where $\vec{g}$ ≈ $9.81\,\text{m/s}^2$ (downward).  
- Weight depends on location (varies with $g$).

---

### 2. Normal Force ($\vec{N}$)
- The **contact force perpendicular** to a surface.  
- For a block resting on a flat surface:  
  $$\sum \vec{F} = m\vec{a} \Rightarrow \vec{N} + \vec{W} = 0$$  
  hence  
  $$N = W = mg$$  
- On an inclined plane:  
  $$N = mg\cos\theta$$  

---

### 3. Frictional Force ($f$)
- Acts **parallel** to contact surface and **opposes motion**.  
- Caused by microscopic surface irregularities.  
- Reduced by lubrication, polishing, or ball bearings.  

**Magnitude:**  
$$f = \mu N$$  
where $\mu$ = coefficient of friction (static or kinetic).

- **Static friction ($f_s$):** Opposes start of motion;  
  $$f_s \le \mu_s N$$  
- **Kinetic friction ($f_k$):** Opposes ongoing motion;  
  $$f_k = \mu_k N$$  
and $\mu_s > \mu_k$.

---

### 4. Air Resistance / Drag Force ($F_D$)
- Experienced by objects moving through air or fluid.  
- Acts **opposite** to motion.  
- Proportional to:
  - Cross-sectional area ($A$)  
  - Velocity ($v$)  

**At moderate speeds:**  
$$F_D = bv$$  
**At high speeds:**  
$$F_D = \tfrac{1}{2} C\rho A v^2$$  

**Net force (vertical motion):**  
$$mg - bv = ma = m\frac{dv}{dt}$$  

When terminal velocity $v_t$ is reached:  
$$mg = bv_t \Rightarrow v_t = \frac{mg}{b}$$  

---

### 5. Tension Force ($\vec{T}$)
- Force transmitted through a string, rope, or cable under tension.  
- Same magnitude of tension throughout an ideal (massless) rope.  
- The rope pulls on both connected objects with equal and opposite forces:  
  $$|\vec{T}_1| = |\vec{T}_2| = T$$  

---

### 6. Gravitational Force
- A long-range attractive force between any two masses:  
  $$F = G\frac{Mm}{r^2}$$  
  where $G = 6.674\times10^{-11}\,\text{N·m}^2\text{/kg}^2$.  
- Near Earth’s surface:  
  $$F = mg$$  

---

## 4.5 Free Body Diagram (FBD)
- **Definition:** A diagram showing all the external forces acting on a body.  
- **Steps to draw:**
  1. Isolate the object of interest.  
  2. Represent the object as a point or box.  
  3. Draw all forces (gravity, normal, friction, tension, applied, etc.).  
  4. Label each force clearly with direction and type.  

Used to apply Newton’s Second Law component-wise:  
$$\sum F_x = ma_x, \quad \sum F_y = ma_y$$  

---

## 4.6 Problem Solving Strategy
1. **Identify** the object(s) to analyze.  
2. **Draw FBD** for each object.  
3. **Resolve** forces into components (x, y).  
4. **Apply** Newton’s Second Law in each direction.  
5. **Solve** for unknowns (acceleration, tension, normal, etc.).  
6. **Check** direction, units, and limits.  

---

## 4.7 Worked Examples

### **Example 1: Force on a Truck**
> A $20{,}000\,\text{kg}$ truck accelerates at $1.5\,\text{m/s}^2$ on level ground.  
> Find the driving force and the normal force exerted by the ground.

**Solution:**
- Given: $m = 20{,}000\,\text{kg}$, $a = 1.5\,\text{m/s}^2$, $g = 9.8\,\text{m/s}^2$  

**In the x-direction:**  
$$\sum F_x = F = ma = (20{,}000)(1.5) = 30{,}000\,\text{N}$$  

**In the y-direction:**  
$$\sum F_y = N - mg = 0 \Rightarrow N = mg = (20{,}000)(9.8) = 196{,}000\,\text{N}$$  

**Kinematics after 2 s:**
$$v = v_0 + at = 0 + 1.5(2) = 3\,\text{m/s}$$  
$$x = v_0t + \tfrac{1}{2}at^2 = 0 + 0.5(1.5)(2^2) = 3\,\text{m}$$  

---

### **Example 2: Tensions in Three Cords**
> A $21\,\text{kg}$ block hangs from three cords as shown.  
> Given $\sin\theta = 4/5$, $\cos\theta = 3/5$, $\sin\phi = 5/13$, $\cos\phi = 12/13$, find all tensions.

**Step 1: For vertical cord**
$$T_1 = mg = 21(10) = 210\,\text{N}$$  

**Step 2: Apply equilibrium at the knot**
$$\sum F_x = 0 \Rightarrow T_3\cos\theta = T_2\cos\phi$$  
$$\sum F_y = 0 \Rightarrow T_3\sin\theta + T_2\sin\phi = T_1$$  

From the first:
$$T_3 = \frac{\cos\phi}{\cos\theta}T_2 = \frac{12/13}{3/5}T_2 = \frac{20}{13}T_2$$  

Substitute into the second:
$$\frac{20}{13}\frac{4}{5}T_2 + \frac{5}{13}T_2 = 210$$  
$$\frac{21}{13}T_2 = 210 \Rightarrow T_2 = 130\,\text{N}$$  
$$T_3 = \frac{20}{13}(130) = 200\,\text{N}$$  

✅ **Final answers:**  
- $T_1 = 210\,\text{N}$  
- $T_2 = 130\,\text{N}$  
- $T_3 = 200\,\text{N}$  

---

# Summary of Key Equations
| Concept           | Formula                        | Notes                    |
| :---------------- | :----------------------------- | :----------------------- |
| Newton’s 2nd Law  | $\sum \vec{F} = m\vec{a}$      | Main dynamics equation   |
| Weight            | $W = mg$                       | Force due to gravity     |
| Friction          | $f = \mu N$                    | $\mu_s > \mu_k$          |
| Normal on incline | $N = mg\cos\theta$             | Perpendicular to surface |
| Drag (linear)     | $F_D = bv$                     | Low-speed approximation  |
| Drag (quadratic)  | $F_D = \frac{1}{2}C\rho A v^2$ | High-speed case          |
| Terminal velocity | $v_t = \frac{mg}{b}$           | Constant speed reached   |
| Gravitational law | $F = G\frac{Mm}{r^2}$          | Universal attraction     |

# Chapter 5: Work & Energy

---

# 5.1 Work

- Work by constant force:  
  $$W = \vec F \cdot \vec d = Fd\cos\theta$$
- Sign meaning:  
  - **+W** → speeds up  
  - **0** → no change  
  - **–W** → slows down  

- Unit:  
  $$1\,\text{J} = 1\,\text{N·m}$$  

(("diagram: force, displacement, angle θ"))

---

# 5.2 Work by a Variable Force

- General case:  
  $$W = \int \vec F \cdot d\vec r$$  

- Along x-axis:  
  $$W = \int F(x)\,dx$$  

- Spring force:  
  $$F = -kx$$  
  $$W = -\frac{1}{2}kx^2$$  

(("diagram: area under F-x graph"))

---

# 5.3 Kinetic & Potential Energy

### Kinetic Energy
$$K = \frac12 mv^2$$

### Potential Energies
- Gravity (near Earth):  
  $$U = mgh$$
- Spring:  
  $$U = \frac12 kx^2$$

### Mechanical Energy
$$E = K + U$$  

---

# 5.4 Conservative vs Non-Conservative Forces

- **Conservative:** work independent of path (gravity, spring)  
- **Non-conservative:** path-dependent (friction)

### Work–Energy Theorem
$$W_{\text{net}} = \Delta K$$  

(("diagram: roller coaster energy changes"))

---

# Chapter 6: Momentum, Collisions & Center of Mass

---

# 6.1 Linear Momentum

- Definition:  
  $$\vec p = m\vec v$$

- Newton’s 2nd Law (momentum form):  
  $$\vec F_{\text{net}} = \frac{d\vec p}{dt}$$  

---

# 6.2 Impulse

- Impulse changes momentum:  
  $$\vec J = \int \vec F\, dt = \Delta\vec p$$  

---

# 6.3 Conservation of Momentum

If no external forces:  
$$\vec p_i = \vec p_f$$  

- Works in all collisions.

(("diagram: two carts colliding"))

---

# 6.4 Collisions

### Elastic Collision
- Momentum conserved  
- KE conserved  

1D formulas:  
$$v_1' = \frac{(m_1 - m_2)v_1 + 2m_2 v_2}{m_1 + m_2}$$  
$$v_2' = \frac{(m_2 - m_1)v_2 + 2m_1 v_1}{m_1 + m_2}$$  

### Inelastic Collision
- Momentum conserved  
- KE **not** conserved  

### Perfectly Inelastic
- Objects stick together:  
  $$v_f = \frac{m_1v_1 + m_2v_2}{m_1 + m_2}$$  

---

# 6.5 Center of Mass (CM)

- Definition:  
  $$x_{\text{cm}} = \frac{\sum m_i x_i}{\sum m_i}, \qquad y_{\text{cm}} = \frac{\sum m_i y_i}{\sum m_i}$$  

- Continuous mass:  
  $$\vec r_{\text{cm}} = \frac{1}{M}\int \vec r\,dm$$  

### Motion of the CM
$$M\vec a_{\text{cm}} = \vec F_{\text{ext}}$$  

(("diagram: system of particles with center of mass"))

---

# Chapter 7: Circular Motion & Centripetal Acceleration

---

# 7.1 Kinematics of Circular Motion

### Angular relationships
- Tangential speed:  
  $$v = \omega r$$  

### Centripetal Acceleration
$$a_R = \frac{v^2}{r} = \omega^2 r$$  

(("diagram: vector directions for a_R and v"))

---

# 7.2 Period & Frequency

- Frequency:  
  $$f = \frac{1}{T}$$  
- Speed in circular motion:  
  $$v = \frac{2\pi r}{T}$$  

---

# 7.3 Dynamics of Circular Motion

Centripetal force requirement:  
$$F_{\text{net}} = m\frac{v^2}{r}$$  

Not a new force — supplied by tension, gravity, friction, etc.

---

# 7.4 Vertical Circular Motion

### At the bottom:
$$F = mg + \frac{mv^2}{r}$$  

### At the top:
$$F = \frac{mv^2}{r} - mg$$  

### Condition to stay taut:
$$v_{\min} = \sqrt{rg}$$  

(("diagram: forces at top and bottom of circle"))

---

# 7.5 Flat Curves (Friction-Based)

Friction provides centripetal force:
$$f_s = \frac{mv^2}{r}$$  

No-skid speed:
$$v_{\max} = \sqrt{\mu_s g r}$$  

---

# 7.6 Banked Curves (No Friction)

$$\tan\theta = \frac{v^2}{rg}$$  

(("diagram: banked angle and forces"))

---

# 7.7 Non-Uniform Circular Motion

Total acceleration:
$$a = \sqrt{a_R^2 + a_{\text{tan}}^2}$$  

Where:  
- Radial: \(a_R = \frac{v^2}{r}\)  
- Tangential: \(a_{\text{tan}} = \frac{dv}{dt}\)  

---

# Summary of Key Equations (Ch. 5–7)

| Concept | Formula |
|--------|---------|
| Work | $W = Fd\cos\theta$ |
| Kinetic Energy | $K = \frac12 mv^2$ |
| Potential Energy (spring) | $U = \frac12 kx^2$ |
| Work–Energy theorem | $W_{\text{net}} = \Delta K$ |
| Momentum | $p = mv$ |
| Impulse | $J = \Delta p$ |
| Perfectly inelastic v | $v_f = \frac{m_1v_1 + m_2v_2}{m_1 + m_2}$ |
| CM | $x_{\text{cm}} = \frac{\sum m_i x_i}{M}$ |
| Centripetal accel | $a_R = v^2/r$ |
| Centripetal force | $F = mv^2/r$ |
| Banked turn | $\tan\theta = v^2/(rg)$ |


# Chapter 8: Rotational Kinematics & Torque

---

# 8.1 Rotational Motion
- A rotating point is described by its **angular position** $\theta$.  
- Angles measured in **radians**:  
  $$360^\circ = 2\pi \text{ rad} = 1 \text{ rev}$$
- Arc length–angle relation:  
  $$\ell = r\theta$$  
- $\ell$: linear distance  
- $\theta$: angular displacement  
- $r$: radius  

![[file-20251121133054309.png]]

---

# 8.2 Angular Velocity
- **Average angular velocity**:  
  $$\bar{\omega} = \frac{\Delta\theta}{\Delta t}$$  
- **Instantaneous angular velocity**:  
  $$\omega = \frac{d\theta}{dt}$$
- **Angular acceleration**:  
  $$\bar{\alpha} = \frac{\Delta\omega}{\Delta t}, \qquad \alpha = \frac{d\omega}{dt}$$  

### Relation to linear motion
- Tangential speed:  
  $$v = \omega r$$  
- Tangential acceleration:  
  $$a_{\text{tan}} = \alpha r$$  
- Radial (centripetal) acceleration:  
  $$a_R = \omega^2 r$$  

(("diagram: linear vs angular quantities"))

---

# 8.3 Relating Angular Velocity & Frequency
- Conversion relation:  
  $$\omega = 2\pi f$$  
- Period:  
  $$T = \frac{1}{f} = \frac{2\pi}{\omega}$$  

### Example (from slides)
(("example placeholder: wheel rotates 1 rev in 0.025s"))

---

# 8.4 Constant Angular Acceleration
**Linear ↔ Angular analogy:**

| Linear | Angular |
|--------|---------|
| $x$ | $\theta$ |
| $v$ | $\omega$ |
| $a$ | $\alpha$ |

**Equations:**
1. $$\omega = \omega_0 + \alpha t$$  
2. $$\theta = \theta_0 + \omega_0 t + \frac12 \alpha t^2$$  
3. $$\omega^2 = \omega_0^2 + 2\alpha(\theta - \theta_0)$$  

---

# 8.5 Rolling Without Slipping
- Condition:  
  $$v = \omega r$$  
- Motion consists of **rotation + translation**.

(("diagram: rolling wheel"))

---

# 8.6 Torque
- **Torque** = rotational effect of a force  
  $$\tau = rF\sin\theta$$  
- Sign convention:  
  - ccw = positive  
  - cw = negative  

### Lever arm
- Perpendicular distance from pivot to force line of action.  
- Only the component of force **perpendicular** to $r$ produces torque.

(("diagram: lever arm, angle θ"))

---

# 8.7 Static Equilibrium
A system is in static equilibrium if:

1. **Translational:**  
   $$\sum \vec{F} = 0$$  
2. **Rotational:**  
   $$\sum \tau = 0$$  

Notes:  
- A force passing through pivot → **zero torque**.  
- Choosing pivot at unknown force simplifies equations.

### Example (from slides)
$$T = \frac{mg}{2\sin12^\circ} = 590\text{ N}$$

(("diagram: cable tension example"))

---

# 8.8 Stability & Balance
### Stable equilibrium
- CoG inside base → returns to equilibrium.

### Neutral equilibrium
- CoG stays same height → new position same “energy”.

### Unstable equilibrium
- Small displacement → system moves away (falls).

(("diagrams: stable vs neutral vs unstable"))

---

# Chapter 9: Rotation – Dynamics, Inertia & Angular Momentum

---

# 9.1 Rotational Dynamics
Newton’s 2nd law for rotation:

$$\sum \tau = I\alpha$$  

- $I$ = moment of inertia  
  $$I = \sum m r^2$$  

### Standard $I$ values (axis through center)
- Hollow cylinder: $I = MR^2$  
- Solid cylinder: $I = \frac12 MR^2$  
- Solid sphere: $I = \frac25 MR^2$  
- Thin rod: $I = \frac{1}{12} ML^2$  

(("diagram: mass distribution and inertia"))

---

# 9.2 Rotational Kinetic Energy
Rotation only:
$$K = \frac12 I\omega^2$$  

Rolling motion:  
$$K = \frac12 Mv_{\text{cm}}^2 + \frac12 I_{\text{cm}}\omega^2$$  

### Example (sphere rolling 1 m down incline)
Using energy conservation:

$$mgh = \frac12 mv^2 + \frac12 I\left(\frac{v}{R}\right)^2$$  

For solid sphere:
$$v_{\text{cm}} = 3.74\ \text{m/s}$$  

Energy distribution:
- Rotational: $K_{\text{rot}} = \frac27 K_{\text{total}}$  
- Translational: $K_{\text{trans}} = \frac57 K_{\text{total}}$

---

# 9.3 Angular Momentum
- Linear momentum:  
  $$p = mv$$  
- Angular momentum:  
  $$L = I\omega$$  

### Angular impulse
$$\Delta L = \tau \Delta t$$  

### Conservation
$$L_i = L_f$$  
When no external torque acts.

### Example (two disks stick together)
$$I_2\omega_0 = (I_1 + I_2)\omega'$$  
$$\omega' = 467\text{ rad/s}$$  

(("diagram: two rotating disks"))

---

# Summary of Key Formulas (Ch. 8 & 9)

| Concept | Formula |
|--------|---------|
| Arc length | $\ell = r\theta$ |
| Angular velocity | $\omega = \frac{d\theta}{dt}$ |
| Tangential speed | $v = \omega r$ |
| Angular acceleration | $\alpha = \frac{d\omega}{dt}$ |
| Frequency relation | $\omega = 2\pi f$ |
| Constant α equations | $\omega=\omega_0+\alpha t$, $\theta=\theta_0+\omega_0 t + \frac12\alpha t^2$, $\omega^2=\omega_0^2+2\alpha\Delta\theta$ |
| Torque | $\tau = rF\sin\theta$ |
| Static equilibrium | $\sum F = 0$, $\sum \tau = 0$ |
| Rotational KE | $K=\frac12 I\omega^2$ |
| Rolling KE | $K=\frac12Mv^2 + \frac12I\omega^2$ |
| Angular momentum | $L = I\omega$ |
| Angular impulse | $\Delta L = \tau\Delta t$ |

