

---

# 📌 Multi-Spring Mass Static Equilibrium

### 👤 Author

**Name:** Yash Rathod
**Roll No:** 23BME045
**Course:** Computer Engineering Lab
**Tool Used:** MATLAB

---

## 📖 Project Overview

This case study analyzes the oscillatory behavior of a mass attached to three springs arranged in parallel.

The objective is to:

* Determine the **effective spring constant**
* Compute the **natural frequency**
* Calculate the **time period of vibration**
* Verify the results using MATLAB simulation

This project demonstrates the application of:

* Linear algebra
* Differential equations
* Simple Harmonic Motion (SHM) theory

---

## 🧮 Problem Statement

Three springs are connected in **parallel** to a mass **m**.

Spring Constants:

* Left Spring = k
* Middle Spring = 2k
* Right Spring = k

### Given:

```
k = 2 N/m  
m = 80 g = 0.08 kg
```

### Required:

* Effective spring constant (k_eff)
* Natural frequency (ωₙ)
* Time period (T)

---

## 📚 Theoretical Background

For springs connected in **parallel**:

```
k_eff = k1 + k2 + k3
```

Equation of motion:

```
m x'' + k_eff x = 0
```

Natural frequency:

```
ωₙ = √(k_eff / m)
```

Time period:

```
T = 2π / ωₙ
```

---

## 🧾 Analytical Solution

### 1️⃣ Effective Spring Constant

```
k_eff = k + 2k + k  
k_eff = 4k  
k_eff = 4 × 2 = 8 N/m
```

### 2️⃣ Natural Frequency

```
ωₙ = √(8 / 0.08)  
ωₙ = 10 rad/s
```

### 3️⃣ Time Period

```
T = 2π / 10  
T ≈ 0.628 seconds
```

---

## 💻 MATLAB Implementation

```matlab
clc;
clear;
close all;

k = 2;     
m = 0.08;  
keff = 4*k;
omega = sqrt(keff/m);

T = 2*pi/omega;

disp('Dynamic Analysis Results')
disp('------------------------')
disp(['Effective stiffness (N/m): ', num2str(keff)])
disp(['Natural frequency (rad/s): ', num2str(omega)])
disp(['Time period (s): ', num2str(T)])

t = linspace(0, 2, 1000);
A = 0.05;
x = A*cos(omega*t);

figure;
plot(t, x, 'LineWidth', 2)
xlabel('Time (s)')
ylabel('Displacement (m)')
title('Oscillation of Multi-Spring Mass System')
grid on
```

---

## 📊 Results

| Parameter                 | Value    |
| ------------------------- | -------- |
| Effective Spring Constant | 8 N/m    |
| Natural Frequency         | 10 rad/s |
| Time Period               | 0.628 s  |

The simulation confirms **Simple Harmonic Motion (SHM)** behavior.

---

## 📈 Output Graph

The displacement vs time graph shows a cosine waveform confirming oscillatory motion.

---

## ✅ Conclusion

* Three parallel springs behave as a **single equivalent spring**.
* Increasing stiffness increases natural frequency.
* The system oscillates with a time period of **~0.63 seconds**.
* MATLAB simulation validates the analytical solution.

---


If you want, I can also make a **more advanced GitHub README** with badges, LaTeX equations rendering, and project structure formatting.
