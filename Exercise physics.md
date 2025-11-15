---
tags:
  - mod
  - Physique
---
Created: 2025-11-15

# Physics Assignment — Full Solutions (Obsidian / LaTeX-ready)

> Paste this whole note into an Obsidian file. All math is written using LaTeX between `$$ ... $$` or inline `$ ... $`.  
> Replace the **B.ii figure placeholder** with the force-vs-position data (or an image) to compute numeric answers — instructions and a ready-to-use template are provided in that section.

---

## A. Kinetic Energy

### A.i
**Given:** \(m=2.9\times10^5\ \mathrm{kg}\), \(v=11.2\ \mathrm{km/s}=1.12\times10^4\ \mathrm{m/s}\).

Kinetic energy:
$$
K=\tfrac12 m v^2.
$$

Compute:
$$
v^2=(1.12\times10^4)^2=1.2544\times10^8\ \mathrm{m^2/s^2},
$$
$$
K=\tfrac12(2.9\times10^5)(1.2544\times10^8)=1.81888\times10^{13}\ \mathrm{J}.
$$

**Answer:** \(\boxed{K \approx 1.82\times10^{13}\ \mathrm{J}}\).

---

### A.ii
**Given:** electron mass \(m=9.11\times10^{-31}\ \mathrm{kg}\), kinetic energy \(K=6.7\times10^{-19}\ \mathrm{J}\). Find speed \(v\).

From \(K=\tfrac12mv^2\),
$$
v=\sqrt{\frac{2K}{m}}.
$$

Compute:
$$
\frac{2K}{m}=\frac{2(6.7\times10^{-19})}{9.11\times10^{-31}}\approx1.471\times10^{12},
$$
$$
v=\sqrt{1.471\times10^{12}}\approx1.21\times10^{6}\ \mathrm{m/s}.
$$

**Answer:** \(\boxed{v\approx 1.21\times10^{6}\ \mathrm{m/s}}\).

---

## B. Work

### B.i
**Given:**  
\(\mathbf{d}=(15\ \mathrm{m})\hat{\imath}-(12\ \mathrm{m})\hat{\jmath}\),  
\(\mathbf{F}=(210\ \mathrm{N})\hat{\imath}-(150\ \mathrm{N})\hat{\jmath}\).

Work:
$$
W=\mathbf{F}\cdot\mathbf{d}=F_x d_x + F_y d_y.
$$

Compute:
$$
W=210(15)+(-150)(-12)=3150+1800=4950\ \mathrm{J}.
$$

**Answer:** \(\boxed{W=4950\ \mathrm{J}}\).

---

### B.ii — Work from a force vs. position graph (figure missing)

**Status:** The original exercise asks for the work done as a particle moves along the \(x\)-axis in intervals \([0,5]\), \([5,10]\), \([10,15]\) given a graph \(F_x(x)\) (force vs position). The numeric graph from the PDF was not available in-text here, so **I cannot produce numeric answers**. Below is a complete, copy-paste-ready explanation and templates so you can compute the results immediately after pasting the figure or the force values.

#### Method / theory (what to do)
Work done by a variable force along the \(x\)-axis from \(x=a\) to \(x=b\) is the integral (signed area):
$$
W_{a\to b}=\int_a^b F_x(x)\,dx.
$$

Geometric method (graphical):
- If \(F_x(x)\) is piecewise-constant on a subinterval, work = (force magnitude) × (interval length) with sign (+ if force above \(x\)-axis, − if below).
- If \(F_x(x)\) is linear on a subinterval, compute area of trapezoid or split into triangle + rectangle.
- For triangles: area \(=\tfrac12\cdot\text{base}\cdot\text{height}\) (sign according to whether \(F_x\) is positive or negative).
- For trapezoids with bases \(F_1,F_2\) and width \(\Delta x\): area \(=\tfrac{(F_1+F_2)}{2}\Delta x\).

#### Template: piecewise-constant example (replace numbers)
If the graph is (example placeholder only — **replace** with actual values from your figure):
- On \([0,5]\): \(F_x(x)=+10\ \mathrm{N}\) (constant).
- On \([5,10]\): \(F_x(x)=-6\ \mathrm{N}\) (constant).
- On \([10,15]\): \(F_x(x)=+4\ \mathrm{N}\) (constant).

Then compute:
$$
W_{0\to5}=10\times(5-0)=50\ \mathrm{J},
$$
$$
W_{5\to10}=(-6)\times(10-5)=-30\ \mathrm{J},
$$
$$
W_{10\to15}=4\times(15-10)=20\ \mathrm{J},
$$
Total:
$$
W_{0\to15}=50-30+20=40\ \mathrm{J}.
$$

#### Template: piecewise-linear example (replace numbers)
If on \([0,5]\) the force rises linearly from \(F(0)=2\) to \(F(5)=8\) N, use trapezoid:
$$
W_{0\to5}=\frac{F(0)+F(5)}{2}\times(5-0)=\frac{2+8}{2}\times5=25\ \mathrm{J}.
$$

If any interval crosses the \(x\)-axis (force sign changes), break the interval at the root and compute areas separately with appropriate signs.

---

#### What to paste here so I (or you) can compute numbers immediately:
1. A screenshot or the numeric force values at the key \(x\)-points (e.g., \(F(0),F(2.5),F(5),F(7.5),F(10),...\)).  
2. Or the piecewise functional form (e.g., \(F_x(x)=\begin{cases}10&0\le x<5\\ -6&5\le x<10\\ 4&10\le x\le15\end{cases}\)).  

Once you paste the figure or values, compute each integral using the templates above. If you want, paste the force table here and I'll compute the numbers and replace the placeholders.

---

### B.iii
**Given:** \(\mathbf{F}=(2x\ \mathrm{N})\hat{\imath}+(3\ \mathrm{N})\hat{\jmath}\). Move from \(r_i=(2,3)\ \mathrm{m}\) to \(r_f=(-4,-3)\ \mathrm{m}\).

Work:
$$
W=\int_{r_i}^{r_f}\mathbf{F}\cdot d\mathbf{r}
=\int_{x_i}^{x_f}F_x(x)\,dx+\int_{y_i}^{y_f}F_y\,dy.
$$

Compute \(x\)-part:
$$
\int_{2}^{-4}2x\,dx=[x^2]_{2}^{-4}=(-4)^2-(2)^2=16-4=12\ \mathrm{J}.
$$

Compute \(y\)-part:
$$
\int_{3}^{-3}3\,dy=3(y)\Big|_{3}^{-3}=3(-3-3)=-18\ \mathrm{J}.
$$

Total:
$$
W=12-18=-6\ \mathrm{J}.
$$

**Answer:** \(\boxed{W=-6\ \mathrm{J}}\).

---

## C. Work–Kinetic Energy Theorem

### C.i
**Given:** \(m=40\ \mathrm{kg}\), \(F_{\text{app}}=130\ \mathrm{N}\) (horizontal), distance \(d=5.0\ \mathrm{m}\), coefficient \(\mu=0.30\), \(g=9.80\ \mathrm{m/s^2}\). Start from rest.

(a) Work by applied force:
$$
W_{\text{app}}=F_{\text{app}}d=130\times5=650\ \mathrm{J}.
$$

(b) Friction force magnitude:
$$
f=\mu m g=0.30\times40\times9.80=117.6\ \mathrm{N},
$$
Work done by friction:
$$
W_f=-f d=-117.6\times5=-588.0\ \mathrm{J}.
$$

(c) Net work (change in kinetic energy):
$$
\Delta K = W_{\text{app}}+W_f=650-588=62\ \mathrm{J}.
$$

(d) Final speed (from \(\Delta K=\tfrac12 m v^2\)):
$$
\tfrac12(40)v^2=62 \Rightarrow v^2=\frac{124}{40}=3.1 \Rightarrow v=\sqrt{3.1}\approx1.7607\ \mathrm{m/s}.
$$

**Answers:**  
- (a) \(650\ \mathrm{J}\)  
- (b) \(588.0\ \mathrm{J}\) lost  
- (c) \(\Delta K=62\ \mathrm{J}\)  
- (d) \(\boxed{v\approx1.76\ \mathrm{m/s}}\)

---

### C.ii
**Given:** \(m=10.0\ \mathrm{kg}\), initial speed \(u=1.50\ \mathrm{m/s}\), pulling force \(F_{\text{pull}}=100\ \mathrm{N}\) (parallel to incline), incline angle \(\theta=20.0^\circ\), \(\mu_k=0.400\), displacement along incline \(s=5.00\ \mathrm{m}\), \(g=9.80\ \mathrm{m/s^2}\).

Compute vertical rise:
$$
h=s\sin\theta=5.00\sin20^\circ\approx5.00(0.34202)\approx1.7101\ \mathrm{m}.
$$

(a) Work by gravity:
$$
W_g=-mgh=-10(9.8)(1.7101)\approx-167.6\ \mathrm{J}.
$$

(b) Normal force and kinetic friction:
$$
N=mg\cos\theta=10(9.8)\cos20^\circ\approx10(9.8)(0.939693)\approx92.14\ \mathrm{N},
$$
$$
f_k=\mu_k N\approx0.4\times92.14\approx36.856\ \mathrm{N},
$$
Work by friction:
$$
W_f=-f_k s\approx-36.856\times5.00\approx-184.28\ \mathrm{J}.
$$

(c) Work by the \(100\ \mathrm{N}\) force:
$$
W_{100}=F_{\text{pull}}s=100\times5.00=500\ \mathrm{J}.
$$

(d) Net change in kinetic energy:
$$
\Delta K = W_{100}+W_g+W_f =500 -167.6 -184.28 \approx148.12\ \mathrm{J}.
$$

(e) Final speed from \(\Delta K=\tfrac12 m (v^2-u^2)\):
$$
v^2 = u^2 + \frac{2\Delta K}{m} = (1.5)^2 + \frac{2(148.12)}{10} =2.25 + 29.624 =31.874,
$$
$$
v=\sqrt{31.874}\approx5.645\ \mathrm{m/s}.
$$

**Answers (rounded):**  
- (a) \(W_g\approx -167.6\ \mathrm{J}\)  
- (b) \(W_f\approx -184.3\ \mathrm{J}\)  
- (c) \(W_{100}=500\ \mathrm{J}\)  
- (d) \(\Delta K\approx148.1\ \mathrm{J}\)  
- (e) \(\boxed{v\approx5.65\ \mathrm{m/s}}\)

---

## F. Circular Motion

### F.i (rotating space station)
**Given:** radius \(r=440\ \mathrm{m}\), target centripetal acceleration \(a_c=2.50g=2.50\times9.80=24.5\ \mathrm{m/s^2}\).

(a) Tangential speed:
$$
v=\sqrt{a_c r}=\sqrt{24.5\times440}=\sqrt{10780}\approx103.84\ \mathrm{m/s}.
$$

(b) Period \(T\) (time for one revolution):
$$
T=\frac{2\pi r}{v}=\frac{2\pi(440)}{103.84}\approx26.62\ \mathrm{s}.
$$

(c) Rotations per minute (rpm):
$$
\text{rpm}=\frac{60}{T}\approx\frac{60}{26.62}\approx2.25\ \text{rev/min}.
$$

**Answers:**  
- (a) \(v\approx103.8\ \mathrm{m/s}\)  
- (b) \(T\approx26.6\ \mathrm{s}\)  
- (c) \(\approx2.25\ \mathrm{rpm}\)

---

### F.ii (pail on a string)
**Given:** \(m=5.0\ \mathrm{kg}\), radius \(r=0.900\ \mathrm{m}\), speed \(v=7.0\ \mathrm{m/s}\).

Centripetal acceleration magnitude:
$$
a_c=\frac{v^2}{r}=\frac{7.0^2}{0.9}\approx\frac{49}{0.9}\approx54.444\ \mathrm{m/s^2}.
$$

(a) Acceleration at the highest point is toward the center (downwards) with magnitude \(a_c\approx54.4\ \mathrm{m/s^2}\).

(b) Tension at the top: centripetal requirement is \(m\frac{v^2}{r}=T+mg\) (both toward center)
$$
T = \frac{m v^2}{r} - mg = 5.0\left(\frac{49}{0.9}\right) - 5.0(9.8)\approx272.22-49.0\approx223.22\ \mathrm{N}.
$$

**Answers:**  
- (a) \(a\approx54.4\ \mathrm{m/s^2}\) (downward)  
- (b) \(\boxed{T\approx223\ \mathrm{N}}\)

---

## G. Linear Momentum & Collisions

### G.i
**Given:**  
Particle A: \(m_A=2.50\ \mathrm{kg}\), \(v_{A,i}=25.0\ \mathrm{m/s}\).  
Particle B: \(m_B=7.50\ \mathrm{kg}\), initial \(v_{B,i}=0\).  
After collision: \(v_{A,f}=-5.00\ \mathrm{m/s}\). Find \(v_{B,f}\) and determine elasticity.

**Momentum conservation:**
$$
m_A v_{A,i} + m_B v_{B,i} = m_A v_{A,f} + m_B v_{B,f}.
$$

Solve for \(v_{B,f}\):
$$
2.50(25.0)+7.50(0) = 2.50(-5.00) + 7.50 v_{B,f},
$$
$$
62.50 = -12.50 + 7.50 v_{B,f} \Rightarrow 7.50 v_{B,f}=75.00,
$$
$$
v_{B,f}=10.0\ \mathrm{m/s}.
$$

**Kinetic energy check:**

Initial KE:
$$
K_i=\tfrac12 m_A v_{A,i}^2=\tfrac12(2.5)(25.0^2)=781.25\ \mathrm{J}.
$$

Final KE:
$$
K_f=\tfrac12 m_A v_{A,f}^2 + \tfrac12 m_B v_{B,f}^2
=0.5(2.5)(5.0^2) + 0.5(7.5)(10.0^2)
=31.25 + 375.00 =406.25\ \mathrm{J}.
$$

Since \(K_f\neq K_i\), mechanical kinetic energy is **not conserved**: the collision is **inelastic**.

**Answers:**  
- \( \boxed{v_{B,f}=10.0\ \mathrm{m/s}} \)  
- Collision is **inelastic** (kinetic energy decreased from \(781.25\) J to \(406.25\) J).

---

## Notes & Next Steps

- **B.ii**: paste the force-vs-position image or a small table of force values (e.g., `x: 0,5,10,15` and `F: ...`) into this document and use the templates above, or send them here and I will compute and replace the placeholders with exact numeric results and show every intermediate step in LaTeX.
- If you want this entire note exported to a PDF or a nicely formatted LaTeX file (`.tex`) I can generate that for you — tell me the filename you want and I will produce a downloadable file.

---

### Quick copy checklist for B.ii (paste this into Obsidian under B.ii and fill values)
```latex
% Example: replace with actual F(x) values from your graph
F_x(x)=\begin{cases}
F_1 & 0\le x < 5\\
F_2 & 5\le x <10\\
F_3 & 10\le x \le15
\end{cases}

W_{0\to5}=\int_0^5 F_1\,dx = F_1(5-0) = 5F_1

W_{5\to10}=\int_5^{10} F_2\,dx = F_2(10-5) = 5F_2

W_{10\to15}=\int_{10}^{15} F_3\,dx = F_3(15-10) = 5F_3

W_{0\to15}=5(F_1+F_2+F_3)
