# PSO-Based Color Image Enhancement  
Enhancing Low-Light Images Using Particle Swarm Optimization and Perceptual Metrics (PSNR + SSIM)

---

## Project Overview

Ever taken a picture in low light, only to end up with a dull, unclear image?

This project aims to fix that — using **Particle Swarm Optimization (PSO)** to **automatically enhance low-light images** by optimizing **brightness**, **contrast**, and **gamma** settings. The enhancement process is **guided by human-perception-inspired metrics** like **PSNR** and **SSIM**, ensuring results aren't just pixel-perfect, but also visually appealing.

---

## Core Idea

Instead of manually tweaking enhancement parameters (and guessing what looks good), we let a **swarm of particles** intelligently search for the **best combination** of:

- 🔆 **Brightness** — How light or dark the image is.
- ⚫️ **Contrast** — How stretched the difference is between shadows and highlights.
- 📈 **Gamma** — How mid-tones are redistributed to control overall tone.

We evaluate each enhanced image against a ground-truth **well-lit version** using:

-  **PSNR (Peak Signal-to-Noise Ratio)** – Measures pixel-wise error.
-  **SSIM (Structural Similarity Index)** – Mimics human perception of visual quality.

---

## What is Particle Swarm Optimization?

**PSO** is a nature-inspired optimization algorithm based on how birds flock or fish school. Each "particle" represents a possible solution and moves through the solution space, influenced by its own experience and that of its neighbors.

In our case:
- Each particle = a combination of `[brightness, contrast, gamma]`
- Fitness = `PSNR + SSIM` of the enhanced image
- Goal = Find the **best enhancement parameters** that make the image closest to the ground truth

---

## Sample Result

 Low-Light Input  Ground Truth  Enhanced Output 

 ![Low-Light](https://github.com/ishika-pandey/Image_Enhancement_BTP/blob/main/output_enhanced.png)

📌 _Note: You can customize and run this on your own dataset easily._
