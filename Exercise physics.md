---
tags:
  - mod
  - Physique
---
Created: 2025-11-15

# Chapter: Work, Energy, Circular Motion & Momentum  
Created: 2025-11-18

---

# A. Kinetic Energy

## **A.i Kinetic Energy of a Spaceship**
**Given:**  
- $m = 2.9 \times 10^5\ \text{kg}$  
- $v = 11.2\ \text{km/s} = 1.12\times10^4\ \text{m/s}$  

**Calculation:**  
$$K = \frac12 mv^2$$  
$$v^2 = (1.12\times10^4)^2 = 1.2544\times10^8$$  
$$K = 0.5 \times 2.9\times10^5 \times 1.2544\times10^8$$  
$$K = 1.82\times10^{13}\ \text{J}$$  

**Final Answer:**  
- $\boxed{1.82\times10^{13}\ \text{J}}$

---

## **A.ii Electron Speed from Kinetic Energy**
**Given:**  
- $m = 9.11\times10^{-31}\ \text{kg}$  
- $K = 6.7\times10^{-19}\ \text{J}$  

Use:  
$$v=\sqrt{\frac{2K}{m}}$$  

Compute:  
$$\frac{2K}{m} = \frac{1.34\times10^{-18}}{9.11\times10^{-31}} = 1.47\times10^{12}$$  
$$v = \sqrt{1.47\times10^{12}} = 1.21\times10^6\ \text{m/s}$$  

**Final Answer:**  
- $\boxed{1.21\times10^6\ \text{m/s}}$

---

# B. Work

## **B.i Work Done by a Constant Force**
**Given:**  
- $\vec{F} = (210\hat{i} - 150\hat{j})\ \text{N}$  
- $\vec{d} = (15\hat{i} - 12\hat{j})\ \text{m}$  

Work = dot product  
$$W = F_x d_x + F_y d_y$$  
$$W = 210(15) + (-150)(-12) = 3150 + 1800 = 4950\ \text{J}$$  

**Final Answer:**  
- $\boxed{4950\ \text{J}}$

---

## **B.ii Work from a Force vs Position Graph (Explanation Template)**  
⚠️ The graph from the assignment is missing, so here is **exactly how to solve it** when you paste the graph later.

### **How to compute the work**
Work = area under the $F_x$ vs $x$ curve:  
$$W = \int_a^b F_x(x)\,dx$$  

### **Rules for the area**
- Rectangle: $A = F\Delta x$  
- Triangle: $A = \tfrac12 F\Delta x$  
- Trapezoid:  
  $$A = \frac{F_1 + F_2}{2}\Delta x$$  
- Areas **above** x–axis → **positive**  
- Areas **below** x–axis → **negative**

---

### **Template (Fill in When You Add Graph)**

#### **(a) Interval $0$ to $5$ m**
$$W_{0\to5} = \text{area from } 0 \text{ to } 5$$

#### **(b) Interval $5$ to $10$ m**
$$W_{5\to10} = \text{area from } 5 \text{ to } 10$$

#### **(c) Interval $10$ to $15$ m**
$$W_{10\to15} = \text{area from } 10 \text{ to } 15$$

#### **(d) Total Work**
$$W_{\text{total}} = W_{0\to5} + W_{5\to10} + W_{10\to15}$$

---

### Paste the graph here when ready:
👉 *(Add image or values in a table — I will compute the exact numbers.)*

---

## **B.iii Work Done by a Position-Dependent Force**
**Given:**  
- $\vec{F}(x,y) = (2x)\hat{i} + 3\hat{j}$  
- From $(2,3)$ to $(-4,-3)$  

Work:  
$$W = \int 2x\,dx + \int 3\,dy$$  

x-part:  
$$\int_{2}^{-4} 2x\,dx = [x^2]_{2}^{-4} = 16 - 4 = 12$$  

y-part:  
	$$\int_{3}^{-3} 3\,dy = 3(-3 - 3) = -18$$  

Total:  
$$W = 12 - 18 = -6\ \text{J}$$  

**Final Answer:**  
- $\boxed{-6\ \text{J}}$

---

# C. Work–Energy Theorem

	## **C.i Box Pushed Across Floor**
**Given:**  
- $m = 40$ kg  
- $F_{\text{app}} = 130$ N  
- $\mu = 0.30$  
- $d = 5$ m  
- $g = 9.8$  

### (a) Applied work  
$$W_{\text{app}} = Fd = 650\ \text{J}$$  

### (b) Work by friction  
$$f = \mu mg = 117.6\ \text{N}$$  
$$W_f = -fd = -588\ \text{J}$$  

### (c) Net work  
$$W_{\text{net}} = 650 - 588 = 62\ \text{J}$$  

### (d) Final speed  
$$\Delta K = \tfrac12 mv^2 = 62$$  
$$v = \sqrt{\frac{124}{40}} = 1.76\ \text{m/s}$$  

**Final Answers:**  
- $W_{\text{app}} = 650$ J  
- $W_f = -588$ J  
- $\Delta K = 62$ J  
- $\boxed{v = 1.76\ \text{m/s}}$

---

## **C.ii Pulling Object Up an Incline**
**Given:**  
- $m = 10$ kg  
- $u = 1.5$ m/s  
- $F = 100$ N  
- $\theta = 20^\circ$  
- $s = 5$ m  
- $\mu_k = 0.4$  

Height:  
$$h = s\sin20^\circ = 1.71\ \text{m}$$  

### (a) Work by gravity  
$$W_g = -mgh = -167.6\ \text{J}$$  

### (b) Work by friction  
$$N = mg\cos20^\circ = 92.14\ \text{N}$$  
$$f_k = 0.4N = 36.86$$  
$$W_f = -184.3$$  

### (c) Work by pulling force  
$$W_F = 100\times5 = 500\ \text{J}$$  

### (d) Net work  
$$\Delta K = 500 - 167.6 - 184.3 = 148.1\ \text{J}$$  

### (e) Final speed  
$$v^2 = u^2 + \frac{2\Delta K}{m} = 2.25 + 29.624$$  
$$v = 5.65\ \text{m/s}$$  

**Final Answer:**  
- $\boxed{5.65\ \text{m/s}}$

---

# F. Circular Motion

## **F.i Artificial Gravity Space Station**
**Given:**  
- $r = 440$ m  
- $a_c = 2.5g = 24.5\ \text{m/s}^2$  

### (a) Speed  
$$v = \sqrt{a_c r} = \sqrt{10780} = 103.84\ \text{m/s}$$  

### (b) Period  
$$T = \frac{2\pi r}{v} = 26.6\ \text{s}$$  

### (c) rpm  
$$\text{rpm} = \frac{60}{26.6} = 2.25$$  

**Final Answers:**  
- $v = 103.8$ m/s  
- $T = 26.6$ s  
- $\boxed{2.25\ \text{rpm}}$

---

## **F.ii Pail in Vertical Circular Motion**
**Given:**  
- $m = 5$ kg  
- $v = 7$ m/s  
- $r = 0.9$ m  

Centripetal acceleration:  
$$a_c = \frac{v^2}{r} = 54.44\ \text{m/s}^2$$  

### (a) Acceleration at top
Direction: downward  
Magnitude: $54.44$ m/s²  

### (b) Tension  
At top:  
$$\frac{mv^2}{r} = T + mg$$  
$$T = mv^2/r - mg$$  
$$T = 5(54.44) - 49 = 223\ \text{N}$$  

**Final Answer:**  
- $\boxed{T = 223\ \text{N}}$

---

# G. Linear Momentum & Collisions

## **G.i Collision Between Two Masses**

**Given:**  
- $m_A = 2.5\ \text{kg}$  
- $v_{A,i} = 25\ \text{m/s}$  
- $m_B = 7.5\ \text{kg}$  
- $v_{B,i} = 0$  
- $v_{A,f} = -5\ \text{m/s}$  

---

## (a) Final velocity of B

### **Step 1 — Use the momentum conservation law**

For a collision in 1D:  
$$p_i = p_f$$  
$$m_A v_{A,i} + m_B v_{B,i} = m_A v_{A,f} + m_B v_{B,f}$$

---

### **Step 2 — Substitute known values**

$$2.5(25) + 7.5(0) = 2.5(-5) + 7.5 v_{B,f}$$

Simplify left side:  
$$2.5 \cdot 25 = 62.5$$  

Simplify right side:  
$$2.5(-5) = -12.5$$  

So the equation becomes:  
$$62.5 = -12.5 + 7.5 v_{B,f}$$

---

### **Step 3 — Solve for $v_{B,f}$**

Move $-12.5$ to the left side:  
$$62.5 + 12.5 = 7.5 v_{B,f}$$  
$$75 = 7.5 v_{B,f}$$  

Now divide both sides by 7.5:  
$$v_{B,f} = \frac{75}{7.5} = 10\ \text{m/s}$$  

---

### ✅ **Final Answer (a):**  
- $\boxed{v_{B,f} = 10\ \text{m/s}}$

---

## (b) Type of Collision

### **Step 1 — Compute initial kinetic energy**

Only A is moving initially:  
$$K_i = \frac12 m_A v_{A,i}^2$$  
$$K_i = \frac12(2.5)(25^2)$$  
$$K_i = 1.25 \cdot 625 = 781.25\ \text{J}$$  

---

### **Step 2 — Compute final kinetic energy**

Both masses move after collision:  
$$K_f = \frac12 m_A v_{A,f}^2 + \frac12 m_B v_{B,f}^2$$  

Substitute values:  
$$K_f = \frac12(2.5)(5^2) + \frac12(7.5)(10^2)$$  
$$K_f = 1.25(25) + 3.75(100)$$  
$$K_f = 31.25 + 375 = 406.25\ \text{J}$$  

---

### **Step 3 — Compare energies**

- $K_i = 781.25$ J  
- $K_f = 406.25$ J  

Energy **decreased**, so the collision is **inelastic**.

---

### ✅ **Final Answer (b):**  
- $\boxed{\text{Collision is inelastic}}$

Created: 2025-11-21  
Source: [[Final_Exam_Physics_I_DUNIS_Spring_2024.pdf]] :contentReference[oaicite:1]{index=1}

# Final Exam — Physics I (Solutions)

---

## Question 1 (Multiple choice)
**Question (verbatim):**  
Choose the correct option:

1. The unit of work is joule. The other physical quantity that has same unit is  
   (a) power (b) velocity (c) energy (d) force

2. A ball is dropped from a height of 10 m

   (a) Its potential energy increases and kinetic energy decreases during the falls

   (b) Its potential energy is equal to the kinetic energy during the fall.

   (c) The potential energy decreases and the kinetic energy increases during the fall.

   (d) The potential energy is 0 and kinetic energy is maximum while it is falling.

3. If the velocity of a body is doubled its kinetic energy  
   (a) gets doubled (b) becomes half (c) does not change (d) becomes 4 times

4. A student carries a bag weighing 5 kg from the ground floor to his class on the first floor that is 2 m high. The work done by the boy is  
   (a) 1 J (b) 10 J (c) 100 J (d) 1000 J

5. The work done is 0 if

   (a) The body shows displacement in the opposite direction of the force applied.

   (b) The body shows displacement in the same direction as that of the force applied.

   (c) The body shows a displacement in perpendicular direction to the force applied.

   (d) The body masses obliquely to the direction of the force applied.

**Solutions / Answers (with reasoning):**

1. Unit of work = joule (J). Energy also has unit joule.  
   **Answer:** **(c) energy**

2. A dropped ball (falling under gravity): gravitational potential energy **decreases** while kinetic energy **increases** as it falls (conversion of potential → kinetic).  
   **Answer:** **(c)**

3. Kinetic energy \(K=\tfrac12 m v^2\). If \(v\to 2v\), then \(K\to \tfrac12 m (2v)^2 = \tfrac12 m 4v^2 = 4(\tfrac12 m v^2)\). So kinetic energy becomes **4 times**.  
   **Answer:** **(d)**

4. Work done against gravity: \(W = m g h\).  
   - \(m=5.0\ \text{kg}\)  
   - \(g=9.8\ \text{m/s}^2\) (use standard)  
   - \(h=2.0\ \text{m}\)

   Compute: \(W = 5.0\times 9.8\times 2.0\).

   Step-by-step multiplication:
   - \(5.0\times 9.8 = 49.0\) (because \(5\times 9.8=49\))
   - \(49.0\times 2.0 = 98.0\)

   So \(W = 98.0\ \text{J}\), which is closest to **100 J** among the choices.  
   **Answer:** **(c)**

5. Work \(W = \vec F\cdot\vec d = F d \cos\theta\). If displacement is **perpendicular** to the force, \(\theta=90^\circ\) and \(\cos90^\circ=0\) so \(W=0\).  
   **Answer:** **(c)**

---

## Question 2
**Question (verbatim):**  
A uniform rod 1.00 m long weighs 250.0 newtons and is hanging from two cords, one connected xA = 40.0 cm from the center, and the other connected xB = 20.0 cm from the center. The center of mass of the rod is at its geometric center.

(a) Find the tension \(T_A\) in the cord connected near the left end.

(b) Find the tension \(T_B\) in the cord connected near the right end.

**Solution:**

**Given / understood:**
- Rod weight (total downward force) \(W = 250.0\ \text{N}\).
- Two upward tensions \(T_A\) (left, at \(x_A=0.40\ \text{m}\) left of center) and \(T_B\) (right, at \(x_B=0.20\ \text{m}\) right of center).
- Rod is static → translational and rotational equilibrium.

**1) Translational equilibrium (vertical):**
\[
T_A + T_B = W = 250.0\ \text{N}. \tag{1}
\]

**2) Rotational equilibrium (take torques about the center):**  
Choose positive torque as counterclockwise (ccw). The weight acts at center → zero torque. \(T_A\) is at \(x=-0.40\) m (left) producing torque of sign depending on chosen direction. Upward \(T_A\) at negative \(x\) gives a clockwise tendency (negative), while \(T_B\) at \(+0.20\) m gives ccw (positive). Sum of torques about center = 0:

\[
\tau_{\text{net}} = T_B(0.20\,\text{m}) - T_A(0.40\,\text{m}) = 0. \tag{2}
\]

From (2):
\[
0.20\,T_B = 0.40\,T_A \quad\Rightarrow\quad T_B = \frac{0.40}{0.20}T_A = 2\,T_A. \tag{3}
\]

Substitute (3) into (1):
\[
T_A + 2T_A = 250.0 \quad\Rightarrow\quad 3T_A = 250.0.
\]

Compute \(T_A\):
- \(T_A = \dfrac{250.0}{3}.\)
- Division: \(250.0 \div 3 = 83.333\ldots\)

Round to three significant figures: **\(T_A = 83.3\ \text{N}\)**.

Then \(T_B = 2T_A = 2\times 83.333\ldots = 166.666\ldots\)

Round to three significant figures: **\(T_B = 166.7\ \text{N}\)**.

**Final answers:**  
- \(T_A = 83.3\ \text{N}\)  
- \(T_B = 166.7\ \text{N}\)

---

## Question 3
**Question (verbatim):**  
Two balls made from clay of masses \(m_1 = 1.0\ \text{kg}\) and \(m_2 = 2.5\ \text{kg}\) travel with speeds of \(v_1 = 2.0\ \text{m/s}\) and \(v_2 = 1.0\ \text{m/s}\) and collide at the origin as shown in Fig I. After collision, they stick together and move in the direction shown in Fig II.

(a) Derive all the necessary equations to find the direction and magnitude of the common velocity after collision

(b) Calculate the direction (\(\theta\)) and magnitude of the common velocity (\(v\)) after collision.

**Note / assumption:** The PDF refers to Fig I/II. The usual (and most common) classroom arrangement for this problem is that \(m_1\) moves along the \(+x\)-direction with speed \(v_1\) and \(m_2\) moves along the \(+y\)-direction with speed \(v_2\) toward the collision point at the origin. I will solve with that standard geometry (if your figure is different, tell me and I will adjust).

**Solution (derivation & calculation):**

- Conservation of linear momentum (inelastic collision where objects stick together). No external impulse (assume negligible external forces during the collision), so momentum conserved:

\[
\vec{p}_{\text{initial}} = \vec{p}_{\text{final}}.
\]

Write components (take \(+\hat{\imath}\) to the right, \(+\hat{\jmath}\) upward):

Initial momenta:
- \( \vec{p}_1 = m_1 v_1 \,\hat{\imath} = (m_1 v_1)\,\hat{\imath}\).
- \( \vec{p}_2 = m_2 v_2 \,\hat{\jmath} = (m_2 v_2)\,\hat{\jmath}\).

Total initial momentum:
\[
\vec{p}_{\text{init}} = (m_1 v_1)\,\hat{\imath} + (m_2 v_2)\,\hat{\jmath}.
\]

After collision, the two masses stick: total mass \(M = m_1 + m_2\). Let \(\vec{v}\) be the common velocity:
\[
\vec{p}_{\text{final}} = M \vec{v}.
\]

Conservation:
\[
M\vec{v} = (m_1 v_1)\,\hat{\imath} + (m_2 v_2)\,\hat{\jmath}.
\]

So component equations:
\[
v_x = \frac{m_1 v_1}{M}, \qquad v_y = \frac{m_2 v_2}{M}.
\]

Magnitude:
\[
v = \sqrt{v_x^2 + v_y^2}.
\]

Direction (angle from +x axis, measured counterclockwise):
\[
\theta = \arctan\!\left(\frac{v_y}{v_x}\right).
\]

**Plug numbers in:**
- \(m_1 = 1.0\ \text{kg}\), \(v_1 = 2.0\ \text{m/s}\) → \(m_1 v_1 = 1.0\times 2.0 = 2.0\ \text{kg·m/s}\).
- \(m_2 = 2.5\ \text{kg}\), \(v_2 = 1.0\ \text{m/s}\) → \(m_2 v_2 = 2.5\times 1.0 = 2.5\ \text{kg·m/s}\).
- Total mass \(M = m_1 + m_2 = 1.0 + 2.5 = 3.5\ \text{kg}\).

Compute components:
- \(v_x = \dfrac{2.0}{3.5}.\) Long division: \(2.0 \div 3.5 = 0.5714285714\ldots\)  
  Keep 6 dp: \(v_x = 0.571429\ \text{m/s}\).

- \(v_y = \dfrac{2.5}{3.5}.\) Division: \(2.5 \div 3.5 = 0.7142857143\ldots\)  
  Keep 6 dp: \(v_y = 0.714286\ \text{m/s}\).

Magnitude:
\[
v = \sqrt{(0.5714286)^2 + (0.7142857)^2}.
\]
Compute squares:
- \(0.5714286^2 \approx 0.3265306\)  (since \(4/7 \approx 0.5714286\), square \(\approx 16/49=0.3265306\))
- \(0.7142857^2 \approx 0.5102041\)  (since \(5/7 \approx 0.7142857\), square \(\approx 25/49=0.5102041\))

Sum: \(0.3265306 + 0.5102041 = 0.8367347\).

Now sqrt: \(v = \sqrt{0.8367347} \approx 0.914732\ \text{m/s}.\)

Angle:
\[
\theta = \arctan\!\left(\frac{v_y}{v_x}\right) = \arctan\!\left(\frac{0.7142857}{0.5714286}\right) = \arctan(1.25).
\]
\(\arctan(1.25) \approx 51.340^\circ = 0.89606\ \text{rad}.\)

**Final numeric answers (rounded reasonably):**
- Magnitude of common velocity: \(v \approx 0.915\ \text{m/s}\).
- Direction: \(\theta \approx 51.34^\circ\) (measured from +x axis), or \(\theta \approx 0.8961\ \text{rad}\).

---

## Question 4
**Question (verbatim):**  
A wheel starts from rest and rotates with a constant angular acceleration to reach an angular speed of \(12\ \text{rad/s}\) in \(3\ \text{s}\). The wheel has a point \(P\) on its rim. The radius of the wheel from point \(P\) is \(0.5\ \text{m}\).

Find:

(a) the magnitude of the angular acceleration of the wheel,  
(b) the angle in radians through which it rotates in this time,  
(c) the tangential speed of the point P at \(t = 3\ \text{s}\),  
(d) the tangential acceleration of the point P at \(t = 3\ \text{s}\) and  
(e) the radial acceleration of the point P at \(t = 3\ \text{s}\).

**Solution:**

**Given:**
- Initial angular speed \(\omega_0 = 0\) (starts from rest).
- Final angular speed \(\omega = 12\ \text{rad/s}\) at time \(t = 3.0\ \text{s}\).
- Radius \(r = 0.50\ \text{m}\).
- Constant angular acceleration \(\alpha\).

**(a) Angular acceleration \(\alpha\):**  
\[
\alpha = \frac{\Delta\omega}{\Delta t} = \frac{\omega - \omega_0}{t} = \frac{12 - 0}{3.0} = \frac{12}{3} = 4.0\ \text{rad/s}^2.
\]

**Answer (a):** \(\alpha = 4.0\ \text{rad/s}^2\).

**(b) Angle rotated (radians) in time \(t\):**  
Use \(\theta = \omega_0 t + \tfrac12 \alpha t^2\).

\[
\theta = 0 + \tfrac12(4.0)(3.0^2) = 0.5\times 4.0 \times 9.0 = 2.0 \times 9.0 = 18.0\ \text{rad}.
\]

**Answer (b):** \(\theta = 18.0\ \text{rad}\).

**(c) Tangential speed of point \(P\) at \(t=3\ \text{s}\):**  
Tangential speed \(v_{\text{tan}} = \omega r\).

\[
v_{\text{tan}} = 12.0\ \text{rad/s} \times 0.50\ \text{m} = 6.0\ \text{m/s}.
\]

**Answer (c):** \(v_{\text{tan}} = 6.0\ \text{m/s}\).

**(d) Tangential acceleration \(a_{\text{tan}}\) at \(t=3\ \text{s}\):**  
\(a_{\text{tan}} = \alpha r\).

\[
a_{\text{tan}} = 4.0\ \text{rad/s}^2 \times 0.50\ \text{m} = 2.0\ \text{m/s}^2.
\]

**Answer (d):** \(a_{\text{tan}} = 2.0\ \text{m/s}^2\).

**(e) Radial (centripetal) acceleration \(a_r\) at \(t=3\ \text{s}\):**  
\(a_r = \omega^2 r\).

\[
a_r = (12.0\ \text{rad/s})^2 \times 0.50\ \text{m} = 144.0 \times 0.50 = 72.0\ \text{m/s}^2.
\]

**Answer (e):** \(a_r = 72.0\ \text{m/s}^2\).

---

# End of solutions
