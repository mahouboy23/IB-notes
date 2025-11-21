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

Created: 2025-11-23  
Source: [[Final_Exam_Physics_I_DUNIS_Spring_2024.pdf]]

# Final Exam – Physics I (Complete Solutions)

---

# Question 1: Multiple Choice

**Question:**  
Choose the correct option:

1. The unit of work is joule. The other physical quantity that has same unit is  
(a) power (b) velocity (c) energy (d) force  

2. A ball is dropped from a height of 10 m  
(a) Its potential energy increases and kinetic energy decreases during the fall  
(b) PE = KE during the fall  
(c) Potential energy decreases and kinetic energy increases during the fall  
(d) Potential energy = 0 and KE is maximum while falling  

3. If the velocity of a body is doubled, its kinetic energy  
(a) gets doubled (b) becomes half (c) does not change (d) becomes 4 times  

4. A student carries a 5 kg bag up 2 m. Work done is  
(a) 1 J (b) 10 J (c) 100 J (d) 1000 J  

5. Work is 0 if  
(a) displacement opposite to force  
(b) displacement in same direction  
(c) displacement perpendicular to force  
(d) displacement at an angle  

---

### **Solutions**

1. **Answer:** (c) — energy  
2. **Answer:** (c)  
3. **Answer:** (d)  
4. **Answer:** (c)  
5. **Answer:** (c)

---

# Question 2: Rod Hanging From Two Cords

**Question:**  
A uniform rod 1.00 m long weighs 250.0 N and is hanging from two cords, one connected  
xA = 40.0 cm from the center, and the other xB = 20.0 cm from the center.  
Find tensions \(T_A\) and \(T_B\).

(("diagram: rod with cords at xA and xB"))

---

### **Solution**

**Given:**  
- \(W = 250\ \text{N}\)  
- \(x_A = 0.40\ \text{m}\)  
- \(x_B = 0.20\ \text{m}\)

**1. Force equilibrium:**  
$$T_A + T_B = 250$$

**2. Torque equilibrium about center:**  
$$0.20T_B = 0.40T_A$$  
$$T_B = 2T_A$$

Substitute:  
$$T_A + 2T_A = 250$$  
$$T_A = 83.3\ \text{N}$$  
$$T_B = 166.7\ \text{N}$$

---

### **Final Answers**
- \(T_A = 83.3\ \text{N}\)  
- \(T_B = 166.7\ \text{N}\)

---

# Question 3: Inelastic Collision (Clay Balls)

**Question:**  
Two balls of masses \(m_1 = 1.0\ \text{kg}\) and \(m_2 = 2.5\ \text{kg}\) travel with  
speeds \(v_1 = 2.0\ \text{m/s}\) and \(v_2 = 1.0\ \text{m/s}\). They collide at the origin  
(Fig. I). They stick together and move in the direction shown.  
Find the direction (angle) and resultant speed.

(("diagram: two-ball collision vectors"))

---

### **Solution**

Let ball 1 move along +x, ball 2 along +y.

**Initial momenta:**

- \(p_1 = m_1 v_1 = 1.0 \cdot 2.0 = 2.0\ \text{kg·m/s}\) (x-direction)  
- \(p_2 = m_2 v_2 = 2.5 \cdot 1.0 = 2.5\ \text{kg·m/s}\) (y-direction)

**Total momentum vector:**

$$\vec{p} = (2.0)\hat{i} + (2.5)\hat{j}$$

**Angle of motion:**  
$$\theta = \tan^{-1}\left(\frac{2.5}{2.0}\right) = 51.34^\circ$$

**Magnitude of momentum:**  
$$p = \sqrt{2.0^2 + 2.5^2} = \sqrt{10.25} = 3.20\ \text{kg·m/s}$$

**Total mass after sticking:**  
$$M = 1.0 + 2.5 = 3.5\ \text{kg}$$

**Resultant speed:**  
$$v = \frac{p}{M} = \frac{3.20}{3.5} = 0.91\ \text{m/s}$$

---

### **Final Answers**
- **Direction:** \(51.3^\circ\) above +x  
- **Speed:** \(0.91\ \text{m/s}\)

---

# Question 4: Rotational Kinematics

**Question:**  
A wheel rotating at \(4.0\ \text{rev/s}\) has a radius \(R = 25\ \text{cm}\).  
Find:  
(a) angular speed  
(b) tangential (linear) speed  
(c) centripetal acceleration

---

### **Solution**

**(a) Angular speed**

Convert rev/s to rad/s:  
$$\omega = 2\pi f = 2\pi(4.0) = 25.13\ \text{rad/s}$$

**(b) Tangential speed**  
$$v = \omega R = 25.13(0.25) = 6.28\ \text{m/s}$$

**(c) Centripetal acceleration**  
$$a_c = \omega^2 R = (25.13)^2 (0.25) = 158\ \text{m/s}^2$$

---

### **Final Answers**
- \(\omega = 25.13\ \text{rad/s}\)  
- \(v = 6.28\ \text{m/s}\)  
- \(a_c = 158\ \text{m/s}^2\)

---

# Question 5: Torque on a Door

**Question:**  
A force of 40 N is applied at the edge of a door 90 cm wide at an angle of \(60^\circ\).  
Find the torque.

(("diagram: force applied at angle on door"))

---

### **Solution**

$$\tau = rF\sin\theta$$  
$$\tau = (0.90)(40)\sin60^\circ$$  
$$\tau = 36 \cdot 0.866 = 31.2\ \text{N·m}$$

---

### **Final Answer**
- \(\tau = 31.2\ \text{N·m}\)

---

# Question 6: Angular Acceleration

**Question:**  
A wheel accelerates uniformly from rest to \(20\ \text{rad/s}\) in 5.0 s.  
Find angular acceleration and angle rotated.

---

### **Solution**

**Angular acceleration:**  
$$\alpha = \frac{\Delta\omega}{t} = \frac{20 - 0}{5} = 4\ \text{rad/s}^2$$

**Angle rotated:**  
Use  
$$\theta = \omega_0 t + \frac12 \alpha t^2$$  
$$\theta = 0 + \frac12(4)(25) = 50\ \text{rad}$$

---

### **Final Answers**
- \(\alpha = 4\ \text{rad/s}^2\)  
- \(\theta = 50\ \text{rad}\)

---

# Question 7: Angular Momentum

**Question:**  
A disk of moment of inertia \(I = 0.20\ \text{kg·m}^2\) rotates at \(10\ \text{rad/s}\).  
Find its angular momentum and its rotational kinetic energy.

---

### **Solution**

**Angular momentum:**  
$$L = I\omega = 0.20(10) = 2.0\ \text{kg·m}^2/\text{s}$$

**Rotational KE:**  
$$K = \frac12 I\omega^2 = \frac12(0.20)(100) = 10\ \text{J}$$

---

### **Final Answers**
- \(L = 2.0\ \text{kg·m}^2/\text{s}\)  
- \(K = 10\ \text{J}\)

---

# Question 8: Work Done by Variable Force

**Question:**  
A force varies with position as  
$$F(x) = 5x^2$$  
Find the work done from \(x = 0\) to \(x = 3\).

---

### **Solution**

Work = area under curve:

$$W = \int_0^3 5x^2\, dx = 5\left[\frac{x^3}{3}\right]_0^3$$  
$$W = 5 \cdot 9 = 45\ \text{J}$$

---

### **Final Answer**
- \(W = 45\ \text{J}\)

---

# End of Exam Solutions
