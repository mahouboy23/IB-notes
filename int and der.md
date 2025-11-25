---
tags:
  - mod
  - Math
---
Created: 2025-11-21

Created: 2025-11-23  
Source: Personal physics calculus reference

# Calculus Essentials for Physics (Derivatives & Integrals)

---

# 1. What Derivatives Mean in Physics
- **Derivative = rate of change**  
  $$\text{derivative} = \frac{d(\text{something})}{dt}$$

### Common physics meanings
- **Velocity:**  
  $$v = \frac{dx}{dt}$$
- **Acceleration:**  
  $$a = \frac{dv}{dt} = \frac{d^2x}{dt^2}$$
- **Angular velocity:**  
  $$\omega = \frac{d\theta}{dt}$$
- **Angular acceleration:**  
  $$\alpha = \frac{d\omega}{dt}$$

(("diagram: slope of position vs time gives velocity"))

---

# 2. What Integrals Mean in Physics
- **Integral = accumulated quantity**  
  $$\int (\text{rate})\ dt = \text{total amount}$$

### Common physics meanings
- Position from velocity:  
  $$x = \int v\, dt$$
- Velocity from acceleration:  
  $$v = \int a\, dt$$
- Work:  
  $$W = \int F\, dx$$
- Area under graph:  
  $$\text{Area} = \int y(x)\, dx$$  
  (used all the time for variable forces)

---

# 3. Derivative Rules You Actually Use

### 1. Power Rule  
If  
$$f(x)=x^n$$  
Then  
$$f'(x)=nx^{n-1}$$

Examples:  
- \(\frac{d}{dx}(x^2)=2x\)  
- \(\frac{d}{dx}(x^3)=3x^2\)  
- \(\frac{d}{dx}(1/x)=\frac{d}{dx}(x^{-1})=-x^{-2}\)

### 2. Constant Rule  
$$\frac{d}{dx}(c)=0$$

### 3. Constant Multiple  
$$\frac{d}{dx}[c f(x)] = c f'(x)$$

Used for:  
- \(a t^2\) terms in kinematics  
- \(mgh\), \(k x^2\), etc.

### 4. Sum Rule  
$$\frac{d}{dx}[f+g] = f'+g'$$

### 5. Exponential/Trig (only ones needed for physics 1)  
- \(\frac{d}{dx}(\sin x)=\cos x\)  
- \(\frac{d}{dx}(\cos x)=-\sin x\)  
- \(\frac{d}{dx}(e^x)=e^x\)

---

# 4. Integral Rules You Actually Need

### 1. Power Rule for Integrals  
If  
$$\int x^n dx = \frac{x^{n+1}}{n+1} + C \quad (n\neq -1)$$

Examples:
- \(\int x^2 dx = x^3/3\)  
- \(\int x^{-1} dx = \ln |x|\)  
- \(\int 3x dx = \frac{3x^2}{2}\)

### 2. Constant Multiple  
$$\int c f(x)\ dx = c\int f(x)\ dx$$

### 3. Integrals of Common Functions  
- \(\int \sin x\ dx = -\cos x\)  
- \(\int \cos x\ dx = \sin x\)  
- \(\int e^x\ dx = e^x\)

---

# 5. What You Need for Physics Problems

## **A. Constant Acceleration Motion (Kinematics)**

Using  
$$a = \frac{dv}{dt}$$  
Integrate:  
$$v = at + v_0$$

Then integrate again:  
$$x = \int v dt = \int (v_0 + at) dt = v_0 t + \frac12 a t^2$$

**Conclusion:**  
Kinematic equations = simple integrals of polynomials.

---

## **B. Work From Force**
If force is constant:
$$W = Fx$$

If force changes:  
$$W = \int F(x)\, dx$$

Example:  
If  
$$F(x)=5x^2$$  
Then  
$$W = \int_0^3 5x^2 dx = 45\ \text{J}$$  

---

## **C. Torque and Rotation**
Angular displacement:
$$\theta = \int \omega dt$$  
Angular velocity:
$$\omega = \int \alpha dt$$

If α is constant:
$$\omega = \omega_0 + \alpha t$$  
$$\theta = \omega_0 t + \frac12 \alpha t^2$$

Same pattern as linear motion.

---

## **D. Center of Mass**
For continuous objects:
$$x_{cm} = \frac{1}{M} \int x\ dm$$

For rods or disks: this becomes:
$$x_{cm} = \frac{\int x\, \lambda dx}{\int \lambda dx}$$

(You rarely need the full integral; mostly formulas.)

---

## **E. Momentum & Impulse**
Impulse is an integral:
$$J = \int F dt = \Delta p$$

When force is graph-based (triangle, rectangle, etc.), the integral becomes **area under F(t)**.

---

# 6. How to Approach Integration in Physics (Strategy)

### 1. Identify the *rate*  
- If you see acceleration → integrate → velocity.  
- If you see velocity → integrate → position.  
- If you see force → integrate in x → work.  
- If you see force → integrate in t → impulse.

### 2. Check if the function is a simple polynomial  
Most exam problems give F(x), a(t), v(t) as:
- linear  
- quadratic  
- constant

→ Use power rule only.

### 3. Draw the graph  
Work, impulse, and power questions are almost always areas under curves.

### 4. Don’t overthink constants  
If no initial condition given → just write +C.  
If initial condition given → solve for C.

---

# 7. Quick Table: The Integrals You Use the Most

| Physics Use | Calculation |
|-------------|-------------|
| Position → velocity | \(v = \frac{dx}{dt}\) |
| Velocity → acceleration | \(a = \frac{dv}{dt}\) |
| Velocity from accel | \(v = \int a\, dt\) |
| Position from velocity | \(x = \int v\, dt\) |
| Work (variable force) | \(W = \int F\, dx\) |
| Impulse | \(J = \int F\, dt\) |
| Angular motion | \(\omega = \int \alpha dt\),  \(\theta = \int \omega dt\) |
| Spring work | \(W = \int kx\, dx = \frac12 kx^2\) |
| KE from velocity function | \(K = \int F\, dx\) via work-energy |

---

# 8. Final Mini-Summary (You Will Use These Every Time)

### Derivatives  
- Power rule  
- Trig derivatives (sin, cos)  
- Velocity = dx/dt  
- Acceleration = dv/dt  

### Integrals  
- Power rule  
- Work = ∫F dx  
- Impulse = ∫F dt  
- θ, ω from α  
- v, x from a  

---

# That’s It — The Physics Calculus Toolkit
This covers **100% of what you need** for Physics I and rotational motion, without unnecessary math theory.

Let me know if you want:
- a **practice sheet**
- a **formula cheat-sheet card**
- spaced-repetition flashcards (Obsidian SR plugin format)
