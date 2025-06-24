### Project: PINN Solution to the 1D Schrödinger Equation

This project implements a **Physics-Informed Neural Network (PINN)** using **DeepXDE** and **TensorFlow** to solve the **1D time-independent Schrödinger equation** for a particle in an **infinite potential well**.

The model learns both the **wavefunction** $\psi(x)$ and the **energy eigenvalue** $E$ directly from the **physics of the problem** — with **no labeled data** — by minimizing the **residuals** of the differential equation.

---

### 📌 Key Highlights

* **Domain:**
  $x \in [-1, 1]$ (infinite square well)

* **Equation:**

  $$
  -\frac{d^2 \psi(x)}{dx^2} = E \psi(x)
  $$

* **Boundary Conditions:**
  $\psi(-1) = \psi(1) = 0$

* **Learned Variable:**
  Energy eigenvalue $E$ (trainable TensorFlow variable)

* **Network Architecture:**
  Fully-connected neural network
  $5$ hidden layers × $120$ neurons each, with **tanh** activation

* **Accuracy Achieved:**
  Final error within **\~5.0039%** of the true ground state energy
  $E_1 = \pi^2 \approx 9.8696$

---

### 🎯 Goals

* Solve a **quantum mechanical eigenvalue problem** using neural networks
* Demonstrate how **physics laws** (not data!) can guide learning
* **Visualize** wavefunctions and probability densities
* Automatically learn the **ground state energy level**

---

### 📊 Output Visualizations

* Learned wavefunction $\psi(x)$
* True vs. Learned comparison
* Probability density $|\psi(x)|^2$
* Heatmap of $\psi(x)$

---

### 📦 Technologies Used

* **Python**
* **TensorFlow 2.x**
* **DeepXDE**
* **NumPy**
* **Matplotlib**
