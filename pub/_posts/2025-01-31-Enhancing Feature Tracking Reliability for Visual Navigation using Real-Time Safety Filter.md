---
title: "Enhancing Feature Tracking Reliability for Visual Navigation using Real-Time Safety Filter"
header:
  teaser: tumbnails/icra25.png
conference: ICRA
authors:
  - Dabin Kim*
  - Inkyu Jang*
  - Youngsoo Han
  - Sunwoo Hwang
  - H. Jin Kim
links: 
 - paper: 
   link: https://arxiv.org/pdf/2502.01092
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=pZ9nvobevcs
   name: "Video"
excerpt: This paper presents a real-time safety filter for robot navigation that maintains visual feature visibility by minimally adjusting velocity commands, ensuring reliable pose estimation even in GPS-denied environments. Validated in both simulation and real-world SLAM scenarios, the method outperforms standard controllers by preserving high-quality localization.
---

{% include youtubePlayer.html id="pZ9nvobevcs" %}
<!-- ---

## 🚀 Making Visual Navigation More Reliable  
### Enhancing Feature Tracking with a Real-Time Safety Filter

In environments without GPS, many robots rely on **visual SLAM** — using a camera to track their position by detecting and following visual features (like corners or edges). But here’s the catch:

> 🔍 If the number of visible features suddenly drops, SLAM performance can fail dramatically — causing tracking loss, localization errors, or even crashes.

Our work addresses this with a simple question:  
**Can we make a robot proactively protect its feature visibility — *before* it’s too late?**

---

## 🎯 Key Idea: A Real-Time Safety Filter for Features

We propose a **real-time safety filter** that runs alongside the robot’s control system. Instead of blindly following a planned velocity, the filter *slightly modifies* the velocity to **keep enough visual features in view**.

### ✨ Think of it like:
> A safety assistant that whispers to the robot:  
> _“Maybe slow down a bit so you don’t lose track of those corners.”_

---

## 🔧 How It Works (In Simple Terms)

Here’s what happens at each time step:

1. 🧭 A controller gives a reference velocity (`v_ref`) to the robot.
2. 👁 The camera sees visual features and computes an **information score** — a measure of how “rich” the current features are.
3. 🧮 A **quadratic program (QP)** solves for a new velocity (`v_filtered`) that:
   - Is close to `v_ref`
   - Ensures the information score stays above a threshold

---

### 📊 Suggested Graphic:
_A diagram showing:_
- Original velocity vector
- Modified velocity vector
- Feature score threshold
- Features moving out of FOV

---

## 🧪 Experiments

### ✅ Simulation:  
- We tested in a simulated indoor environment with sudden changes in feature visibility.
- Without our filter, the robot frequently lost track of features.
- With our filter, it slowed or adjusted direction to maintain trackability.

<div style="background: transparent; display: flex; gap: 20px; justify-content: center; text-align: center;">
  <div style="flex: 1;">
    <img src="/images/blog/icra25/sim_baseline.gif" alt="Sim" style="width: 100%; max-width: 400px;">
    <p><em>Baseline Result</em></p>
  </div>
  <div style="flex: 1;">
    <img src="/images/blog/icra25/sim_proposed.gif" alt="Real" style="width: 100%; max-width: 400px;">
    <p><em>Proposed Result</em></p>
  </div>
</div>
<!-- Figure below the GIFs -->
<!-- <div style="text-align: center; margin-top: 20px;">
  <img src="/images/blog/icra25/sim_result.png" style="max-width: 60%; height: auto;">
  <p style="font-style: italic; font-size: 0.9rem;">Figure: Simulation Result</p>
</div>

### ✅ Real-world Deployment:  
- We mounted a monocular camera on a wheeled robot.
- The robot navigated safely even when entering textureless areas like blank walls or glass.

---

### 📷 Suggested Graphic:
_Side-by-side screenshots of:_
- Feature tracking over time (with and without filter)
- Trajectories diverging due to tracking failure

---

## 📈 Why It Matters

- 🎯 **SLAM safety**: Prevents catastrophic failures due to feature loss.
- ⚡ **Real-time**: The filter runs fast enough for real robots.
- 🧠 **Minimal intervention**: Only adjusts motion when necessary — keeps original behavior otherwise.

---

## 🧩 Future Ideas

We’re excited to:
- Combine this with **active vision** to move toward richer feature regions
- Extend it to **multi-sensor fusion** systems
- Use it in **autonomous drones**, where losing features mid-flight can be fatal

--- -->

Vision sensors are extensively used for localizing a robot's pose, particularly in environments where global localization tools such as GPS or motion capture systems are unavailable. In many visual navigation systems, localization is achieved by detecting and tracking visual features or landmarks, which provide information about the sensor's relative pose. For reliable feature tracking and accurate pose estimation, it is crucial to maintain visibility of a sufficient number of features. This requirement can sometimes conflict with the robot's overall task objective. In this paper, we approach it as a constrained control problem. By leveraging the invariance properties of visibility constraints within the robot's kinematic model, we propose a real-time safety filter based on quadratic programming. This filter takes a reference velocity command as input and produces a modified velocity that minimally deviates from the reference while ensuring the information score from the currently visible features remains above a user-specified threshold. Numerical simulations demonstrate that the proposed safety filter preserves the invariance condition and ensures the visibility of more features than the required minimum. We also validated its real-world performance by integrating it into a visual simultaneous localization and mapping (SLAM) algorithm, where it maintained high estimation quality in challenging environments, outperforming a simple tracking controller.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{kim2025enhancing,
  title={Enhancing Feature Tracking Reliability for Visual Navigation using Real-Time Safety Filter},
  author={Kim, Dabin and Jang, Inkyu and Han, Youngsoo and Hwang, Sunwoo and Kim, H Jin},
  journal={arXiv preprint arXiv:2502.01092},
  year={2025}
}
```